## Compiling GADGET-2 for GLASS ICs


```bash
# in fftw-2.1.5/
./configure --enable-type-prefix --enable-float --enable-mpi --prefix ~/glass-test/fftw_prefix/include/
make
make install
./configure --enable-type-prefix --enable-mpi --prefix ~/glass-test/fftw_prefix/include/ 
make
make install
```

#### See also

- https://wwwmpa.mpa-garching.mpg.de/gadget/gadget-list/0432.html
- https://wwwmpa.mpa-garching.mpg.de/gadget/gadget-list/0171.html
