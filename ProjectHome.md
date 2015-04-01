# [Moved to GitHub](https://github.com/gregswift/keploy) #


Keploy is a python application that allows you to deploy your ssh public key to remote systems without having to remember all the little things, like file permissions.

## Features: ##

  * Push ssh public key to remote(s)
  * Remove ssh public key from remote(s)
  * Replace old public key with a new one on remote(s)
  * Can target all hosts in un-hashed known\_hosts file

## Usage: ##

  * To deploy your default public key (~/.ssh/{id\_rsa,id\_dsa,identity}.pub) to all hosts in your known\_hosts file:
> > ` # keploy -k `

  * To deploy your default public key to host remote.host.com:
> > ` # keploy remote.host.com `

  * **NEW** To deploy your default public key to host remote.host.com and auto accept the ssh public key:
> > ` # keploy -y remote.host.com `

  * To deploy your default public key to remote.host.com as user bob and enable Agent Forwarding:
> > ` # keploy -l bob -A remote.host.com `

  * To replace your old key (now ~/.ssh/id\_rsa.old.pub) with your new default public key onto all hosts in the file "~/myhosts":
> > ` # keploy -o ~/.ssh/id_rsa.old.pub -f ~/myhosts `

  * Remove your public key from all boxes in your known\_hosts file, and turn off Agent Forwarding:
> > ` # keploy -r -k -A `

## Supported Platforms ##
  * Linux
  * OSX

## Developed using ##
[![](http://wingware.com/images/wingware-logo-107x34.png)](http://wingware.com)