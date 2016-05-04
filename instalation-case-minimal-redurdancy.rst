All application on two servers
==============================

In this architecture is exists two instance of each type of application.
Instances of applications (database, message brokers, media and etc), running on each server.

This sollution is permits:

1. implement redurance (no single point of failure);
#. load balance calls between two servers;
#. more simple to understand architecture, and more easy to maintain than maximum architecture.

Two server kazoo architecture is shown on figure below.
Communications with each to each circuit are shown on figure. 

.. image:: svg/kazoo_two_servers.svg
   :width: 500px
   :alt: Two servers Kazoo architecture



