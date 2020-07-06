.. meta::
    :description: Pureport
    :keywords: pureport, multicloud, fabric, cloud networking, Multicloud Router

=====================================
Multicloud Fabric
=====================================

The Pureport Multicloud Fabric platform provides a software-as-a-service
solution that allows customers to build and operate cloud native networks for
connecting customer sites to public cloud providers over dedicated, high speed
cloud on-ramps without the need to invest in expensive network overlay
solutions or having to manage inefficient traffic paths due to inefficient
routing between clouds.

This document provides an overview of the Pureport Multicloud Fabric service
components and describes how those components work in conjunction with one
another to deliver a full end-to-end cloud native network infrastructure.

The Pureport Multicloud Fabric consists of the following:

* Fabric API
* Fabric Networks
* Fabric Connections
* Fabric Services


Fabric API
----------

Pureport believes in an API-first design philosophy and therefore, at the hear
of the Pureport Multicloud Fabric, is the Fabric API.  All configuration and
operational state is facilitated by the Fabric API.   The Fabric API represents
the demarcation point between all visible user services such as provisioning,
orchestration, configuration, etc) and all of the backend implementations to
realize those services.

The Fabric API is the only entry point available for interfacing with the
Pureport Multicloud Fabric and as such is the most critical element of the
service delivery.

The Fabric API provides a full declarative, Open API documented, RESTful API
service delivered over HTTPS for full programmatic control of all configuration
and operational tasks necessary to build and operate cloud native networks.

In order to fully realize the capabilities of the Fabric API, Pureport provides
a fully self service web console available at https://console.pureport.com.

Console
~~~~~~~

Providing an interface to the Pureport service, the Fabric Console provides
users with an easy to use point-and-click interface designed to make building
cloud native networks easy.  The Fabric Console provides customers with the
ability to configure, deploy, and manage cloud native networks.

For more details about how to use the Fabric Console, see :ref:`Fabric Console Users
Guide <users_guide_intro>`. for more details.

CLI
~~~



SDK
~~~



Fabric Networks
---------------

Fabric Networks represent a logical grouping of connections designed to provide
a multicloud or hybrid cloud service.  Fabric Networks are similar in
operation to public cloud providers VPCs and provide transit service between
clouds.  Customers can create as many virtual networks as necessary to support
multiple use cases.  Connections can be assign to one and only one Fabric
Network at a time.

For details on creating Fabric Networks please see the :ref:`Networks
<users_guide_networks>` section of the Users Guide.

Fabric Connections
------------------

Fabric Connections provide connectivity to a single public cloud service or
to a customer branch office or data center location.  Connections are
responsible for establishing connectivity to public clouds over dedicated links
or to private clouds over either private lines or VPN technology.  Pureport
connections support deployments at various speed tiers and are configured for
high availability by default.

Currently Pureport supports a number of different Fabric Connections depending
on the type of cloud or site you are connecting to.

Cloud Connect
~~~~~~~~~~~~~

The Pureport Cloud Connect connection provides network connectivity to a
public cloud provider over a private, high speed cloud on-ramp connection.
Cloud Connect connections are responsible for terminating network connections
into public cloud providers over high speed cloud connections.

Cloud Connect connections are typically deployed in pairs to support highly
available solutions by default.  Cloud Connect connections act as the
ingress / egress point between a Fabric Network and a public cloud provider.

Site Connect
~~~~~~~~~~~~

The Pureport Site Connect  provides network connectivity to remote offices over
encrypted IPSec VPN technology.  Site Gateways terminate IPSec tunnels to
customer sites at the edge of a Pureport Multicloud Fabric and then transport
traffic across the customers private Fabric Network to cloud providers.

Site Gateways deliver connectivity over the public Internet and are commonly
deployed in pairs supporting highly available connections.  See
:ref:`Connecting over IPSec VPN <connections_ipsec_vpn>` for more details.

Port Connect
~~~~~~~~~~~~

For large organizations that wish to directly connect sites to their Pureport
Fabric Network, Pureport provides a Port Gateway.  Port Gateways are designed
to terminate direct connectivity to the Pureport Multicloud Fabric over
dedicated fiber connectivity.  Port Gateway's are similar in functionality to
Site Gateway's however bring the added benefit of predicable high throughput,
low latency performance associated with private line fabric connectivity.

Port Gateways can be deployed in either highly available, redundant
connectivity or single connection to a Fabric Network.  For more details about
connecting over private line, please see :ref:`Connecting over Direct Fiber
<connections_port_connect>` for more details.

Fabric Services
---------------

In addition to provide fully meshed network connectivity to public clouds and
customer sites, Pureport also provides optional services that can be enabled to
enhance Fabric Gateways.

Cloud NAT
~~~~~~~~~

One of the challenges when connecting multiple networks together is overlapping
IP address space.  The easiest way to address this problem is to enable network
address translation (NAT) at points to solve this problem.  Just about every
cloud provider and network equipment manufacturer supports enabling NAT on
their respective service and device.

Operational challenge can result though due to different implementations
depending on the service and/or platform.  Having a single consist
implementation to NAT for connecting networks and cloud services reduces the
overall administrative burden of operating cloud networks.

Pureport provides a feature that can be optionally enabled on any Fabric
Gateway to enable network address translation.  By enabling NAT on Pureport
Gateways, organizations have a single point of administration and operation for
NAT implementations.
