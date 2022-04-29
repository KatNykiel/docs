# Platformio IDE Terminal

In addition to managing and editing files, it's often useful to have a command line interface directly connected to the clusters. For this, we'll use a package called **platformio-ide-terminal**

Similarly to Remote FTP, search for this package in settings and installer

```{note}
Ensure that you are installing the correct *terminal* package, not the other platformio-ide tools (though those can be useful as well)
```

To automatically connect to a cluster by default, open Settings (```CTRL + ,```), then select 'Packages → platformio-ide-terminal → Settings'. Within these settings, set 'Auto Run Command' to your ssh connection line. For example,

    ssh [[YOUR USERNAME]]@gilbreth.rcac.purdue.edu

```{note}
If you set up SSH keys in the previous step, those should let you connect automatically without the need of a password or 2FA
```

If you want to files in the cluster directly from the Atom editor, change your SSH command to use port-forwarding, as below

    ssh -L[[1234]]:localhost:[[1234]] [[YOUR USERNAME]]@gilbreth.rcac.purdue.edu

Where [[1234]] is some arbitrary 4-digit number you'll use as a port

```{note}
Within these same settings, you can assign some shortcuts to phrases you type a lot (squeue ..., cd /scratch..., etc.). We'll discuss how to assign these shortcuts to hotkeys in the 'keybindings' section later on
```
