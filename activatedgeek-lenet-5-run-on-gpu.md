<h1 id="activatedgeek-lenet-5-run-on-gpu">activatedgeek/LeNet-5 run on GPU</h1>

↑ **Parent:** [Activatedgeek/LeNet-5](activatedgeek-lenet-5.md)

By default, the setup runs on [CPU](central-processing-unit.md) only, not [GPU](graphics-processing-unit.md), as could be seen by running [htop](htop.md). But by the magic of [PyTorch](pytorch.md), modifying the program to run on the [GPU](graphics-processing-unit.md) is trivial:
```
cat << EOF | patch
diff --git a/run.py b/run.py
index 104d363..20072d1 100644
--- a/run.py
+++ b/run.py
@@ -24,7 +24,8 @@ data_test = MNIST('./data/mnist',
 data_train_loader = DataLoader(data_train, batch_size=256, shuffle=True, num_workers=8)
 data_test_loader = DataLoader(data_test, batch_size=1024, num_workers=8)

-net = LeNet5()
+device = 'cuda'
+net = LeNet5().to(device)
 criterion = nn.CrossEntropyLoss()
 optimizer = optim.Adam(net.parameters(), lr=2e-3)

@@ -43,6 +44,8 @@ def train(epoch):
     net.train()
     loss_list, batch_list = [], []
     for i, (images, labels) in enumerate(data_train_loader):
+        labels = labels.to(device)
+        images = images.to(device)
         optimizer.zero_grad()

         output = net(images)
@@ -71,6 +74,8 @@ def test():
     total_correct = 0
     avg_loss = 0.0
     for i, (images, labels) in enumerate(data_test_loader):
+        labels = labels.to(device)
+        images = images.to(device)
         output = net(images)
         avg_loss += criterion(output, labels).sum()
         pred = output.detach().max(1)[1]
@@ -84,7 +89,7 @@ def train_and_test(epoch):
     train(epoch)
     test()

-    dummy_input = torch.randn(1, 1, 32, 32, requires_grad=True)
+    dummy_input = torch.randn(1, 1, 32, 32, requires_grad=True).to(device)
     torch.onnx.export(net, dummy_input, "lenet.onnx")

     onnx_model = onnx.load("lenet.onnx")
EOF
```
and leads to a faster runtime, with less `user` as now we are spending more time on the GPU than CPU:
```
real    1m27.829s
user    4m37.266s
sys     0m27.562s
```

## ↑ Ancestors (14)

1. [Activatedgeek/LeNet-5](activatedgeek-lenet-5.md)
2. [LeNet implementation](lenet-implementation.md)
3. [LeNet](lenet.md)
4. [List of convolutional neural networks](list-of-convolutional-neural-networks.md)
5. [Convolutional neural network](convolutional-neural-network.md)
6. [ANN model](ann-model.md)
7. [Artificial neural network](artificial-neural-network.md)
8. [Neural network](neural-network.md)
9. [Machine learning](machine-learning-split.md)
10. [Computer](computer-split.md)
11. [Information technology](information-technology.md)
12. [Area of technology](area-of-technology.md)
13. [Technology](technology-split.md)
14. [Ciro Santilli's Homepage](split.md)
