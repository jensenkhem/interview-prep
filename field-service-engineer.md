# Virtualization

## What are the benefits of virtualization?
Virtualization uses software to create an abstraction layer over computer hardware, enabling the division of a server's resources multiple virtual machines (VMs). This 'abstraction layer' that allows efficient division of server resources is called a **hypervisor**. 

Each VM runs its own operating system (OS) and behaves like an independent computer, isolated from other VMs on the same physical hardare, even though it is running on just a portion of the actual underlying computer hardware.

## Containerization vs VMs

Containers are more lightweight and portable than VMs, as they do not have their own OS and computer resources dedicated to them and represent a package containing a binary and its necessary dependencies. 

However, since containers run on the same OS and VM as other containers, they are less isolated than VMs, which may be cause for security concerns.

### Use cases
#### VMs
- **Testing**: Allows testing of software in an isolated sandboxed environment
- **Development**: Useful for developers who need to program or test software to run on different operating systems
- **Redundancy / HA**: Virtual machines can be easily restored from backups during failures

#### Containers
- **CI/CD**: Containers are very useful for automated build/test/deploy pipelines due to their portability and small footprint

- **SOA**: Containers are good for SOA because of their ability to be scaled up and down and encapsulate a single application service

# Networking

## Basic Concepts
### DNS
A DNS server is a computer with a database that associates IP addresses with the names of computers. Takes in a name, finds its IP address, and provides access to the content.

### Router vs Switch

**Routers** are used to connect different networks, and forward data between networks. On the other hand, **switches** are used to connect devices *within* a network, and is responsible for sending device specific data, not to a network of multiple devices.

- **Layer 2**: MAC Addresses (Permanent)
- **Layer 3**: IP Addresses (Can change!)

### Proxy
A proxy server acts as a gateway between private and public networks. In order to restrict access to private networks, you first send your request to a proxy server, which then redirects you to the content you desire inside the private network.

A reverse proxy is similar, accept it intercepts requests from clients and redirects it to the appropriate server. This is an important concept in loadbalancing and replication.

# TLS Handshake 

## Key Generation
Server generates a public/private key, and a certificate is received from CA, which binds the public key to the identity of the server.

For mTLS, the client also needs to be issued a certificate.
## Handshake process
1. Client initiates contact with the server, server exchanges TLS version and other configuration information with client
1. Client verifies that the server is indeed who they say they are by checking the certificate signed by the CA associated with the server. If mTLS, the server will also have to verify the client.
1. Client generates a shared secret key that is encrypted with the server's public key. Can only be decrypted using the server's private key.
1. Secret key is decrypted, and session keys are distributed which encrypt all communication between the client/server from here on out.
1. Handshake concludes

## mTLS vs TLS
- **mTLS**: mTLS is used in situations that require strong client authentication, such as secure API access, where client identity verification is crucial.
- **TLS**: Used in situations where client identity verification is not critical, such as web browsing.

# SCADA
**S**upervisory **C**ontrol **A**nd **D**ata **A**cquisition

# Honeywell Questions
## About Honeywell
Based on what i've read, Honeywell is focused right now on providing solutions for industrial automation, transition to clean energy, aviation, and much more. 

## Why I would be a good fit

### Prior background
I understand I will be using my skills to service, configure, maintain and diagnose distributed
control systems and their respective networks. I am familiar with some virtualization technologies and
networking, as I did some work there in my COOP work terms at Willoglen Systems.

### Communication
I am not shy to ask for help because the priority is the safety of the operating facility. If I don't know or am unsure about something, I believe that it is important to communicate that clearly to the parties involved, and make some calls or whatever else is needed to resolve the issue. Risk management is the top priority in these situations.


