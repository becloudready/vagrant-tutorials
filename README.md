# vagrant
Vagrant examples 

# Hello World Vagrant

Download and install vagrant on your PC/Mac, open command prompt

```
mkdir helloworld
vagrant init centos/7
vagrant up
vagrant ssh
```

After the last command you will be inside the newly created vagrant linux box. If you are inside Proxy please make sure to export the proxy variable

```
export http_proxy=<myproxy:port>
```

# Repo Layout

Each example has been categorized in directory fashion and it fully working example.These examples are meant to be idiot proof, if they are not, then call us idiot and raise issue we will fix it.

## ansible-example instruction

Make sure you have installed latest version of Virtualbox and Vagrant
```
git clone https://github.com/becloudready/vagrant.git
cd vagrant/ansible-example
ansible up --provision
```

## multiple-machine

Make sure you have installed latest version of Virtualbox and Vagrant
```
git clone https://github.com/becloudready/vagrant.git
cd vagrant/multiple-machine
ansible up --provision
```
If you have mutliple network adaptors it would ask for which adaptor to select, as by default I have chosen for public_network which would create a bridge interface.

In my machine it shows like, I select 1 [ WiFi ]

```
==> node03: Available bridged network interfaces:
1) en0: Wi-Fi (AirPort)
2) en1: Thunderbolt 1
3) en2: Thunderbolt 2
4) p2p0
5) awdl0
6) bridge0
==> node03: When choosing an interface, it is usually the one that is
==> node03: being used to connect to the internet.
    node03: Which interface should the network bridge to? 1
==> node03: Preparing network interfaces based on configuration...
```
