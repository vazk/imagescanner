# Getting started #

**ATTENTION:** _You **MUST** have the drivers of your scanner device installed and working before getting started._

## Requirements ##

**Python:**
  * Check REQUIREMENTS in the setup.py file.
_If you install using setup.py install the python requirements will be install
ed automagically for you._

**On Linux:**
  * libsane >= 1.0
  * pysane >= 2.0

**On Windows:**
  * None (so far)

## Installation ##

There are a few ways that you can use to install ImageScanner:

  1. From Python Package Index
```
 pip install imagescanner
```
  1. From the source code:
```
 cd imagescanner
 python setup.py install
```

## Scanning a file ##

  * Getting access to a scanner device:
```
 from imagescanner import ImageScanner

 # instantiate the imagescanner obj 
 iscanner = ImageScanner()
 
 # get all available devices
 scanners = iscanner.list_scanners()

 # choose one of the devices
 scanner = scanners[0]

 # scan your file (returns a PIL object)
 scanner.scan()
```