# COMET run fixer

Script to register and merge two OME-TIFF files derived from interrupted COMET runs.  
The registration is performed with palom: https://github.com/labsyspharm/palom

## Usage

From the command line:
```
python3 comet_fixer.py image1 image2 output_image
```

### Setup

Best used from a mamba environment.

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
Take as input a folder with an arbitrary number of images from the same run, instead of 2 files.
