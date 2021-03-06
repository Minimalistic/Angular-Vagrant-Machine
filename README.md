# Angular Vagrant Machine
This is a basic vagrant machine, that when you run the initial configuration of `vagrant up`, it downloads and configures a simple Ubuntu Artful64 Virtual Machine as well as installs NodeJS and NPM.

# Installation
After downloading/forking the repository, navigate to the project folder in a command prompt and enter `vagrant up` The console will then spill out a bunch of text while it prepares the environment. At some point during the installation you may see:

```
    default: SSH auth method: private key
    default: Warning: Connection reset. Retrying...
    default: Warning: Remote connection disconnect. Retrying...
    default: Warning: Connection reset. Retrying...
    default: Warning: Remote connection disconnect. Retrying...
```

If you do, just let it continue trying, it will eventually time out (should) automatically and correct itself.  There will then be *even more* configurations that are run.  This entire installation/configuration may take anywhere from 5-10 minutes depending on internet speed/computer specs.

When the automated configuration has completed and you have a command prompt again, enter `vagrant ssh` and you will be up and running inside the virtual machine.

Once you're properly inside the vagrant machine, you just need to do a few final steps to get Angular all setup.  Run:

`npm install -g @angular/cli`

Then you can create the app and it's folder:

`ng new my-angular-app`

Once that completes, you can:

`cd my-angular-app` in to your app folder and run:

`ng serve --open` to start the app server.

At this point, the app should be running at `http://localhost:4200/` and you can navigate to it using your web browser.

This virtual machine also has a pre-configured shared folder called `/shared_vagrant_folder` which then allows you to share files between the virtual machine and your OS.
