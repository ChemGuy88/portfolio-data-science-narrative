# Best Practice for Data Science

## Set environment variables
Set environment variables in `%CONDA_PREFIX%/etc/conda`. See the [docs](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)

## Set IPython configuration for each Anaconda Virtual Environment
Create `ipython_configuration.py` in `%CONDA_PREFIX%/etc/ipython`. See [docs](https://ipython.readthedocs.io/en/stable/config/intro.html#systemwide-configuration)
Then change the `IPYTHONDIR` environment variable via Anaconda.

## Example (Windows)

Your Anaconda `env_vars.bat` file will look like this:

```bash
set SECRET_VARIABLE_1=secretValue1
set SECRET_VARIABLE_2=secretValue2
set SECRET_PATH=\\networkFolder\userName\folder1
set IPYTHONDIR=%CONDA_PREFIX%\etc\ipython
pushd \\networkFolder\userName\folder1 #&@REM This is only necessary if your projectDirectory is a networkFolder
cd \\networkFolder\userName\folder1
```