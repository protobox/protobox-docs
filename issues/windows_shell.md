# Windows - Shell command error

If you are receiving an error like the one below, this page will help resolve it.

	[default] Running provisioner: shell...
	[default] Running: C:/Users/Valan/AppData/Local/Temp/vagrant-shell20131218-8956-1osvdtb
	stdin: is not a tty
	/vagrant/ansible/shell/os-detect.sh: line 2: $'\r': command not found
	/vagrant/ansible/shell/os-detect.sh: line 5: $'\r': command not found
	/vagrant/ansible/shell/os-detect.sh: line 11: $'\r': command not found
	/vagrant/ansible/shell/os-detect.sh: line 19: syntax error near unexpected token `elif'
	'vagrant/ansible/shell/os-detect.sh: line 19: `    elif [ $(which lsb_release) ]; then
	/vagrant/ansible/shell/os-detect.sh: line 2: $'\r': command not found
	/vagrant/ansible/shell/os-detect.sh: line 5: $'\r': command not found
	/vagrant/ansible/shell/os-detect.sh: line 11: $'\r': command not found
	/vagrant/ansible/shell/os-detect.sh: line 19: syntax error near unexpected token `elif'
	'vagrant/ansible/shell/os-detect.sh: line 19: `    elif [ $(which lsb_release) ]; then

This error is the result of being on a windows machine and checking out the git repository with windows line endings when the shell script needs unix line endings to work.

You can typically solve this by trying the following:

- Using `notepad++` to convert the files to unix line endings
- Try to use `dos2unix` to convert to unix line endings
- Try to checkout the git repository without windows line endings
