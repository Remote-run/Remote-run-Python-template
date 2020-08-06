# Remote-run-Python-template

The template for running Python applications in the on the Remote run system. 



## Requirements

When submitting a Python request the current context of the executable will be packaged and sent to the server. When on the server the requirements.txt will be installed and the run-file (set in the config) will be run with the run prams (also set in the config). Because of the "why bother" approach python has to versioning and compatibility, a general solution wold be impractical, thats why you can set the docker image to run from. The default image is ```nvidia/cuda:10.1-runtime``` . You can put stuff in the requirements.txt to be installed on top of this. To avoid having to wait for installation, a image with the packages preinstalled cold be used e.g. ```tensorflow/tensorflow:latest-gpu ```

To run successfully you need to:

1. have a requirements.txt in the executable context with ALL dependencies. That is, no local dependencies, if any are needed they have to be in the local context
2. Everything you want returned after the run is complete has to be saved to the the ./save_data dir
3. Python 3 is used

## Usage

Execute the executable called Remote-run and follow the instructions  on screen. If all the requirements above are met you can run whatever  you want.