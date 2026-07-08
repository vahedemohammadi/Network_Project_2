# Phase 3 Detailed Report: Server Response and RTT Analysis

## Project Information

- **Student Name:** Vahedeh Mohamadi
- **Student ID:** 40217023166
- **Course:** Computer Networks
- **Topic:** HTTP Response Analysis, Status Code Examination, and Round Trip Time (RTT) Measurement

---

# 1. Introduction and Objectives

In the previous phases, the HTTP **GET** request and the protocol headers across the TCP/IP layers were analyzed.

The objective of this phase is to examine the HTTP response received from the web server, extract and analyze the HTTP **Status Code**, accurately measure the **Application Layer Round Trip Time (RTT)**, and investigate the possible causes of communication delays from a network engineering perspective.

---

# 2. HTTP Response Packet Analysis

To locate the HTTP response packet in Wireshark, the following display filter was used:

```text
http.response.code == 200
```