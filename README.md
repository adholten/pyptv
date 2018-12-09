# PyPTV
Python GUI for the OpenPTV library `liboptv`


[![Build Status](https://travis-ci.org/alexlib/pyptv.svg?branch=master)](https://travis-ci.org/alexlib/pyptv) [![DOI](https://zenodo.org/badge/121291437.svg)](https://zenodo.org/badge/latestdoi/121291437)




**PyPTV** or otherwise called **OpenPTV-Python** is the Python GUI for [OpenPTV](http://www.openptv.net). It is based on `traits`, `traitsui`, `chaco`, `enable` and `pyface` from Enthought Inc. and provides an UI *interface* the OpenPTV library that includes all the core algorithms (correspondence, tracking, calibration, etc.) written in ANSI C and has Python bindings using Cython.  

Both PyPTV and the OpenPTV library are in the development phase and continuously refactored. Please follow the development on the community mailing list:

	openptv@googlegroups.com


## Documentation, including installation instructions of liboptv

<http://openptv-python.readthedocs.io>


## Installing this package, pyptv, including liboptv and using Anaconda:

        git clone --recursive --single-branch -b test_add_3cam https://github.com/alexlib/pyptv.git
        cd pyptv
        conda create -n pyptv --file requirements.txt

### Activate your package, enter the `liboptv` bindings and add the `optv` to the packages:

		conda activate pyptv
		cd ~/openptv/py_bind
		python setup.py install
	
* If Cython is missing, add it using:

		conda install cython -n pyptv
		python setup.py install


## Getting started:

If the compilation passed, open the terminal and run:  

		python pyptv_gui/pyptv_gui.py ../test_cavity
		
or:  

		pythonw pyptv_gui/pyptv_gui.py ../test_cavity
		
It is possible to install wxPython instead of PyQt4, and switch between those:  

		ETS_TOOLKIT=qt4 python pyptv_gui/pyptv_gui.py ../test_cavity

Follow the instructions in our **screencasts and tutorials**:
  
  *  Tutorial 1: <http://youtu.be/S2fY5WFsFwo>  
  
  *  Tutorial 2: <http://www.youtube.com/watch?v=_JxFxwVDSt0>   
  
  *  Tutorial 3: <http://www.youtube.com/watch?v=z1eqFL5JIJc>  
  
  
Ask for help on our mailing list:

	openptv@googlegroups.com



