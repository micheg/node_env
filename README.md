# node_env:
manage virtual node environments.

# purpose:
This little script takes inspiration from this article:
https://medium.com/@jaheenafsarsyedks/how-to-create-a-virtual-environment-for-node-js-479c743ef137.

The aim of the project is to create a script able to manage node virtual environments, in a similar way to what Python does.
I created this "repository" because other similar solutions did not work correctly with OSX.

Currently the system has been tested on *OSX Catalina* and *Ubuntu*, but should work on any unix-like system with wget and tar.

# what is missing:
Much ... being a preliminary version at present it only supports OSX and Linux in x86 and x64 version, it completely lacks support for ARM or Windows systems.

Probably with a busybox portable it could also work on Windows, I'll test it as soon as possible.

# usage:

node_env **{NAME}** **{VERSION}**, ex:
  
	node_env my_env 12.12.0
  
then:

	. my_env/bin/activate
  
or
  
	node_env --list-version for installable versions

You can use the script directly from the network:

	curl -s https://raw.githubusercontent.com/micheg/node_env/main/node_env | bash -s -- --list-version

	curl -s https://raw.githubusercontent.com/micheg/node_env/main/node_env | bash -s my_env2 12.12.0

# to do:
A lot of things.
