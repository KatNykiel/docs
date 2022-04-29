# Hydrogen

**Hydrogen** is an Atom package which lets you run Jupyter-like Python files within your Atom editor. This gives you the benefits of instantaneous code feedback, without being restricted by clunky Jupyter Notebooks.

Installation is similar to the previous steps - search for 'Hydrogen' (by nteract) and install.

## Running local Python files
To run Hydrogen kernels locally, you'll need to install [Python](https://www.python.org/downloads/). After installing Python, install the ipykernel package locally

    pip install ipykernel
    python -m ipykernel install

Let's start by testing out Hydrogen using a simple python file. In your Gilbreth directory, create a new file called **hydrogen.py**

```{attention} If you edit a file in your remote directory, you'll be editing a local copy that updates the remote copy when you save. Therefore, when running local Hydrogen kernels, you won't have access to the cluster's environment or file system.
```

Hydrogen uses Python (.py) files to simulate Jupyter Notebooks. Similarly, it has markdown and code cells, which can be separated in the following way

    # %% markdown

    This is the content of the Markdown cell. $$H|\psi\rangle = E|\psi\rangle$$

    # %% codecell

    fish = 2+2
    print("Wow Kat, thank you for writing this tutorial!")

Try copying the above cells into your **hydrogen.py** file, and typing ```ALT-SHIFT-ENTER```. This should run the cell your cursor is in, then move down to the next cell

This system takes a little getting used to, but it's essentially equivalent to cells in Jupyter notebooks

## Running remote Python files

Running files locally is cool, but it's often desired to run Python files directly in the cluster.

1. Connect to a cluster using ssh port forwarding (this should be done from the previous step)

```python
ssh -L[[1234]]:localhost:[[1234]] [[YOUR USERNAME]]@gilbreth.rcac.purdue.edu
```

2. Setup config file in the cluster (you can do this using the platformio-ide-terminal)

```python
pip install jupyter
jupyter notebook --generate-config
```

```{attention} By default, the RCAC clusters use Python v2.7.5. Yuck, but it's as simple as typing **module load anaconda** to use a newer version. If you add 'module load anaconda' to a file named '.bashrc' in your home directory, it will automatically load anaconda every time you connect
```

3. In config file (~/.jupyter/jupyter_notebook_config.py), uncomment

```
    #c.NotebookApp.token = ''
```
and set the string to some arbitrary phrase (i.e. 'katnyp')

4. Run a Jupyter server using

```python
jupyter notebook --port=[[1234]] --no-browser
```

You should now see a Jupyter Notebook server running in the terminal!

```{note} If you're using multiple terminals, this will only work on the first connection you make. This shell will now be 'unusable', but you can just open a new terminal and use that
```

5. If you just want to use your local Jupyter in-browser in the cluster environment, copy the output of the previous command into a browser

```python
# it should look something like this
http://127.0.0.1:[[1234]]/?token=...
```

This is Jupyter notebook server connected to the RCAC clusters. Cool! But we want more, we want it *within Atom*

6. From Hydrogen package settings, set 'Kernel Gateways' to the following

```python
[{
  "name": "Gilbreth",
  "options": {
    "baseUrl": "http://localhost:[[1234]]",
    "token": "[[your chosen token]]"
  }
}]
```

7. To connect, we there's a few steps we need to take.

```{note} Instead of using the Menu bar, we'll introduce the **command palette**. It's a convenient way to access commands within Atom without using the mouse or scrolling through menus.

```

To connect to a remote kernel, open the command palette using ```CTRL-SHIFT-P```
- type 're k' to select 'Hydrogen: Connect to Remote Kernel'
- select Gilbreth
- choose 'Authenticate with a token'
- type in your chosen token
- choose [new session] (or connect to an existing one)
- choose your desired Python kernel

Congrats, you're now connected to the clusters! As a check, try adding the following code cell to your Python file

```python
# %% codecell
import os
os.getcwd()
```

You should see that you're in the cluster!
