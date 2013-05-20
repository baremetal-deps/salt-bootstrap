Bootstrapping Salt
==================

This is a fork of Saltstack's bootstrap script with the modifications outlined below.


Basic Usage
-----------

```
wget https://raw.github.com/baremetal-deps/salt-bootstrap/master/bootstrap-salt.sh
sudo bash bootstrap-salt.sh git git://github.com/baremetal-deps/salt.git master
```


Modifications
-------------

### Prevent failure when installing to a LXC ###

A modification to the upstream source was made which prevented successful
installation on a Linux Container.  This branch adjusts the patch to leave
behind a working salt minion on a LXC.


### Specify repository when using the git installation target ###

Override the default repository when using git as the install target.  Note, if
you specify a repository, you must specify a branch.
