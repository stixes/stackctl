# Stackctl

For those of us, who has not yet given up on the simplicity of docker swarm mode, here is a helper script with some quality of life improvements for managing stacks in a cluster.

Born from actual use in production and testing clusters, this simple tool accelerates some of the usual toil work related to using docker swarm mode and stacks in particular.

## Docker-compose

Comming from developer using docker-compose for setting things up, this tool mimics the workflows used in docker-compose, supporting up, down, stop and recreate, and adding in the suport for default .env files for configuration.

## stack.yml

The tool expects a compose type file named stack.yml to be present in the PWD. This may be accompanied by any support files like .env 

*Example*

    $ cd /stacks/my-stack
    $ ls -a
    stack.yml .env
    $ stackctl up

## Installation

The main script can be downloaded directly from github and placed in /usr/local/bin/ or however you prefer to install such utilities.

## Remote host and default environment

If exists, stackctl will source configuration from /etc/stackctl and $HOME/.stackctlrc for both universal and per user setup. This allow you to set other environment variables, such as default secrets for use in stack.yml files and DOCKER\_HOST and associated variables for accessing a non-local docker swarm.


