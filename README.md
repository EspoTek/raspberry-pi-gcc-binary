# GCC 7.2 binary for Raspberry Pi #

I've compiled *GCC 7.2.0* for Raspberry Pi, enabled languages C, C++ and Fortran. The compilers should work with all current versions of Pi.
You can read more about how I compiled *GCC* at []() and you can repeat the process yourself if you wish to recreate the binary on your Pi.

How to use:
===========

* Extract the archive, it is a .tar.bz2 file:
```
#!console

tar xf gcc-7.2.0.tar.bz2
```

* Copy/move gcc-7.2.0 to /usr/local/gcc-7.2.0
* Extract the archive, it is a .tar.bz2 file:
```
#!console

sudo mv gcc-7.2.0 /usr/local
```

* Add the above to your path:
```
#!console

export PATH=/usr/local/gcc-7.2.0/bin:$PATH
```

* Now, you should be able to use the compilers: *gcc-7.2.0* for C, *g++-7.2.0* for C++ and *gfortan-7.2.0 for Fortran*.
* If you want to permanently add the compilers to your path, append the *export* line to the end of your .bashrc file:
```
#!console

echo 'export PATH=/usr/local/gcc-7.2.0/bin:$PATH' >> .bashrc
source .bashrc
```
