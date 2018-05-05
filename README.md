# GCC 8.1 binary for Raspberry Pi #

I've compiled *GCC 8.1.0* for Raspberry Pi, enabled languages C and C++. The compilers should work with all current versions of Pi.
You can read more about how I compiled *GCC* at [https://solarianprogrammer.com/2017/12/07/raspberry-pi-raspbian-compiling-gcc/](https://solarianprogrammer.com/2017/12/07/raspberry-pi-raspbian-compiling-gcc/) and you can repeat the process yourself if you wish to recreate the binary on your Pi.

How to use:
===========

* Extract the archive, it is a .tar.bz2 file:
```
#!console

tar xf gcc-8.1.0.tar.bz2
```

* Copy/move gcc-8.1.0 to /usr/local/gcc-8.1.0:
```
#!console

sudo mv gcc-8.1.0 /usr/local
```

* Add the above to your path:
```
#!console

export PATH=/usr/local/gcc-8.1.0/bin:$PATH
```

* Now, you should be able to use the compilers: *gcc-8.1.0* for C and *g++-8.1.0* for C++.

* If you want to permanently add the compilers to your path, append the *export* line to the end of your .bashrc file:
```
#!console

echo 'export PATH=/usr/local/gcc-8.1.0/bin:$PATH' >> .bashrc
source .bashrc
```

Note:
=====

I kept *GCC 7.2.0* in this repo for people that also need a Fortran compiler. *gcc-7.2.0.tar.bz2* contains *gcc-7.2.0*, *g++-7.2.0*, *gfortran-7.2.0*.
