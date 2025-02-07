## Compiling GADGET-2 for GLASS ICs

> How to compile GADGET-2 on a modern system to generate GLASS IC files

### FFTW:

```bash
# in fftw-2.1.5/
./configure --enable-type-prefix --enable-float --enable-mpi --prefix ~/glass-test/fftw_prefix/
make
make install
./configure --enable-type-prefix --enable-mpi --prefix ~/glass-test/fftw_prefix/ 
make
make install
```

### Gadget:

```bash
# in Gadget-2.0.7/Gadget2/
nano Makefile # replace /home/lukas/glass-test/ with own path to base folder
make
```



### Sources:

- https://web.archive.org/web/20200202183309/https://wwwmpa.mpa-garching.mpg.de/galform/gadget/gadget2.tar.gz
- https://web.archive.org/web/20250116173001/https://www.fftw.org/fftw-2.1.5.tar.gz

Compare hashes with `sha256sum -c hashes.txt`

### Additional fixes:

In case of `fftw.texi:49: misplaced` or related:

```diff
diff --git a/Makefile b/Makefile
index 61739f9..dac706f 100644
--- a/Makefile
+++ b/Makefile
@@ -143,7 +143,7 @@ sbindir = ${exec_prefix}/sbin
 sharedstatedir = ${prefix}/com
 sysconfdir = ${prefix}/etc
 target_alias = 
-SUBDIRS = fftw rfftw tests doc threads mpi
+SUBDIRS = fftw rfftw tests threads mpi
 EXTRA_DIST = README.hacks bootstrap.sh COPYRIGHT acx_pthread.m4 acx_mpi.m4
 
 extradist = fortran gensrc matlab cilk FAQ
```

### See also

- https://wwwmpa.mpa-garching.mpg.de/gadget/gadget-list/0432.html
- https://wwwmpa.mpa-garching.mpg.de/gadget/gadget-list/0171.html
