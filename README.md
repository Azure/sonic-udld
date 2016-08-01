SONiC NAS DAEMON
============

Network abstraction service daemon. 

Description
-----------

This repo contains the Network abstraction service daemon. This initializes the various components of Network abstraction service.  

Building
---------
Please see the instructions in the sonic-nas-manifest repo for more details on the common build tools.  [Sonic-nas-manifest](https://github.com/Azure/sonic-nas-manifest)

Build Requirements:
 - sonic-base-model
 - sonic-common-utils
 - sonic-nas-common
 - sonic-object-library
 - sonic-logging
 - sonic-nas-ndi
 - sonic-nas-ndi-api
 - sonic-nas-linux
 - sonic-nas-interface
 - sonic-nas-l2
 - sonic-nas-l3
 - sonic-nas-platform-s6000
 - sonic-nas-acl
 - sonic-nas-qos

Copy the debian files to the parent folder (default location of debian files) and then run the following command:

Dependent Packages:
  libsonic-logging1 libsonic-logging-dev libsonic-common1 libsonic-common-dev libsonic-model1 libsonic-model-dev libsonic-object-library1 libsonic-object-library-dev libsonic-nas-common1 libsonic-nas-common-dev sonic-ndi-api-dev sonic-sai-api-dev libsonic-nas-ndi1 sonic-object-library sonic-nas-ndi-api-dev libsonic-nas-ndi-dev libsonic-nas-linux1 libsonic-nas-linux-dev libsonic-nas-interface1 libsonic-nas-interface-dev libsonic-nas-acl1 libsonic-nas-acl-dev libsonic-nas-l2-1 libsonic-nas-l2-dev libsonic-nas-l3-1 libsonic-nas-l3-dev libsonic-nas-qos1 libsonic-nas-qos-dev libsonic-nas-platform-s6000-1 libsonic-sai-common-utils1 libsonic-sai-common1

BUILD CMD: sonic_build --dpkg libsonic-logging1 libsonic-logging-dev libsonic-common1 libsonic-common-dev libsonic-model1 libsonic-model-dev libsonic-object-library1 libsonic-object-library-dev sonic-nas-ndi-api-dev libsonic-nas-common1 libsonic-nas-common-dev sonic-object-library sonic-ndi-api-dev sonic-sai-api-dev libsonic-nas-ndi1 libsonic-nas-ndi-dev libsonic-nas-linux1 libsonic-nas-linux-dev libsonic-nas-interface1 libsonic-nas-interface-dev libsonic-nas-acl1 libsonic-nas-acl-dev libsonic-nas-l2-1 libsonic-nas-l2-dev libsonic-nas-l3-1 libsonic-nas-l3-dev libsonic-nas-qos1 libsonic-nas-qos-dev libsonic-nas-platform-s6000-1 --apt libsonic-sai-common-utils1 libsonic-sai-common1 -- clean binary

NOTE:
This build command uses the S6000 platform library - this will not effect runtime behaviour (can be used on the VM or any platform).

(c) Dell 2016

