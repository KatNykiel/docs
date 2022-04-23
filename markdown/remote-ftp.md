# Remote FTP
Atom describes itself as a 'hackable' text editor because it has thousands of community-made packages which greatly extend the utility of Atom. We're now going to install some useful packages

**Remote FTP** is a package that transfers files between local and remote servers. This is useful when connecting to RCAC clusters or nanoHUB. In this exmaple, we'll demonstrate how to connect to the Gilbreth cluster.

Press ```CTRL + ,``` to open the Settings menu. From here, click 'Install.' This lets you query and install packages for Atom.

Locate and install the 'remote-ftp' package (by icetee). After it's done installing, you can select 'Packages -> Remote FTP -> Toggle' from the menu bar. This will open a new tab in your left pane.

```{note} The left tab labeled 'project' is your local project folder - the right 'remote' tab is your remote file manager. Remote FTP will sync any remote changes locally
```
To connect to the  Gilbreth cluster, we need to create an .ftpconfig file. This is done by selecting 'Packages -> Remote FTP -> Create FTP config file'

In this file, there are a few settings we need to change.
- host: 'gilbreth.rcac.purdue.edu'
- user: '[[YOUR USERNAME]]'
- pass: '[[YOUR PASSOWRD]]' (we'll set up SSH keys later)
- remote: 'home/[[YOUR USERNAME]]'

```{attention} WARNING
Add '.ftpconfig' to your .gitignore file! You should never commit your .ftpconfig file, it contains your password

TODO: ssh keys
