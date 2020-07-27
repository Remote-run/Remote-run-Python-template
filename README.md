# Remote-run-Python-template

The template for running Python applications in the on the Remote run system. 



## Requirements

When submitting a Python request the current context of the executable will be packaged and sent to the server. When on the server the requirements.txt will be installed and the runfile (set in the config) wil be run with the run params (also set in the config). Because of the "why bother" approach python has to versioning and compatibility a general solution wold be impractical, thats why you can set the docker image to run from. the default image is ```nvidia/cuda:10.1-runtime``` . You can put stuff in the requierments.txt to be installed on top of this but to avoid having to wait for installation a image with the packages preinstalled cold be used e.g. tensorflow-gpu.

To run successfully you need to:

1. have a requierments.txt in the executable context with ALL dependencies. That is, no local dependencies, if any are needed they have to be in the local context
2. Everything you want returned after the run is complete has to be saved to the the ./save_data dir
3. Python 3 is used

## Usage

Execute the executable called Remote-run and follow the instructions  on screen. If all the requirements above are met you can run whatever  you want.