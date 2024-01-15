# IPv4 Overview 

A device gets an IP from the internet router

In an IP like this one here:   

***192.168.1.204***

In each position we can have a number between 0 and 255, with 256 posible combinations! Each 3 digit position is called an Octet. 

We also have Subnet Masks, in a subnet mask, like this one here:  

***255.255.255.0***

If an Octet of the Subnet Mask is *255*, we know that the corresponding Octet of our IPv4 will stay the same within the network.

So, in our ***192.168.1.204***, we know that the first *3 octets* will always be the same, only the last octet will change!

## IPv4 Network and Host portions 

Using the previous IPv4 as an example, we can separate our IP in two parts:

- ***192.168.1***: This is the **Network Portion**, all devices within the network share the same network portion.

- ***.204***: This is the **Host Portion**, this is the part that diferentiates devices within the network

As an ***ANALOGY***, the Network Portion can be compared to a street, and the Host portion can be compared to an Individual House!

With this logic, in a private network we can have up to 254 different usable IP addresses! But why 254 and not 256?  
- The address 192.168.1.0 is reserved and is our **Network Address**

- The address of 192.168.1.255 is our ***Broadcast Address***, this address is used to send data to all devices within a network subnet

- And our 192.168.1.1 is our ***Default Gateway***
    - It's our router IP Address
    - This is what allows us to talk to the internet


## IPv4 Classes

| Class    | First Octet Range | IP Range                    | Subnet Mask   |
| -------- | ----------------- | --------------------------- | :-----------: |
| Class A  | 0 - 126           | 0.0.0.0 - 126.255.255.255   | 255.0.0.0     |
| Class B  | 128 - 191         | 128.0.0.0 - 191.255.0.0     | 255.255.0.0   |
| Class C  | 182 - 223         | 192.0.0.0 - 223.255.255.0   | 255.255.255.0 |
| Class D  | 224 - 239         | 224.0.0.0 - 239.255.255.255 | -             |
| Class E  | 240 - 255         | 240.0.0.0 - 255.255.255.255 | -             |

### Important points
Class D are reserved for multicast, we can't touch this one
Class E are experimental, we can't touch this one either

***And what about the entire 127 octet range?***
These are called *Loop Back* addresses, they are used for network testing, the only dumb thing is, with the subnet mask, this 127 IP has about 16 million addresses reserved for testing, which is unnecessary!

## What's NAT

***Network Address Translation (NAT)*** is a technique used to map private IP addresses within a local network to a single, shared public IP address.

Each device in your local network has a unique private IP assigned by your router. When these devices access the internet, the NAT device assigns them temporary public IP addresses from your Internet Service Provider (ISP). 

This allows multiple devices within your local network to share a common public IP for internet communication.
