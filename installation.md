# Installation

**OSX, *nix** - Using the commad line line:

	ruby -e "$(curl -fsSL https://raw.github.com/protobox/protobox/master/ansible/shell/bootstrap)"

Alternatively, you can install it via git manually:

    git clone git@github.com:protobox/protobox.git protobox
    cd protobox && cp data/config/common.yml-dist data/config/common.yml

Make sure you add an entry to your `/etc/hosts` for any virtualhosts in your `data/config/common.yml` file:

	192.168.5.10    protobox.dev www.protobox.dev

Then run `vagrant up` and pull up `http://protobox.dev` in your browser to see if it is setup correctly.
