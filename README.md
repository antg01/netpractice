# Netpractice

**System Administration and Networking Practice**

> Solve networking problems and deepen your understanding of IP addressing, subnetting, routers, and more.

---

## 🧠 About

**Net\_Practice** is a project designed to train and assess your understanding of network configuration, IP addressing, subnetting, and the OSI model. It is part of the 42 school curriculum and focuses on identifying and fixing misconfigured networks in a visual environment.

This repository contains personal notes, explanations, and logic used to solve each level of the project. Additionally, you can find a walkthrough guide on my YouTube channel:

---

## 📘 Objectives

* Understand the **TCP/IP model** and **OSI layers**
* Configure **small-scale networks**
* Practice **IP addressing** and **subnetting**
* Differentiate between **routers**, **switches**, and **gateways**
* Solve real-world-like network routing issues

---

## 🤔 Frequently Asked Questions

### 🟢 How does TCP/IP addressing work?

* **TCP/IP** is a suite of communication protocols used to interconnect network devices.
* It's organized into layers:

  * **Application Layer (L7):** Web browsers, email, FTP, etc.
  * **Transport Layer:** Handles ports and segmentation (e.g., TCP, UDP)
  * **Network Layer (L3):** Deals with IP addresses and routing
  * **Data Link & Physical Layers (L1–L2):** Cables, switches, MAC addresses

### 🟢 What is the OSI Model?

* A conceptual framework with 7 layers:

  * **Application, Presentation, Session**
  * **Transport**
  * **Network**
  * **Data Link**
  * **Physical**
* In TCP/IP, **Presentation** and **Session** are part of the Application layer.

---

## 🧑‍💻 Key Concepts

### 🔹 LAN (Local Area Network)

* A network within a limited area (home, office).
* Devices communicate locally and often through a router to the internet.

### 🔹 IP Addressing

* A unique address assigned to each device on a network (e.g., `192.168.1.1`).
* **IPv4** uses 32 bits: `A.B.C.D` format.
* **IPv6** uses 128 bits: hexadecimal notation.

Reserved IPs in any subnet:

* **Network Address** (e.g., `192.168.1.0`)
* **Broadcast Address** (e.g., `192.168.1.255`)
* Usable range: everything in between

---

## 🧩 Subnetting

### What is a Subnet?

* A way to divide a larger network into smaller, manageable pieces.
* Defined by a **subnet mask** (e.g., `255.255.255.0` or `/24`).

### How to Subnet:

1. Convert subnet mask to binary:

   * `255.255.255.0` → `11111111.11111111.11111111.00000000`
2. Count the **1s** = network bits
3. Remaining **0s** = host bits → usable IPs = `2^host_bits - 2`
4. To create multiple subnets:

   * Steal bits from host portion → convert them to **1s**
   * For 4 subnets: need 2 bits → new mask `/26` = `255.255.255.192`

### Example:

To create 4 subnets from `192.168.1.0/24`:

* New mask: `/26` = `255.255.255.192`
* Increments of 64 (2⁶):

  ```
  192.168.1.0     - 192.168.1.63
  192.168.1.64    - 192.168.1.127
  192.168.1.128   - 192.168.1.191
  192.168.1.192   - 192.168.1.255
  ```

---

## 🔁 Reverse Subnetting (Used in NetPractice)

To solve a problem:

1. Convert IP and subnet mask to binary.
2. Identify network and host bits.
3. Calculate subnet ranges using the increment (last network bit).
4. Match IPs to correct ranges.
5. Identify if communication between devices is possible.

---

## 📦 Devices Overview

### 🔸 Switch

* Connects devices within the same LAN.
* Operates at **Layer 2** (Data Link).
* Directs traffic within the LAN using MAC addresses.

### 🔸 Router

* Connects different networks (e.g., LAN to WAN).
* Operates at **Layer 3** (Network).
* Uses IP addresses and routing tables.
* Supports features like NAT and DHCP.

### 🔸 Gateway

* Acts as the bridge between different networks or protocols.
* Often the same device as the router.
* Entry and exit point of the local network.

---

## 🌐 WAN (Wide Area Network)

* A network that spans large geographical areas.
* Connects multiple LANs together.
* Relies on routers, gateways, and public IP addressing.

---

## 🛡 Router Features

To function properly, a router must support:

### 1. **NAT (Network Address Translation):**

* Converts private IPs to public IPs and vice versa.
* Allows multiple devices to share one public IP.

### 2. **FIREWALL:**

* Security rules controlling incoming/outgoing traffic.

### 3. **ROUTING:**

* Determines path for data to travel.
* Utilizes **routing tables** and **next-hop IPs**.

### 4. **DHCP (Optional but common):**

* Assigns IPs dynamically to hosts in the network.

---

## 📎 Point-to-Point Links

* Direct connection between two devices.
* Commonly used between two routers.
* Often uses `/30` subnet (only 2 usable IPs).

---

## 📁 Contents of This Repo

* 🔧 Notes per level of NetPractice
* ❓ Explanations of mistakes and questions asked
* 🧮 Subnetting strategies and binary math breakdowns
* 🖥 YouTube guide for walkthrough and concepts

---

## ✅ How to Use

1. Clone this repository.
2. Review notes for each level.
3. Apply subnetting strategies to fix misconfigured networks.
4. Follow along with the video guide for visual understanding.

---

## 🧠 Credits & Resources

* [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer)
* [IP Calculator](https://www.ip-calculator.io/)
* [Subnetting Made Easy](https://www.youtube.com/watch?v=MrF2sXlgAzI)

---

## 📝 License

This project is for educational purposes.
Feel free to share or adapt with credit.

---
