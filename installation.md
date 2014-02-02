# Installation

**OSX, *nix** - Using the commad line line:

	ruby -e "$(curl -fsSL https://raw.github.com/protobox/protobox/master/ansible/shell/bootstrap)"

Alternatively, you can install it via git manually:

    git clone git@github.com:protobox/protobox.git protobox
    cd protobox && cp data/config/common.yml-dist data/config/common.yml

Then run `vagrant up` and pull up `http://192.168.5.10/` in your browser to see if it is setup correctly.
