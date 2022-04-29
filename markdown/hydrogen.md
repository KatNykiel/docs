# Hydrogen

**Hydrogen** is an Atom package which lets you run Jupyter-like Python files within your Atom editor. This gives you the benefits of instantaneous code feedback, without being restricted by clunky Jupyter Notebooks.

Installation is similar to the previous steps - search for 'Hydrogen' (by nteract) and install.

## Running local Python files
To run Hydrogen kernels locally, you'll need to install [Python](https://www.python.org/downloads/). After installing Python, install the ipykernel package locally

    python -m ipykernel install

Let's start by testing out Hydrogen using a simple python file. In your Gilbreth directory, create a new file called **hydrogen.py**

```{attention} If you edit a file in your remote directory, you'll be editing a local copy that updates the remote copy when you save. Therefore, when running local Hydrogen kernels, you won't have access to the cluster's environment or file system.
```

Hydrogen uses Python (.py) files to simulate Jupyter Notebooks. Similarly, it has markdown and code cells, which can be separated in the following way

    # %% markdown

    This is the content of the Markdown cell. $$H|\psi\rang = E|\psi\rang$$

    # %% codecell

    fish = 2+2
    print("Wow Kat, thank you for writing this tutorial!")

Try copying the above cells into your **hydrogen.py** file, and typing ```ALT-SHIFT-ENTER```
