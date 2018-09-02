# configuring-a-virtual-machine
 To setup a virtual machine running a windows OS, We would be using [`vagrant`](https://www.vagrantup.com/) and [`virtualbox`](https://www.virtualbox.org/).

 `Vagrant` is an open-source software product for building and maintaining portable virtual software developement environments. We can use `vagrant` to build a `box` from scratch or use an existing box

 [`Box`](https://www.vagrantup.com/docs/boxes.html) is the package format for Vagrant environments. A box can be used by anyone on any platform that Vagrant supports to bring up an identical working environment.


`Virtualbox` is a free and open-source hosted hypervisor for x86 computers currently being developed by Oracle Corporation. Basically, `virtualbox` enables us to run more than one operating system at a time. For example, On my MacOS I could also run a windows OS.


# Prerequisites
To follow along with this guide, we need to have `vagrant` and `virtualbox` installed on our system. If you don't have them installed, follow the steps below

1. Ensure you have [`homebrew`](https://brew.sh/) installed on your system or click [`here`](https://brew.sh/) for instruction on installing `homebrew`
2. To install vagrant, run the command below in your terminal
   ```
   brew install cask vagrant
   ```
3. To install virtualbox, run the command below
   ```
   brew install cask virtualbox
   ```

## Procedure
After completing the prerequisites, follow the steps below to configure a virtual machine on your system.

1. Clone the repository below on github, run the command below to do that
   ```
   git clone https://github.com/kensanni/configuring-a-virtual-machine.git
   ```
2. Move into `configuring-a-virtual-machine` directory
   ```
   cd configuring-a-virtual-machine
   ```
3. To build the windows OS, run
   ```
   vagrant up
   ```
   This might takes some time, depending on your network connectivity since the size of the box is a little bit large.

4. run `virtualbox` to open the virtualbox UI and click on the `show` button to open your windows OS
   
   <img src="http://res.cloudinary.com/sannikay/image/upload/v1535883719/server-setup_pvdwmx.png">
 
When we run `vagrant up`, vagrant checks for a `Vagrantfile`. Vagrantfile is a configuration file for vagrant, here we specified an existing windows OS vagrant box.

## Trobleshooting

If you are getting an error like the one below
<img src="https://res.cloudinary.com/sannikay/image/upload/v1535884417/error_ymyvuy.png">

This is most likely caused by a poor network connectivity. To fix this error, ensure you have a stable network and also prevent your system from going to sleep while `vagrant up` is still running.
