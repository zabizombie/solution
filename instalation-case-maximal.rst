Each application on separate servers
====================================

In the maximum kazoo configuration each application is installed on separate servers.
This solution is permits:

1. easy increase performance of each type on servers;
#. implement redundancy (no single point of failure);
#. implement easy software version upgrade.

Maximum kazoo architecture is shown on figure below.
To simplify the figure are not shown the communications with each to each circuit.

.. image:: svg/kazoo_max.svg
   :width: 500px
   :alt: Kazoo maximal architecture


