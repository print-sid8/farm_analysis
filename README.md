# farm_analysis

##  Farm analysis - NDVI and NDMI

This repo has a notebook that will perform NDVI and NDMI analysis on given AOIs, on a monthly basis and create PNG outputs that are then visualized on a Folium basemap. It uses [Element84 API](https://www.element84.com/earth-search/) to acquire Sentinel-2 L2A images from AWS Open Data S3 buckets, in your area of interest and time range.


### Setting up the Environment

This script was developed using Python > = 3.6, in Ubuntu 20.04.


Note : osgeo gdal must be setup, and the script `gdalinstall.sh` helps installing gdal in a Debian OS such as Ubuntu.
It is run as below -

```bash
bash gdalinstall.sh
```

Note : The environment setup requires Dask, Xarray, and few other libraries for Multiprocessing, hence "Coiled" must be setup using miniconda/conda. Miniconda reduces dependencies. 

It is run as below -

```bash
conda install -c conda-forge coiled
```

To create a new conda env -

```bash
coiled install gjoseph92/stackstac
```

Activate conda environment -

```bash
conda activate coiled-gjoseph92-stackstac
```

And install additional packages in the `requirements.txt` file using :

```bash
pip install requirements.txt
```

--------------------

Once the software environment is setup, the Jupyter Notebook should work, and the explanation and comments are within the Notebook.

Simply calling "jupyter-notebook" from within the conda env and this github repo folder in your local, should run all the code properly.