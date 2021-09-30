# Chapter 3 Transport Layer

- [3.1 Introduction and Transport-Layer Services](#31-Introduction-and-Transport-Layer-Services)
- [3.2 Multiplexing and Demultiplexing](#32-Multiplexing-and-Demultiplexing)

## 3.1 Introduction and Transport-Layer Services

A transport-layer protocol provides for logical communication between application processes running
on different hosts. By logical communication, we mean that from an application’s perspective, it is as if
the hosts running the processes were directly connected; in reality, the hosts may be on opposite sides
of the planet, connected via numerous routers and a wide range of link types.

### Relationship Between Transport and Network Layers

Recall that the transport layer lies just above the network layer in the protocol stack. Whereas a
transport-layer protocol provides logical communication between processes running on different hosts, a network-layer protocol provides logical-communication between
hosts.

## 3.2 Multiplexing and Demultiplexing

- **Demultiplexing**: Each transport-layer segment has a set of fields in the segment for this purpose. At the receiving end, the transport layer examines these fields to identify the receiving socket and then directs the segment to that socket. This job of delivering the data in a transport-layer segment to the correct socket.
- The job of gathering data chunks at the source host from different sockets, encapsulating each data chunk with header information (that will later be used in demultiplexing) to create segments, and passing the segments to the network layer is called **multiplexing**.

Each port number is a 16-bit number, ranging from 0 to 65535. The port numbers ranging from 0 to 1023 are called well-known port numbers and are restricted.
