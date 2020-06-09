.. _devops_integration_ansible:

.. meta::
    :description: Pureport
    :keywords: pureport, multicloud, fabric, cloud networking, Multicloud Router

=====================================
Ansible
=====================================

Pureport provides full integration with Ansible for automating the building of
mutlicloud and hybrid cloud networks.  Pureport provides a number of Ansible
collecitons that can be used to quickly build virtual networks and establish
connections to public cloud providers.  This document provides details on how
to use the Ansible collections.

Collections
-----------

Pureport curates multiple collections for providing integration with Ansible.
All collections are provide freely to the open source community and are fully
supported and backed by the Pureport engineering team.

Ansible collections provide both modules for automating tasks using the
Pureport Fabric API as well as automating full end to end connections between
Pureport and public cloud providers.

The source code for all collections are currenlty hosted at
`here <https://github.com/ansible-collections/pureport>`_.  As collections are
developed and completed, collections are released to Ansible Galaxy
`here <https://galaxy.ansible.com/pureport>`_.

Getting Started
---------------

To get started using the Pureport Ansible collections, you need to install the
collections into your local Ansible environment using the Ansible Galaxy
command.

.. code-block:: bash

    $ ansible-galaxy collection install pureport.fabric


The ``pureport.fabric`` collection provides all of the Pureport modules which
can be used to automate creating networks and collections in plays.  Once the
collection is installed, you can create playbooks for interactin with the
Pureport Fabric API.

Here is a very simple example a playbook that will create a new network.

.. code-block:: yaml

   ---
   - hosts: localhost
     tasks:
       - pureport.fabric.network:
           name: cloud network




