# Hosts Issue

## How do I add an entry to my `/etc/hosts` file?

Adding an entry to your `hosts` file will allow you to access your website in the virtual machine by a url. For example you can add an entry for `http://protobox.dev/` which would try to connect to your virtual machine IP.

For our first entry lets try getting `http://protobox.dev` to work with the default protobox configuration. Open up your terminal app and type `sudo nano /etc/hosts`. Paste the following entry below into the file. Note: you may have to type your system password to access the file.

	192.168.5.10    protobox.dev www.protobox.dev

Now press `ctrl+o` to write to the file and `ctrl+x` to exit. Thats it! If your vagrant machine is running you should now be able to access `http://protobox.dev` in your web browser.

You will need to repeat this process for each virtual host that you have setup for apache or nginx. The IP address will be the one you picked in the Vagrant section of the website. The domain is what you picked during the Server Name section of apache or nginx configurations.