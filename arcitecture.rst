Kazoo architecture
==================

Kazoo contains following types of servers

1. database (CouchDB);
#. application (whistle, ecallmgr);
#. message broker (RabbitMQ);
#. media (FreeSwitch);
#. registration and proxy (Kamailio).

General kazoo architecture is shown on Fig. 1

.. image:: svg/kazoo_general_arhitecture.svg
   :width: 500px
   :alt: Kazoo general architecture
         

Database servers
----------------

Given type of servers stores:

1. kazoo configuration;
#. media files (announcements, music on hold, voice mail and etc);
#. call detail records (CDR).

Application servers
-------------------

On this servers is executes call processing. Given type of servers contains folowing application:

1. whistle;
#. ecallmgr.

Whistle application prepares call processing rules. Ecallmgr application is executes call processing rules on media servers.

Message broker
---------------

All exchange between whistle application, ecallmgr and registation servers (description of the functions listed below) is executed via message broker.
Message broker is delivers request and responces between kazoo components.

Media servers
-------------

This type of servers is:

1. proceses SIP messages from/to endpoints (hardware and software phones, gateways);
#. proxyes RTP media;
#. transcodes media.

In simple configuration media servers act as registrator.

Registration and proxy servers
------------------------------

This type of servers is:

1. Stores information about SIP-endpoints registration;
#. delivers sip messages to endpointd via NAT devices (NAT traversal);
#. executes load bancing calls betwen media servers;
#. executes simple fraud and DDoS protection.

In simple configuration separate registrator (proxy) server may be not installed.
