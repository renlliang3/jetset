[![Build Status](https://travis-ci.org/andreatramacere/jetset.svg?branch=py23)](https://travis-ci.org/andreatramacere/jetset)

![img](./logo/logo_large.png)


JetSeT is  an open source  C/Python   framework  to reproduce radiative and accelerative processes acting in relativistic jets,  
allowing to fit the numerical models to observed data. The main features of this framework are: 

 * handling observed data: re-binning, definition of data sets, bindings to astropy tables and quantities
   definition of complex numerical radiative scenarios: Synchrotron Self-Compton (SSC), external Compton (EC) and EC 
   against the CMB 
 
 * Constraining of the model in the pre-fitting stage, based on accurate  and already published phenomenological trends. 
   In particular, starting from phenomenological parameters, such as spectral indices, peak fluxes and frequencies, and 
   spectral  curvatures, that the code evaluates automatically, the pre-fitting algorithm is able to provide a good 
   starting model,following the phenomenological trends that I have implemented. fitting of multiwavelength SEDs using  
   both frequentist approach (iminuit) and bayesian MCMC sampling (emcee)
 
 * Self-consistent temporal evolution of the plasma under the effect of radiative and accelerative processes, both first  
   order and second order (stochastic acceleration) processes.



# Acknowledgements

If you use this code in any kind of scientific publication please cite the following papers:

* `Tramacere A. et al. 2011` http://adsabs.harvard.edu/abs/2011ApJ...739...66T
* `Tramacere A. et al. 2009` http://adsabs.harvard.edu/abs/2009A%26A...501..879T
* `Massaro E. et. al 2006`   http://adsabs.harvard.edu/abs/2006A%26A...448..861M

# Documentation
visit: https://jetset.readthedocs.io/en/latest/



# Install  JetSeT from Anaconda  (suggested for OSX and Linux)
 - I suggest to use anaconda and python3 (https://www.anaconda.com/download/)
 
 - create a virtual environment (not necessary, but suggested): 
 
    `conda create --name jetset python=3.7 ipython jupyter`
    
     `conda activate jetset`
     
- install the code:
  
  `conda install -c andreatramacere jetset`
  
if conda fails with dependencies you can try
  
   - `conda install -c andreatramacere -c astropy jetset`
    
     OR

   - `conda install -c andreatramacere -c conda-forge jetset`
# Install the JetSeT from source 


## Download the code
   - Get the source code from: 

     - https://github.com/andreatramacere/jetset/archive/stable.tar.gz

   - Uncompress the  archive  `jetset-stable.tar.gz`
   
   - cd to  the dir `jetset-stable` 

## Installation from source using Anaconda 
 
 - Install requirements, run on the command line:
    - `conda install --file requirements.txt`
     
     if conda fails with dependencies you can try
  
   - `conda install -c astropy  --file requirements.txt`
    
     OR

   - `conda install -c conda-forge  --file requirements.txt` 
   
    if anaconda fails to install swig, you can try one of the following alternative [methods](swig.md)
   
 - run on the command line: 
     * `python setup.py clean`
     * `python setup.py install`


**run all the examples outside of the installation dir**


## Installation from source using PIP 
 
 - Install requirements, run on the command line: `pip install -r requirements.txt `
    
   if pip fails to install swig, you can try one of the following alternative [methods](swig.md)
  
  - run on the command line: 
    * `python setup.py clean`
    * `python setup.py install`

**run all the examples outside of the installation dir**


##  Requirements
The following python packages are required:

        python >=3.6 (python >=3.6 is suggested, older python 3 versions should  work, python 2 is not supported any more from version>=1.1.0)
        setuptools
        scipy
        numpy
        astropy
        matplotlib
        swig
        future
        iminuit
        corner
        six
        emcee
        pyyaml
         


A C compiler is also necessary, plus the SWIG wrapper generator.

All the dependencies are be installed following the Anaconda method 
 **OR** the pip method, as described above.

# jetset code repoistory

The code is hosted here: 
 -  https://github.com/andreatramacere/jetset
 




# Build documentation

 requires: 
    
 - sphinx
 - pylint
 - sphinx-pyreverse: "https://github.com/alendit/sphinx-pyreverse"
 - nbsphinx: "conda install -c conda-forge nbsphinx"
 - sphinx_rtd_theme: conda install -c anaconda sphinx_rtd_theme 
 - sphinx-bootstrap-theme: 'https://github.com/ryan-roemer/sphinx-bootstrap-theme'
 - sphinx automod: 'https://github.com/astropy/sphinx-automodapi'    
 
 
 


