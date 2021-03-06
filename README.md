# ISL
**GNU ISL library for building GCC with Graphite loop optimizations**

This is an unofficial verbatim redistribution of the binary&source form of the GNU ISL library (a prerequisite for compiling programs like GCC), under the terms of MIT license.

This redistribution is under the the same MIT license.

Please visit the official website for more details: https://gcc.gnu.org/install/prerequisites.html

## Usage
The binary/ folder contains both a tar.gz file and a folder, which are equivalent. You can use either one.

## Compilation notes
### Compilation environment
* CentOS 6.6
* x86_64 architecture
* Compiler: gcc version 4.4.7 20120313 (Red Hat 4.4.7-11)

### Compilation steps
#### Version: 0.11.1
**(with GMP-4.3.2)**
```bash
wget ftp://gcc.gnu.org/pub/gcc/infrastructure/isl-0.11.1.tar.bz2
tar xvf isl-0.11.1.tar.bz2
mkdir build_isl-0.11.1
cd build_isl-0.11.1
../isl-0.11.1/configure --prefix=/home/steven/install/isl/0.11.1 -with-gmp=system --with-gmp-prefix=/home/steven/install/libgmp/4.3.2 --with-gmp-exec-prefix=/home/steven/install/libgmp/4.3.2 --enable-portable-binary=yes --enable-shared=yes --enable-static=yes
make -j10
make check | tee QualityVerification.txt
make install
```
#### Version: 0.12.2
**(with GMP-4.3.2)**
```bash
wget ftp://gcc.gnu.org/pub/gcc/infrastructure/isl-0.12.2.tar.bz2
tar xvf isl-0.12.2.tar.bz2
mkdir build_isl-0.12.2
cd build_isl-0.12.2
../isl-0.12.2/configure --prefix=/home/steven/install/isl/0.12.2 -with-gmp=system --with-gmp-prefix=/home/steven/install/libgmp/4.3.2 --with-gmp-exec-prefix=/home/steven/install/libgmp/4.3.2 --enable-portable-binary=yes --enable-shared=yes --enable-static=yes
make -j10
make check | tee QualityVerification.txt
make install
```
### Quality verification
See the "QualityVerification.txt" for the output of "make check".
