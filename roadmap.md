# Roadmap

These are some features are exploring, in order of importance. 

1. **Create Ruby Gem** - This would allow us to simply the installation process and add a lot more functionality to protobox. You will be able to `gem install protobox` to install it globally. You will also be able to `protobox new` within a directory to pull down the protobox files.

2. **Make Applications / Provisioning Dynamic** - This would unbundle the applications from the main repository and move them to external repositories. In your protobox yaml file you can specify repositories to be downloaded during `protobox install`. This will allow dynamic installation and provisioning of any ansible playbooks.

3. **Improve Web GUI Settings** - The web GUI settings like php ini are hard to enter. This should be reworked for a better user experience.

4. **Improve Web GUI Applications** - Applications should be able to bundle a YAML file with form field questions to ask on the protobox website. These form fields will then be stored in the yaml and passted to the dynamic playbooks.

5. **Create Expore Area** - Add a form to submit boxes on the website with the git url and author information. This will allow users to find your boxes on the website and install them with protobox.

6. **Improve Dashboard** - The dashboard needs to be reworked to include a lot more data. It should list all of the mysql databases, usernamees and passwords. If you installed tools like phpmyadmin and others it should report them here. Applications should be able to bundle settings like admin urls, logins, etc. It should keep an ansible log and make it easy to share when reporting a bug. 

7. **Dependencies** - Applications and software should have dependencies. So on the Web GUI, we need to check to make sure these dependencies are met before generating a config.

8. **Easy / Advanced Mode** - When installing an application I would like to have a global toggle that shows / hides fields based on whether or not it is something the average user would need to change. For example when installing a common application like a cms, it is typically only going to work with a certain langauge, database, etc. On easy mode these advanced options will all be hidden.

9. **Improve Web GUI UX** - Implement push state so that you can use the back button between tabs. Make sure forms can be tabbed all the way through. Try to catch errors before they submit, such as dependencies. Add some social features to tweet and share your new configuration.

10. **Live Provisioning** - Look into using protobox to provision a server a digital ocean, aws, etc. 

11. **Docker** - Look at using docker instead of VMs. This could open up the oppoturnity to have one protobox install with all of the configurations powering different containers. It could optionally include a container like docker shipyard for having a web gui to maintain your other containers. This opens up the possibility for using your existing VM to install and provision more containers. 

## Contributing

[If you are interested in helping, please read here.](contributing.md)