# Chapter 2 Application Layer

Network applications are the raisons d’être of a computer network—if we couldn’t conceive of any useful
applications, there wouldn’t be any need for networking infrastructure and protocols to support them.
Since the Internet’s inception, numerous useful and entertaining applications have indeed been created.
These applications have been the driving force behind the Internet’s success, motivating people in
homes, schools, governments, and businesses to make the Internet an integral part of their daily
activities.

## 2.1 Principles of Network Applications

- The **application architecture**, on the other hand, is designed by the application developer and dictates how the application is structured over the various end systems. In choosing the application architecture, an application developer will likely draw on one of the two predominant architectural paradigms used in modern network applications: the client-server architecture or the peer-to-peer (P2P) architecture.
In a **client-server architecture**, there is an always-on host, called the server, which services requests from many other hosts, called clients.
In a **P2P architecture**, there is minimal (or no) reliance on dedicated servers in data centers. Instead the application exploits direct communication between pairs of intermittently connected hosts, called peers.
  - One of the most compelling features of P2P architectures is their **self-scalability**. For example, in a P2P file-sharing application, although each peer generates workload by requesting files, each peer also adds service capacity to the system by distributing files to other peers. P2P architectures are also cost effective, since they normally don’t require significant server infrastructure and server bandwidth (in contrast with clients-server designs with datacenters). However, P2P applications face challenges of security, performance, and reliability due to their highly decentralized structure.

### Transport Services Available to Applications

#### Reliable Data Transfer

Something has to be done to guarantee that the data sent by one end of the application is delivered correctly and completely to the other end of the application. If a protocol provides such a guaranteed data delivery service, it is said to provide **reliable data transfer**.

When a transport-layer protocol doesn’t provide reliable data transfer, some of the data sent by thesending process may never arrive at the receiving process. This may be acceptable for **loss-tolerant applications**, most notably multimedia applications such as conversational audio/video that can tolerate some amount of data loss.

#### Throughput

Applications that have throughput requirements are said to be **bandwidth-sensitive applications**. Many current multimedia applications are bandwidth sensitive, although some multimedia applications may use adaptive coding techniques to encode digitized voice or video at a rate that matches the currently available throughput.

While bandwidth-sensitive applications have specific throughput requirements, **elastic applications** can make use of as much, or as little, throughput as happens to be available. Electronic mail, file transfer, and Web transfers are all elastic applications. Of course, the more throughput, the better. There’san adage that says that one cannot be too rich, too thin, or have too much throughput!

#### Timing

A transport-layer protocol can also provide timing guarantees. As with throughput guarantees, timing guarantees can come in many shapes and forms. An example guarantee might be that every bit that the sender pumps into the socket arrives at the receiver’s socket no more than 100 msec later.

For non-real-time applications, lower delay is always preferable to higher delay, but no tight constraint is placed on the end-to-end delays.

#### Security

Finally, a transport protocol can provide an application with one or more security services. For example,
in the sending host, a transport protocol can encrypt all data transmitted by the sending process, and in
the receiving host, the transport-layer protocol can decrypt the data before delivering the data to the
receiving process. Such a service would provide confidentiality between the two processes, even if the
data is somehow observed between sending and receiving processes. A transport protocol can also
provide other security services in addition to confidentiality, including data integrity and end-point
authentication.

### Transport Services Provided by the Internet

The Internet (and, more generally, TCP/IP networks) makes two transport protocols available to
applications, UDP and TCP. When you (as an application developer) create a new network application
for the Internet, one of the first decisions you have to make is whether to use UDP or TCP. Each of
these protocols offers a different set of services to the invoking applications.

#### TCP Services

The TCP service model includes a connection-oriented service and a reliable data transfer service.
When an application invokes TCP as its transport protocol, the application receives both of these
services from TCP.

- **Connection-oriented service**. TCP has the client and server exchange transport-layer control information with each other before the application-level messages begin to flow. This so-called handshaking procedure alerts the client and server, allowing them to prepare for an onslaught of packets. After the handshaking phase, a **TCP connection** is said to exist between the sockets of the two processes. The connection is a full-duplex connection in that the two processes can send messages to each other over the connection at the same time. When the application finishes sending messages, it must tear down the connection.
- **Reliable data transfer service**. The communicating processes can rely on TCP to deliver all data
sent without error and in the proper order. When one side of the application passes a stream of
bytes into a socket, it can count on TCP to deliver the same stream of bytes to the receiving socket,
with no missing or duplicate bytes.

TCP also includes a congestion-control mechanism, a service for the general welfare of the Internet
rather than for the direct benefit of the communicating processes. The TCP congestion-control
mechanism throttles a sending process (client or server) when the network is congested between
sender and receiver.

> Neither TCP nor UDP provides any encryption—the data that the sending process passes into its socket is the same data that travels over the network to the destination process. Because privacy and other security issues have become critical for many applications, the Internet community has developed an enhancement for TCP, called **Secure Sockets Layer (SSL)**.

#### UDP Services

UDP is a no-frills, lightweight transport protocol, providing minimal services. UDP is connectionless, so
there is no handshaking before the two processes start to communicate. UDP provides an unreliable
data transfer service—that is, when a process sends a message into a UDP socket, UDP provides no
guarantee that the message will ever reach the receiving process. Furthermore, messages that do arrive
at the receiving process may arrive out of order.

UDP does not include a congestion-control mechanism, so the sending side of UDP can pump data into
the layer below (the network layer) at any rate it pleases. (Note, however, that the actual end-to-end
throughput may be less than this rate due to the limited transmission capacity of intervening links or due
to congestion).

## 2.2 The Web and HTTP

HTTP uses TCP as its underlying transport protocol (rather than running on top of UDP).

It is important to note that the server sends requested files to clients without storing any state
information about the client. If a particular client asks for the same object twice in a period of a few
seconds, the server does not respond by saying that it just served the object to the client; instead, the
server resends the object, as it has completely forgotten what it did earlier. Because an HTTP server
maintains no information about the clients, HTTP is said to be a **stateless protocol**.

### Non-Persistent and Persistent Connections

- **non-persistent connections**: each request/response sent over a *separate* TCP connection
  - Non-persistent connections have some shortcomings
    - a brand-new connection must be established and maintained for *each requested object*
    - each object suffers a delivery delay of two RTTs—one RTT to establish the TCP connection and one RTT to request and receive an object
- **persistent connections**: all of the requests and their corresponding responses be sent over the *same* TCP connection

With HTTP 1.1 persistent connections, the server leaves the TCP connection open after sending a
response. Subsequent requests and responses between the same client and server can be sent over
the same connection. In particular, an entire Web page (in the example above, the base HTML file and
the 10 images) can be sent over a single persistent TCP connection.

### HTTP Message Format

The HTTP specifications [RFC 1945; RFC 2616; RFC 7540] include the definitions of the HTTP
message formats. There are two types of HTTP messages, request messages and response messages,
both of which are discussed below.

#### HTTP Request Message

    GET /somedir/page.html HTTP/1.1
    Host: www.someschool.edu
    Connection: close
    User-agent: Mozilla/5.0
    Accept-language: fr

The first line of an HTTP request message is called the **request line**; the subsequent lines are called the **header lines**.

#### HTTP Response Message

    HTTP/1.1 200 OK
    Connection: close
    Date: Tue, 18 Aug 2015 15:44:04 GMT
    Server: Apache/2.2.3 (CentOS)
    Last-Modified: Tue, 18 Aug 2015 15:11:03 GMT
    Content-Length: 6821
    Content-Type: text/html

    (data data data data data ...)
