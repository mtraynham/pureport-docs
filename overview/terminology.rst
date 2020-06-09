.. meta::
    :description: Pureport
    :keywords: pureport, multicloud, fabric, cloud networking, Multicloud Router

=====================================
Terminology
=====================================

This page provides a list of term definitions that are used through the
Pureport documentation side along with a brief definition of each term.  

.. glossary::

   Network
        A network is the base building block within the Pureport Mutlicloud
        Fabric and represents a virtual cloud network.  Connections are added
        to networks in order to establish connectivity between clouds and
        sites.

   Connection
        A connection represents connectivty to a single cloud.  Connections are
        organized into virtual networks (:term:`Network`).  A connection will
        include one or two gateways (:term:`Gateway`).  

   Gateway
        Gateways are always tightly coupled with connections
        (:term:`Connection`) and provide a singular IP endpoint for attaching
        to a cloud.  Each connection will have at most two gateways (for high
        availability) but may in some cases only have one gateway.  



