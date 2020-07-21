# SI Open Access AWS Example

### Using SI Open Access Data on AWS to semantically cluster and search against American Art paintings

The demo notebook has the following components:
* Using Dask to parse and filter collections metadata on AWS
* Download image files from S3
* Producing image feature vectors with TensorFlow
* Clustering images with UMAP
* Searching for semantically similar paintings using Annoy
* Next Steps

![SAAM UMAP](saam_umap.png)

## Running the Demo

### Running on Binder

This repository has been set up to run on mybinder.org ([About mybinder.org](https://mybinder.readthedocs.io/en/latest/about.html#about)), which provides a pre-configured Python environment with all required packages installed. The only downside is that mybinder.org does not provide very much compute power, and it will shut down after a short period of inactivity. Just click on the badge below, and a free container will be created for you:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/sidatasciencelab/siopenaccess/master?urlpath=lab)

### Running on your local computer

If you have Anaconda or miniconda installed on your computer, it is fairly straightforward to install all of the required packages into a conda environment.

Download this repository to your computer (use the Download Zip option above if you do not have git installed):

```
(base)$ git clone https://github.com/sidatasciencelab/siopenaccess.git

Cloning into 'siopenaccess'...
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 852 (delta 0), reused 2 (delta 0), pack-reused 848
Receiving objects: 100% (852/852), 77.21 MiB | 11.06 MiB/s, done.
Resolving deltas: 100% (12/12), done.
```

```
(base)$ cd siopenaccess
```

Use the environment.yml file in this repository to install the exact Python package requirements you will need:

```
(base)$ conda env create -f binder/environment.yml

Collecting package metadata (repodata.json): done
Solving environment: done
Downloading and Extracting Packages

s3transfer-0.3.3     | 91 KB     | #################### | 100%
zeromq-4.3.2         | 8.8 MB    | #################### | 100%
bokeh-2.1.1          | 7.0 MB    | #################### | 100%
…
#
# To activate this environment, use
#
#     $ conda activate siopenaccess
#
# To deactivate an active environment, use
#
#     $ conda deactivate
```

Now that the environment has been created and all packages installed, activate it:

```
(base)$ conda activate siopenaccess
```

Finally, launch the Jupyter Lab interface so that you can interact directly with "SI Open Access SAAM S3 Example.ipynb". We are using the Jupyter Lab interface for this demo because of its integrations with Dask monitoring plugins, but you can also run the notebook using "jupyter notebook"

```
(siopenaccess)$ jupyter lab
```

This command will open an instance of Jupyter Lab in your browser.
