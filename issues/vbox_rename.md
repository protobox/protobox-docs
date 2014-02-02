# Virtualbox - Renaming Error

If you are receiving an error like the one below, this page will help you resolve it.

	A customization command failed:

	["modifyvm", :id, "--name", "protobox"]

	The following error was experienced:

	#<Vagrant::Errors::VBoxManageError: There was an error while executing `VBoxManage`, a CLI used by Vagrant
	for controlling VirtualBox. The command and stderr is shown below.

	Command: ["modifyvm", "5d9acc2a-ffb2-406e-83a0-5073e78ac6ab", "--name", "protobox"]

	Stderr: VBoxManage: error: Could not rename the directory '/home/protobox/VirtualBox VMs/protobox_default_1391243423387_88058' to '/home/protobox/VirtualBox VMs/protobox' to save the settings file (VERR_ALREADY_EXISTS)
	VBoxManage: error: Details: code NS_ERROR_FAILURE (0x80004005), component SessionMachine, interface IMachine, callee nsISupports
	VBoxManage: error: Context: "SaveSettings()" at line 2527 of file VBoxManageModifyVM.cpp
	>

	Please fix this customization and try again.

This appears to be a common vagrant error without pre-set solution yet [1][2][3]. In our experience trying the following helped resolve the issue depending on your configuration:

- `vagrant reload` - this should hopefully clear up the issue
- open virtualbox application, if you see an old machine on the left delete it if you don't need it
- try a `vagrant destroy -f` to clear the old one out
- if all else fails you can manually delete `/home/protobox/VirtualBox VMs/protobox_default_1391243423387_88058` (folder from the error above) and `vagrant up` should work

If none of these work, please file an issue at the [vagrant github repository](https://github.com/mitchellh/vagrant/issues/).

[1] https://github.com/mitchellh/vagrant/issues/1198
[2] https://github.com/mitchellh/vagrant/issues/1817
[3] https://github.com/mitchellh/vagrant/issues/1809