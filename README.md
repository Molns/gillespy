#GillesPy

GillesPy is a modeling toolkit for stochastic simulations for Linux and OSX. It provides a python interface to the StochKit stochastic simulation solvers. It contains a simple python interface for model construction, editing, and simulating models stochastically and deterministically.

GillesPy is part of the StochSS project, see http://www.stochss.org for more details.

## Dependencies

GillesPy requires numpy, scipy, and matplotlib for proper functionality. Installation details for these packages can be found at http://scipy.org. 

GillesPy does not install the StochKit or StochKitODE solvers, but requires them for stochastic simulation. Either StochKit  **OR** StochSS must be installed to provide these solvers.

Installation instructions for StochKit: http://sourceforge.net/projects/stochkit/

**OR**

Installation instructions for StochSS:  http://iguana.cs.ucsb.edu/wordpress/?page_id=224


##Installation

Installation instructions are provided for Linux Ubuntu and OSX.

##### Ubuntu

If StochSS or StochKit is installed, GillesPy must be pointed to the solver locations. This is done during the installation, through setting a SUDO environment variable depending on whether you have StochSS or StochKit.

For StochSS, set the variable STOCHSS_HOME while in the SUDO environment. On a linux Ubuntu system, with StochSS 1.6 installed in your home directory:
```
  git clone https://github.com/GillesPy/gillespy.git
  cd gillespy
  sudo STOCHSS_HOME=$HOME/stochss.linux.1.6/ python setup.py install
```

Note: simply using export STOCHSS_HOME will not provide a SUDO environment variable.

If StochKit is installed, this process is similar, but instead set the environment variable STOCHKIT_HOME:
```
  git clone https://github.com/GillesPy/gillespy.git
  cd gillespy
  sudo STOCHKIT_HOME=$HOME/StochKit2.0.10/ python setup.py install
```

As of this time, if only StochKit is installed, the StochKitODE solver is inaccessible.
```
  TODO: Provide a way to install StochKitODE.
```


##### OSX
If StochSS or StochKit is installed, GillesPy must be pointed to the solver locations. This is done during the installation, through setting a SUDO environment variable depending on whether you have StochSS or StochKit.

For StochSS, set the variable STOCHSS_HOME while in the SUDO environment. On OSX, if you have StochSS 1.6 installed in your Applications directory, then you would:
```
  git clone https://github.com/GillesPy/gillespy.git
  cd gillespy
  sudo STOCHSS_HOME=/Applications/StochSS-1.6/StochSSserver.app/Contents/Resources/ python setup.py install
```

##### OSX (without StochSS)

If you do not have StochSS installed, you will need to download StochKit (http://sourceforge.net/projects/stochkit/) and the StochKit-ODE package from StochSS.
Then set the environement variables STOCHKIT_HOME and STOCHKIT_ODE_HOME before you run the setup.py script as above.

Note: simply using export STOCHSS_HOME will not provide a SUDO environment variable.

If StochKit is installed, this process is similar, but instead set the environment variable STOCHKIT_HOME:
```
  git clone https://github.com/GillesPy/gillespy.git
  cd gillespy
  sudo STOCHKIT_HOME=/Applications/StochKit2.0.10/ python setup.py install
```

As of this time, if only StochKit is installed, the StochKitODE solver is inaccessible.
```
  TODO: Provide a way to install StochKitODE.
```

