# beedock (xhyve + docker)

Xhyve already utilizes docker, but locks you in on a network and provides a lot of complication to just running a host on a KVM similar to other solutions.

The goal of this CLI is to simplyfy that and provide an entry point for macOS. My needs are wanting to test things in different environments from my Macbook, create a VM that MaaS can provision, and also deploy nodes that kubernetes can utilize.

These needs have different needs, but one problem comes to having a cli like xhyve to provision VMs, a tool like tuntap to provision a network, and hyperkit to run it.

The goal is to have something hopefully as easy as docker and KVM and contains all of the features you need to perform similar functions.
