# ke4ahr.github.io
This is a website for explaining the various software hosted at GitHub.

# rax25kb: https://github.com/ke4ahr/rax25kb/
CAVEAT: The version numbers are messed up; the order is 1.0.0, 2.0.0, 1.6.1, 1.6.2, and so on.  This is a R(everse) AX.25 KISS Bridge, written in Rust. It is a highly functional, highly capable serial communication system for amateur radio operators. It is capable of operating on Windows, Linux, and anywhere else Cargo can build Rust code. 

The 1.0.0 version functions as a shim between a radio with a built-in TNC and a consumer application using TCP port X (X is any port number the user is able to bind to). The shim corrects outgoing KISS packets before they leave the serial port to prevent TNC crashes. The shim also corrects KISS packets as they are recieved from a TASCO chipset TNC in the radio. Enable the PhilFlag to kick in the features to "fix" your radio. This program does not address the TNC bug as a result of hearing an APRS Beacon packet over 76 bytes however. The application supports all varieties of KISS protocol except for SMACK. It has the ability to listen on a loopback, IPv4, or IPv6 TCP port and connect the TCP client with local resources: KISS/XKISS TNCs on serial ports. It also supports interacting with AGW protocol consumers, and can function as a KISS TNC to AGW bridge or vice versa. It has the ability to copy data from one serial port to another, converting a stack of individually attached serial TNCs to a single XKISS interface. It has the ability to dump packets out at AX.25, all modes of KISS, and just as raw serial data. Further, it supports exporting AX.25 data to pcap. Command line arguments override configuration file directives. It's multi-threaded. That is version 1.0.0.

Version 1.6.2 will perform identically to V1.0.0 with the same configuration file. Verson 1.6.2 introduces a cross-connect capability in the configuration file which permits any to any connections with the exception that they are one-to-one connections.  With a newer-style configuration, One TCP port listener on port 8001 can be connected to one serial port, or one KISS TNC, or one XKISS TNC on a serial port carrying one or more XKISS TNCs interconnected. In this way, it can be used to connect a KISS-aware application to an XKISS stack on a single serial port. Using serial ports, it can convert several standard KISS TNCs into a virtual XKISS TNC running at any standard serial rate, including the extended USB serial port speeds up to 4 MHz. Likewise, any combination of AGW can be cross-connected to KISS, XKISS, or TCP on individual ports. If you want to stack up four TNCs and run four different applications, you can configure rax25kb to listen on 127.0.0.1:8001, 8002, 8003, and 8004 and have each of those correspond to XKISS address 0, 1, 2, and 3 on /dev/USBtty0 or COM1:. Of course, it also has the ability to dump any of those into a log file. Your imagination, CPU, and funding are the only limitations. Version 1.6.2 is also multi-threaded. 

# PyFBB: https://github.com/ke4ahr/PyFBB/
This is a library implementing the BBS Forwarding Protocol standard for amateur radio packet radio BBSs (and Winlink) based off of F6FBB's document on the BBS Forwarding Protocol, then W0RLI's 1998 and 2012 documents, as well as Winlink's BF2 forwarding standard. This library is an attempt to have 100% coverage in the message passing framework in Python. It is somewhat limited as I have other libraries in the works for the pieces it is missing.

My email is my callsign at a common Google product. 

73 (Best Regards), and I look forward to hearing from you. 



# PyFBB
