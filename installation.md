# Installation

Using the command line line (**OSX, *nix**):

	vagrant plugin install vagrant-protobox
	ruby -e "$(curl -fsSL https://raw.github.com/protobox/protobox/master/lib/shell/bootstrap)"

Then run `vagrant up` and pull up `http://192.168.5.10/` in your browser to see if it is setup correctly.

## Having issues?

If you have any problems during installation or receive any error messages, check out our [common issues](issues.md)

## Advanced Installation

Alternatively, you can install it via GIT:

	vagrant plugin install vagrant-protobox
    git clone git@github.com:protobox/protobox.git protobox
    cd protobox && cp data/config/common.yml-dist data/config/common.yml

Or, download the [protobox.zip](https://github.com/protobox/protobox/archive/master.zip) and open terminal to run the following:

	cd /your/protobox/directory
	vagrant plugin install vagrant-protobox
	cp data/config/common.yml-dist data/config/common.yml
