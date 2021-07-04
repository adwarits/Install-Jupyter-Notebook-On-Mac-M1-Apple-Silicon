# Install-Jupyter-Notebook-On-Mac-M1-Apple-Silicon

I found out that it is extremely hard to install Jupyter Notebook in the new Mac M1 with Apple Silicon.
After did some research online, I decided to share the steps here.
Let's have some fun with Jupyter Notebook.
Special thanks to [Al Buzz Videos](https://www.youtube.com/watch?v=W_Qbrnp6uis)

## 1. Install Miniforge 3

- Download Miniforge 3 for arm64 (Apple Silicon) from https://github.com/conda-forge/miniforge 
- Open terminal (Type Terminal in Launchpad)
- Open downloads folder from your terminal (type “cd Downloads”)
- Type “ls” to look at your file in Downloads folder and find your Miniforge 3 files
- Install Miniforge 3 (type “bash [Miniforge File Name])
- Restart the Terminal

## 2. Install and Activate Conda

- Install Conda by typing “conda create --name python38 python=3.8” (python38 is the new virtual environment folder - we can name it differently)
- After the conda has been installed, activate it by typing “conda activate python38”. At this point the virtual environment has been activated and we are in virtual environment mode.

## 3. Install TensorFlow

- Download TensorFlow from https://github.com/apple/tensorflow_macos/releases (find file tensorflow_macos-0.1alpha3.tar.gz) 
- Open downloads folder from your terminal (type “cd Downloads”)
- Type “ls” to look at your file in Downloads folder and find your TensorFlow files
- Type “tar -xvf tensorflow_macos-0.1alpha3.tar” to extract your downloads
- Open downloads folder again from your terminal (type “cd Downloads”)
- Type “ls” to look at your file in Downloads folder and find the tensorflow_macos
- Type “cd tensorflow_macos”
- Type “ls” to look at your file in tensorflow_macos folder and find the arm64
- Open arm64 by typing “cd arm64”
- Type “pwd” to get the arm64 location
- Define the library by typing “ibs="/Users/adwarits/Downloads/tensorflow_macos/arm64"”
- Open the list of the conda environment in the computer by typing “conda env list”
- Define the environment by typing “env="/Users/adwarits/miniforge3/envs/python38"”
- Type “conda install cached-property”
- Type “conda install six”
- Type below command one by one

pip install --upgrade -t "$env/lib/python3.8/site-packages/" --no-dependencies --force "$libs/grpcio-1.33.2-cp38-cp38-macosx_11_0_arm64.whl"

pip install --upgrade -t "$env/lib/python3.8/site-packages/" --no-dependencies --force "$libs/h5py-2.10.0-cp38-cp38-macosx_11_0_arm64.whl"

pip install --upgrade -t "$env/lib/python3.8/site-packages/" --no-dependencies --force "$libs/numpy-1.18.5-cp38-cp38-macosx_11_0_arm64.whl"

pip install --upgrade -t "$env/lib/python3.8/site-packages/" --no-dependencies --force "$libs/tensorflow_addons-0.11.2+mlcompute-cp38-cp38-macosx_11_0_arm64.whl"

pip install --upgrade -t "$env/lib/python3.8/site-packages/" --no-dependencies --force "$libs/tensorflow_addons_macos-0.1a3-cp38-cp38-macosx_11_0_arm64.whl"

conda install -c conda-forge -y absl-py

conda install -c conda-forge -y astunparse

conda install -c conda-forge -y gast

conda install -c conda-forge -y opt_einsum

conda install -c conda-forge -y termcolor

conda install -c conda-forge -y typing_extensions

conda install -c conda-forge -y wheel

conda install -c conda-forge -y typeguard

conda install -c conda-forge -y typeguard

pip install wrapt flatbuffers tensorflow_estimator google_pasta keras_preprocessing protobuf

pip install --upgrade -t "tf_2_4/lib/python3.8/site-packages/" --no-dependencies --force "$libs/tensorflow_macos-0.1a3-cp38-cp38-macosx_11_0_arm64.whl"

