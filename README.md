SQuIDS
===========

![SQuIDS Logo](/resources/squids_logo_small.png)

Prerequisites
-------------

The following packages are required to build and use the library, and
can probably be obtained from your favorite package manager:

* gsl (>= 1.15): http://www.gnu.org/software/gsl/
* C++ compiler with C++11 support.

Supported Platforms and Compilers
---------------------------------

This software is designed to work in POSIX environments with
standard conformant C++ compilers. It should be noted that various 
C++11 features are used for efficient calculation, so a reasonably 
modern compiler is necessary. See the list below for compilers
known to compile the software successfully. 

* GCC: Version 4.8.1 or later is known to work.
* Clang: Version 3.3 or later is known to work. 
* ICC: Version 15.0 is known to work; version 14.0 should work 
       as well but has not been tested. 

It is also necessary to have a sufficiently new standard library
implementation. The libstdc++ supplied with gcc 4.8 or newer, and
libc++ are known to work. 

The software has been tested and found to work on the following
operating systems:

* Linux
* Darwin (Mac OS X)
* FreeBSD

Configuration
-------------

A configure script, config.sh, is provided in the root directory.

The path for the GSL libraries can be specified running:

	./config.sh --with-gsl-incdir=DIR --with-gsl-libdir=DIR

if not specified pkg-config will be used to try to find
the your GSL installation. After successful configuration run:

	make

To verify that the software is functioning correctly, the 
unit tests can be run with the command:

	make test

Finally, the software can be installed using the command:

	make install

By default this will attempt to install the library within /usr/local; 
this can be changed by using the --prefix option when running config.sh:

	./config --prefix=$HOME

will select to install the software in the current user's home directory, 
for example. 

Examples
--------

Three examples programs can be found in the examples subdirectory.

In order to plot the example results you will need:

* gnuplot (>4.0): http://www.gnuplot.info/

Documentation
-------------

Documentation can be generated by running:

	make docs

and will be put in the docs subdirectory.

Citation
--------

If you want cite this work, or want to look at further description
please refer to

*A Simple Quantum Integro-Differential Solver (SQuIDS)*

Carlos A. Arguelles Delgado, Jordi Salvado, Christopher N. Weaver

arXiv:1412.3832 (https://inspirehep.net/record/1334148)

