# Task 5: Capture and Analyze Network Traffic Using Wireshark

This repository contains the deliverables for Task 5 of the Elevate Labs Cyber Security Internship , which involved capturing and analyzing network traffic using Wireshark.

## Task Objective

The objective of this task was to capture live network packets and identify basic protocols and traffic types. This provides hands-on packet analysis skills and protocol awareness.

## Tools Used

* **Wireshark**: A free and open-source packet analyzer.

## Process Followed

1.  **Installed Wireshark**.
2.  **Started packet capture** on the active network interface (e.g., Wi-Fi/Ethernet).
3.  **Generated network traffic** by:
    * Browse the website `http://neverssl.com` to generate HTTP traffic.
    * This also inherently generated DNS (for domain resolution) and TCP (as HTTP's underlying transport protocol) traffic.
4.  **Stopped the capture** after a sufficient amount of traffic was gathered (approximately one minute).
5.  **Filtered captured packets** by protocol to analyze specific traffic types (e.g., HTTP, DNS, TCP).
6.  **Identified** several different protocols within the capture.
7.  **Exported the capture** as a `.pcapng` file.
8.  **Summarized the findings** in this report.

## Protocols Identified

At least three different protocols were identified in the capture:

1.  **HTTP (Hypertext Transfer Protocol):**
    * **Description:** The foundation of data communication for the World Wide Web. It's an application layer protocol used for transmitting hypermedia documents, such as HTML.
    * **Observation:** HTTP traffic was observed when accessing `neverssl.com`. This included GET requests from the client (my browser) to the server and OK responses from the server.

2.  **DNS (Domain Name System):**
    * **Description:** A hierarchical and decentralized naming system used to identify computers, services, and other resources reachable through the Internet or other Internet Protocol networks. It translates human-readable domain names (like `neverssl.com`) into machine-readable IP addresses.
    * **Observation:** DNS queries and responses were observed when my browser first tried to resolve the IP address for `neverssl.com` and other resources the site might have loaded.

3.  **TCP (Transmission Control Protocol):**
    * **Description:** One of the main protocols of the Internet protocol suite. It provides reliable, ordered, and error-checked delivery of a stream of octets (bytes) between applications running on hosts communicating via an IP network. HTTP and many other application protocols rely on TCP.
    * **Observation:** TCP segments were observed handling the setup (three-way handshake), data transmission (for HTTP), and teardown of connections to the `neverssl.com` server.

## Deliverables

* **Packet Capture File:**
    * [`capture.pcapng`](./capture.pcapng) (This file contains all the captured network packets).
* **Report:** This `README.md` file summarizes the findings and packet details.
* **Screenshots:**
    * DNS Capture: [`dns_capture.png`](./dns_capture.png)
    * TCP Capture: [`tcp_capture.png`](./tcp_capture.png)
    * HTTP Capture: [`http_capture.png`](./http_capture.png)
    * Website Used: [`Neverssl_site.jpg`](./Neverssl_site.png)

## Key Learnings

This task provided valuable hands-on experience with Wireshark for packet capture and analysis. It helped in understanding how different protocols interact to enable internet communication and reinforced the importance of packet analysis in network troubleshooting and security.

---
