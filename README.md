# jupyterlab-logevent
start jupyterlab extension bu following these steps.

conda create -n jupyterlab-log --override-channels --strict-channel-priority -c conda-forge -c nodefaults jupyterlab=3 cookiecutter nodejs jupyter-packaging git

conda activate jupyterlab-log
#Note: You’ll need to run the command above in each new terminal you open before you can work with the tools you installed in the jupyterlab-ext environment.

#git clone repository
#Initialize the project from a cookiecutter
cookiecutter https://github.com/jupyterlab/extension-cookiecutter-ts
cd jupyterlab_log
ls

#commit
git init
git add .
git commit -m 'Seed apod project from cookiecutter'


#Build and install the extension for development
pip install -ve .
jupyter labextension develop --overwrite .

#ready to go
conda activate jupyterlab-log
jupyter lab
