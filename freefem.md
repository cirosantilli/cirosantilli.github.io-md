# FreeFem

↑ **Parent:** [Partial differential equation solver](partial-differential-equation-solver.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/FreeFem++)

[https://freefem.org/](https://freefem.org/)

[https://github.com/FreeFem/FreeFem-sources](https://github.com/FreeFem/FreeFem-sources)

Started in 1987 and written in Pascal, by the French from [Pierre and Marie Curie University](pierre-and-marie-curie-university.md), the French are really strong in [numerical analysis](numerical-analysis.md).

Ciro wasn't expecting it to be as old. Ported to C++ in 1992.

The fact that French wrote it can be seen in the documentation, for example [https://doc.freefem.org/tutorials/index.html](https://doc.freefem.org/tutorials/index.html) uses file extension `mycode.edp` instead of `mycode.pde` where `dep` stands for "[Équation aux dérivées partielles](https://fr.wikipedia.org/wiki/Équation_aux_dérivées_partielles)".

Besides the painful build, using FreeFem is relatively simple, as can be seen from the examples on the website.

They do use a [domain-specific language](domain-specific-language.md) on the examples, which appears to be the main/only interface, which is a bad thing, Ciro would rather have a [Python](python-programming-language.md) [API](application-programming-interface.md) as the "main API", which is more the approach taken by the [FEniCS Project](fenics-project.md), but so be it. This [domain-specific language](domain-specific-language.md) business means that you always stumble upon basic stuff you want to do but can't, and then you have to think about how to share data between the simulation and the plotting. The plotting notably is super complex and they can't implement all of what people want, upstream examples often offload that to gnuplot. This is potentially a big advantage of [FEniCS Project](fenics-project.md).

It nice though that they do have some graphics out of the box, as that allows to quickly debug common problems.

Uses [variational formulation of a partial differential equation](variational-formulation-of-a-partial-differential-equation.md), which is not immediately obvious to beginners? The introduction [https://doc.freefem.org/tutorials/poisson.html](https://doc.freefem.org/tutorials/poisson.html) gives an ultra quick example, but your are mostly on your own with that.

On Ubuntu 20.04, the `freefem` is a bit out-of-date (3.5.8, there isn't even a tag for that in the [GitHub](github.md) repo, and refs/tags/release\_3\_10 is from 2010!) and fails to run the examples from the website. It did work with the example package though, but the output does not have color, which makes me sad :-)
```
sudo apt install freefem freefem-examples
freefem /usr/share/doc/freefem-examples/heat.pde
```

So let's just compile the latest v4.6 it from source, on Ubuntu 20.04:
```
sudo apt build-dep freefem
git clone https://github.com/FreeFem/FreeFem-sources
cd FreeFem-sources
# Post v4.6 with some fixes.
git checkout 3df0e2370d9752801ac744b11307b14e16743a44

# Won't apply automatically due to tab hell.
# https://superuser.com/questions/607410/how-to-copy-paste-tab-characters-via-the-clipboard-into-terminal-session-on-gnom
git apply <<'EOS'
diff --git a/3rdparty/ff-petsc/Makefile b/3rdparty/ff-petsc/Makefile
index dc62ab06..13cd3253 100644
--- a/3rdparty/ff-petsc/Makefile
+++ b/3rdparty/ff-petsc/Makefile
@@ -204,7 +204,7 @@ $(SRCDIR)/tag-make-real:$(SRCDIR)/tag-conf-real
 $(SRCDIR)/tag-install-real :$(SRCDIR)/tag-make-real
     cd $(SRCDIR) && $(MAKE) PETSC_DIR=$(PETSC_DIR) PETSC_ARCH=fr install
     -test -x "`type -p otool`" && make changer
-    cd $(SRCDIR) && $(MAKE) PETSC_DIR=$(PETSC_DIR) PETSC_ARCH=fr check
+    #cd $(SRCDIR) && $(MAKE) PETSC_DIR=$(PETSC_DIR) PETSC_ARCH=fr check
     test -e $(DIR_INSTALL_REAL)/include/petsc.h
     test -e $(DIR_INSTALL_REAL)/lib/petsc/conf/petscvariables
     touch $@
@@ -293,7 +293,6 @@ $(SRCDIR)/tag-tar:$(PACKAGE)
     -tar xzf $(PACKAGE)
     patch -p1 < petsc-hpddm.patch
 ifeq ($(WIN32DLLTARGET),)
-    patch -p1 < petsc-metis.patch
 endif
     touch $@
 $(PACKAGE):
EOS

autoreconf -i
./configure --enable-download --enable-optim --prefix="$(pwd)/../FreeFem-install"
./3rdparty/getall -a
cd 3rdparty/ff-petsc
make petsc-slepc
cd -
./reconfigure
make -j`nproc`
make install
cd ../FreeFem-install
PATH="${PATH}:$(pwd)/bin" ./bin/FreeFem++ ../FreeFem-sources/examples/tutorial/
```

Ciro's initial build experience was a bit painful, possibly because it was done on a relatively new Ubuntu 20.04 as of June 2020, but in the end it worked: [https://github.com/FreeFem/FreeFem-sources/issues/141](https://github.com/FreeFem/FreeFem-sources/issues/141)

The main/only dependency appears to be [PETSc](https://en.wikipedia.org/wiki/Portable,_Extensible_Toolkit_for_Scientific_Computation) which is used by default, which is a good sign, as that library appears to automatically parallelize a single input to several backends (single [CPU](central-processing-unit.md), MPI, GPU) so you know things will scale up as you reach simulations.

The problem is that it compiling such a complex dependency opens up much more room for hard to solve compilation errors, and takes a lot more time.

**Table of contents**

- [FreeFem examples](freefem-examples.md)
  - [heat-dirichlet.1d.freefem](heat-dirichlet-1d-freefem.md)
  - [heat-dirichlet-2d-freefem](heat-dirichlet-2d-freefem.md)

## ↑ Ancestors (7)

1. [Partial differential equation solver](partial-differential-equation-solver.md)
2. [Partial differential equation](partial-differential-equation.md)
3. [Differential equation](differential-equation.md)
4. [Calculus](calculus-split.md)
5. [Area of mathematics](area-of-mathematics.md)
6. [Mathematics](mathematics-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (6)

- [Ciro Santilli's Open Source Enlightenment](ciro-santilli-s-open-source-enlightenment.md)
- [Dirichlet boundary condition](dirichlet-boundary-condition.md)
- [FEniCS Project](fenics-project.md)
- [Heat equation](heat-equation.md)
- [Robin boundary condition](robin-boundary-condition.md)
- [Variational formulation of a partial differential equation](variational-formulation-of-a-partial-differential-equation.md)
