# DISWebGateway

This is a native Distributed Interactive Simulation (DIS) websockets 
implementation.

Websockets are Javascript implementations of TCP sockets
(plus some extra special sauce.) This enables Javascript running 
inside an HTML page can send and receive binary DIS messages over
TCP. The implications for M&S can be significant; with WebGL
this enables 3D graphics inside the web page. Even without 
3D graphics many useful applications can be created via web
mashups with, for example, Google Maps, Open Street Map, and
D3.js graphics.

This distribution uses Jetty (a Java-based web application server
similar to Apache Tomcat in functionality) to implement the server
side of websockets. The application is configured via the
GatewayConfiguration.properties file in the root directory.

Included are web pages that implement simple Google Maps web
page and Open Street Map web pages that display the location 
of DIS entities using maps. These pages are in the content directory,
and require access to the map data providers.

This distribution includes a Javascript implementation of DIS
that encodes and decodes the standard IEEE binary format. Thus
DIS messages from legacy applications can be  forwarded 
to the web page from the server side and decoded in the web page. An example
of this is in the content directory, the same location the mapping
web pages are kept, and the constructive.html web page. As with the ESPDU
PDUs, the javascript can send and receive fire and detonation PDUs over
a native, Ethernet network, and allow you to make a wide range of DIS
applications.

There are a number of experimental features you probably shouldn't
mess with, including a Redis server for cloud-based distributions
that can scale, and an area of interest management (AOIM)/distributed data management
(DDM) implementation that uses Javascript to filter packets on the
server side on a per-connection basis.

License is BSD. Copyright 2008-2016 MOVES Institute, Naval Postgraduate
School.


