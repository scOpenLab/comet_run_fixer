# COMET run fixer

Jupyter notebook to register and merge two OME-TIFF files derived from interrupted COMET runs.  
The registration is performed with palom: https://github.com/labsyspharm/palom

## Usage
The script is for now run as a Jupyter Notebook.

### Setup

Requirements:
```
palom
dask
tifffile
ome_types
unidecode
```

### Input

Paths to two OME-TIFF files derived from the same interrupted COMET run.


### Output

An OME-TIFF file with all the channels from the two files registered, and the run metadata from the first file.
The channel and cycle metadata from the second file are added to the ones from the first and written to the output.
The output OME-TIFF file can be read with the COMET Horizon VIewer.

## TO-DO
Convert to a python script able to handle a folder with multiple files from a single run.
