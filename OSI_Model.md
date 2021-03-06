The OSI Model
=============

So far we have spent all of our time describing the four-layer model
used to design and implement the TCP/IP protocols and applications that
make up the Internet. However, the TCP/IP  model is not the only model
we can use to help us understand how networks work. The other
model commonly used to make sense of network design is called
the Open System Interconnection (OSI) model. While the TCP/IP model
was designed and evolved as the TCP/IP protocols were developed,
deployed, and changed, the OSI model was the result of a careful design
process by many networking experts who worked to develop a general
approach to network models.

In today's networked world, the OSI model and the TCP/IP model serve two
different purposes.^[This, of course, is an oversimplification. Prior to 1990,
there *were* operational network implementations based on ISO specifications
that followed the OSI network model very closely. But today, those ISO/OSI 
network implementations no longer are in broad use.]
The TCP/IP model is an *implementation* model, in that it provides the
guidance for those who would build TCP/IP-compatible network hardware
or software. The OSI model is more of an *abstract* model that 
can be used to understand a wide range of network architectures.

While TCP/IP is the most widely used network technology today, many
different types of networks have been implemented and deployed 
over the past 50 years. And as we continue to improve and evolve networking, 
new implementation models may emerge.

The OSI model has seven layers instead of the four layers of the
TCP/IP model. Starting at the bottom (nearest the physical
connections) of the OSI model, the layers are: (1) Physical, (2) Data
Link, (3) Network, (4) Transport, (5) Session, (6) Presentation,
and (7) Application. We will look at each layer in the OSI model
in turn, starting with the Physical layer.

Physical (Layer 1)
--------------------

The OSI Physical layer deals with the physical attributes of the
actual wired, wireless, fiber optic, or other connection that is
used to transport data across a single link. The Physical layer also
defines the shapes of the connectors and type of media which can be used.
Another problem solved at this layer is how to encode the bits
(0's and 1's) that make up the data being sent across the
medium.^["Manchester Encoding" is a common technique for encoding 
bits for transmission across a wire.]
The "bit encoding" (or modulation) determines how fast data
can be sent across the link.

Data Link (Layer 2)
---------------------

The OSI Data Link layer is concerned with how the systems using
a physical link cooperate with one another. When data is broken
into packets, the Data Link layer defines special sequences to
indicate the beginning and end of each packet. The stations
communicating using the physical connection are assigned addresses
to allow for effective use of the media. Sometimes multiple stations
are sharing the same media (as on a wireless network) and the
Data Link layer defines how those stations will share the connections
with the other systems connected to the network. Most Data Link
layers also have some form of checksum to detect and/or correct for
errors in the transmitted data.

The design problems solved in the Physical and Data Link layers of
the OSI model are addressed by the Link layer of the TCP/IP model.

Network (Layer 3)
-------------------

Like the Internetwork Layer (IP) in the TCP/IP model, the OSI
Network layer deals with the global assignment of "routable"
addresses to the various systems connected to the network. The
Network layer governs how routers forward packets across multiple
hops to get from their source to their destination. Like the IP
layer, The OSI Network layer does not attempt to be error free,
as it assumes that lost data will be detected and retransmitted at
the next layer up.

Transport (Layer 4)
---------------------

The Transport layer in the OSI model manages packet loss and
retransmission as well as flow control and window size. The
rest of the functionality of the TCP/IP Transport layer is handled
in the Session layer in the OSI model.

Session (Layer 5)
-------------------

The OSI Session layer handles establishing connections between
applications. The Session layer deals with "ports" so that a
connecting client application can "find" the correct server
application on a particular system. Some aspects of secure
transmission are also handled in the OSI Session layer.

Presentation (Layer 6)
------------------------

The Presentation layer focuses on how data is represented and
encoded for transmission across the network. As an example,
the Presentation layer would describe how to encode the pixels
of an image so that the receiving application can properly
decode the data. The Presentation layer also handles data
encryption and decryption.

Application (Layer 7)
-----------------------

The OSI Application Layer is very similar to the Application layer
in the TCP/IP model, in that it contains the applications themselves.
Some applications are client applications that initiate connections,
and other applications are the server applications that respond to
those connection requests. The various pairs of applications
have protocol standards that define interoperability between multiple
clients and multiple servers from different vendors.

![Comparing the TCP and OSI Models](../images/iso-tcp)

Comparing the OSI and TCP/IP Models
-----------------------------------

We can use the OSI model to provide an alternative "view" of the
TCP/IP model by comparing how the OSI model breaks network
functionality into its layers and how the TCP/IP model breaks
its functionality into layers.

Link Layer (TCP/IP)
-------------------

The TCP/IP Link layer combines the Physical and Data Link layers
from the OSI model. The Physical and Data Link layers are usually
implemented in hardware.  Products like Ethernet, WiFi, satellite,
or fiber optic often are implemented in a network driver card that
plugs into the back of a computer or router. The network driver
card generally implements both the physical and the data link aspects
of the connection in the hardware on the card.  In most cases, the data
link layers are tuned to the limitations and requirements of their
corresponding physical layers. So in real systems, it is somewhat
rare for a particular data link layer to be arbitrarily paired with
any number of physical layers. Since it can be hard to separate the
physical and data link aspects for a particular link technology, the 
TCP model combines them into a single layer for simplicity.

Internetwork Layer (TCP/IP)
---------------------------

One place that maps pretty cleanly between the two models is
the OSI Network and TCP/IP Internetwork layers. They perform the
same functions of creating a globally routable address space and
building routers to insure that packets properly find their way
from the source to the destination across multiple hops.

Transport Layer (TCP/IP)
------------------------

The features of the Transport layer in TCP/IP are spread across the
Transport and Session layers of the OSI model.  The OSI Transport
layer deals with flow control and packet retransmission,
while the OSI Presentation layer deals with multiple applications
running on multiple ports as well as session establishment and teardown.

The Secure Sockets Layer (SSL) in the TCP/IP model corresponds to
parts of the Session and Presentation layers in the OSI model.

Application Layer (TCP/IP)
--------------------------

The TCP/IP Application Layer combines the non-security aspects of the
OSI Presentation layer and the OSI Application layer. While
many TCP/IP applications deal with issues like encoding and decoding
various types of data, the TCP/IP model does not see data formatting
as a separate "layer". Various data encoding and decoding technologies
are used in TCP/IP applications, but TCP/IP tends to treat these
capabilities as library code that applications make use of as needed
for the application.

Conclusion
----------

While the TCP/IP model described in this book is widely used to guide
the implementation of TCP/IP networks, hardware, and software, the
OSI model can help us look at and compare a wide range of network
architectures ranging from openly developed networks to proprietary
vendor-specific networks.

Glossary
--------

**abstract model**: A model and set of terminology that is used to generally
understand a problem area and guide the development of standards and
implementations to solve problems.

**implementation model**: A model and set of terminology that is used to 
guide the development of standards and an implementation to solve a particular
problem.

**ISO**: International Organization for Standardization.  A worldwide body
that develops standards in computing, networking, and many other areas.

**OSI**: Open System Interconnection.  A seven-layer model used to help organize 
the design of various approaches to network architecture.


Questions
---------

You can take this quiz online at http://www.net-intro.com/quiz/

1. What is the primary value of the OSI network model?
a) OSI networks are used in the southern hemisphere
b) The OSI approach can be use to analyze many different network models
c) OSI networks make better use of limited bandwidth
d) OSI networks are more secure

2. How many layers does the OSI model have?
a) Four
b) Six
c) Seven
c) Nine

3. Which of the OSI layers deals with the shape of connectors for network connections?
a) Physical
b) Data Link
c) Network
d) Transport

4. Which of the layers is most similar between the OSI and TCP network models?
a) TCP Link Layer and OSI Data Link Layer
b) TCP Internetwork Layer and OSI Network Layer
c) TCP Transport Layer and OSI Transport Layer
d) TCP Application Layer and OSI Session Layer

5. What layer does the TCP/IP Secure Sockets Layer map to in the OSI network model?
a) Secure Data Link Layer (SDLL)
b) Secure Network Layer (SNL)
c) Secure Transport Layer (STL)
d) Session and Presentation Layers

6. Why does the TCP model combine the OSI Data Link and Physical layers into a single Link layer?
a) Because the TCP model does not worry about the Physical layer
b) Because the TCP model designers were ignored at the 1981 OSI meeting in Utrect, Netherlands
c) Because quite often the design of Data Link and Physical layers are tightly connected for a particular technology
d) To make the TCP model easier to understand by end users



