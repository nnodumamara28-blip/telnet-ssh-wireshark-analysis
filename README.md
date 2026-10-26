# Lab: Examining Telnet and SSH in Wireshark

## Objective
Capture Telnet and SSH sessions with Wireshark and compare how each protocol
handles data in transit.

## Environment
- Kali Linux: Telnet and SSH servers installed, started and enabled
- CyberOps Workstation VM: client, with Wireshark capturing on the network interface

## Part 1: Telnet
Connected to the Kali Telnet server, captured the traffic, filtered with `telnet`
and used Follow > TCP Stream.

**Finding:** The whole session, including the username and password, is readable
plaintext.

## Part 2: SSH
Connected to the Kali SSH server, captured the traffic, filtered with `ssh` and
used Follow > TCP Stream.

**Finding:** After the key exchange, the data is encrypted and unreadable.

## Reflection: Why is SSH preferred over Telnet?
Telnet sends everything, including credentials and commands, in plaintext, so
anyone who can sniff the traffic can read or hijack the session. SSH encrypts
the session, authenticates the server with host keys, and protects data
integrity, which makes it safe on untrusted networks.

## Screenshots
## Captures
Raw Wireshark files are in the `captures/` folder.
