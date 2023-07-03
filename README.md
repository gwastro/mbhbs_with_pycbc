# mbhbs_with_pycbc
PyCBC-based search and inference of MBHBs in LDC Sangria

## Setup

To begin, we need to setup our virtual enviroment and install all the
required packages to run our code. We used conda enviroments throughout
our development with the command:

`conda create -n {env_name_here} -c conda-forge gcc_linux-64 gxx_linux-64 gsl lapack=3.6.1 numpy scipy Cython jupyter ipython matplotlib python=3.9`

The packages that you will need to install into this enviroment are:

- [BBHx](https://github.com/mikekatz04/BBHx):

```
git clone https://github.com/mikekatz04/BBHx.git
cd BBHx
python setup.py install
```

- [PyCBC](https://github.com/gwastro/pycbc):

```
git clone https://github.com/gwastro/pycbc.git
cd pycbc
pip install -r requirements.txt
pip install -r companion.txt
pip install .
```

- [BBHX-waveform-model](https://github.com/gwastro/BBHX-waveform-model):

```
git clone https://github.com/gwastro/BBHX-waveform-model.git
cd BBHX-waveform-model
pip install .
```

All links direct you to the respective github pages.


## Dataset downloads (in progress)

# Data and PSD generation

To begin we will generate the data for the type of analysis we would like to investigate. In the *signal_generation* directory we have subdirectories for the different noise types:

* zero_noise
* no_gbs
* with_gbs
* sangria

Each directory (with the exception of *sangria*) has subdirectories for single injections or multiple (named single and multi respectively). Running the script found in these subdirectories will generate the signal injections in the type of noise specified. The *sangria* directory simply converts the Sangria data into a PyCBC format for search and inference.

After the data has been generated, we can now estimate the PSDs by navigating to the *psds* directory. Again, you will find the same directories as in the *signal_generation* directory. Run the script in the desired folder to produce the PSDs for that data.

# Search and Inference
## Search (in progress)

## Inference (in progress)

