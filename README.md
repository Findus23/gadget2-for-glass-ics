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

#### Sources:

- https://web.archive.org/web/20200202183309/https://wwwmpa.mpa-garching.mpg.de/galform/gadget/gadget2.tar.gz
- https://web.archive.org/web/20250116173001/https://www.fftw.org/fftw-2.1.5.tar.gz

Compare hashes with `sha256sum -c hashes.txt`

#### See also

- https://wwwmpa.mpa-garching.mpg.de/gadget/gadget-list/0432.html
- https://wwwmpa.mpa-garching.mpg.de/gadget/gadget-list/0171.html
