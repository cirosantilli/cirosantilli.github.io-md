<h1 id="runwayml-stable-diffusion">runwayml/stable-diffusion</h1>

↑ **Parent:** [Open source text-to-image model](open-source-text-to-image-model.md)

[https://github.com/runwayml/stable-diffusion](https://github.com/runwayml/stable-diffusion)

[Conda](conda.md) install is a bit annoying, but gets the job done. The generation quality is very good.

Someone should package this better for end user "just works after Conda install" image generation, it is currently much more of a library setup.

Tested on [Amazon EC2](amazon-elastic-compute-cloud.md) on a [g5.xlarge](g5-xlarge.md) machine, which has an [Nvidia A10G](nvidia-a10g.md), using the [AWS Deep Learning Base GPU AMI (Ubuntu 20.04)](aws-deep-learning-base-gpu-ami-ubuntu-20-04.md) image.

First install [Conda](conda.md) as per [Section "Install Conda on Ubuntu"](install-conda-on-ubuntu.md), and then just follow the instructions from the README, notably the [Reference sampling script](https://github.com/runwayml/stable-diffusion/tree/08ab4d326c96854026c4eb3454cd3b02109ee982#reference-sampling-script) section.
```
git clone https://github.com/runwayml/stable-diffusion
cd stable-diffusion/
git checkout 08ab4d326c96854026c4eb3454cd3b02109ee982
conda env create -f environment.yaml
conda activate ldm
mkdir -p models/ldm/stable-diffusion-v1/
wget -O models/ldm/stable-diffusion-v1/model.ckpt https://huggingface.co/CompVis/stable-diffusion-v-1-4-original/resolve/main/sd-v1-4.ckpt
python scripts/txt2img.py --prompt "a photograph of an astronaut riding a horse" --plms
```
This took about 2 minutes and generated 6 images under `outputs/txt2img-samples/samples`, includining an image `outputs/txt2img-samples/grid-0000.png` which is a grid montage containing all the six images in one:

![](https://raw.githubusercontent.com/cirosantilli/media/master/Runwayml_stable-diffusion_a-photograph-of-an-astronaut-riding-a-horse.png)

TODO how to change the number of images?

A quick attempt at removing their useless safety features (watermark and [NSFW](not-safe-for-work.md) text filter) is:
```
diff --git a/scripts/txt2img.py b/scripts/txt2img.py
index 59c16a1..0b8ef25 100644
--- a/scripts/txt2img.py
+++ b/scripts/txt2img.py
@@ -87,10 +87,10 @@ def load_replacement(x):
 def check_safety(x_image):
     safety_checker_input = safety_feature_extractor(numpy_to_pil(x_image), return_tensors="pt")
     x_checked_image, has_nsfw_concept = safety_checker(images=x_image, clip_input=safety_checker_input.pixel_values)
-    assert x_checked_image.shape[0] == len(has_nsfw_concept)
-    for i in range(len(has_nsfw_concept)):
-        if has_nsfw_concept[i]:
-            x_checked_image[i] = load_replacement(x_checked_image[i])
+    #assert x_checked_image.shape[0] == len(has_nsfw_concept)
+    #for i in range(len(has_nsfw_concept)):
+    #    if has_nsfw_concept[i]:
+    #        x_checked_image[i] = load_replacement(x_checked_image[i])
     return x_checked_image, has_nsfw_concept


@@ -314,7 +314,7 @@ def main():
                             for x_sample in x_checked_image_torch:
                                 x_sample = 255. * rearrange(x_sample.cpu().numpy(), 'c h w -> h w c')
                                 img = Image.fromarray(x_sample.astype(np.uint8))
-                                img = put_watermark(img, wm_encoder)
+                                # img = put_watermark(img, wm_encoder)
                                 img.save(os.path.join(sample_path, f"{base_count:05}.png"))
                                 base_count += 1
```
but that produced 4 black images and only two unfiltered ones. Also likely the lack of sexual training data makes its porn suck, and not in the good way.

## ↑ Ancestors (14)

1. [Open source text-to-image model](open-source-text-to-image-model.md)
2. [Text-to-image model](text-to-image-model.md)
3. [Text-to-image generation](text-to-image-generation.md)
4. [Image generation](image-generation.md)
5. [Generative AI by modality](generative-ai-by-modality.md)
6. [Generative AI](generative-ai.md)
7. [AI by capability](ai-by-capability.md)
8. [Artificial intelligence](artificial-intelligence-split.md)
9. [Machine learning](machine-learning-split.md)
10. [Computer](computer-split.md)
11. [Information technology](information-technology.md)
12. [Area of technology](area-of-technology.md)
13. [Technology](technology-split.md)
14. [Ciro Santilli's Homepage](split.md)
