# Phase 4 Detailed Report: HTTPS and TLS Handshake Analysis

## Student Information

- **Student Name:** Vahedeh Mohamadi
- **Student ID:** 40217023166
- **Course:** Computer Networks

---

# 1. Introduction and Objectives

The objective of this bonus phase is to examine the **Transport Layer Security (TLS)** protocol used in secure web communications. This phase focuses on analyzing the **TLS Handshake** process initiated when accessing a website over **HTTPS** using the command:

```bash
curl https://example.com
```

Additionally, this phase explains why HTTP headers and message contents cannot be viewed as **plain text** after encryption has been established.

---

# 2. Executed Command and Wireshark Display Filter

To generate secure HTTPS traffic, the following command was executed:

```bash
curl https://example.com
```

After capturing the network traffic, the following Wireshark display filter was applied to isolate TLS packets:

```text
tls
```

---

# 3. TLS Handshake Analysis

Based on the captured packets exchanged with **example.com** (Server IP: **188.114.99.0**), the following key handshake messages were identified:

| Frame | Message Type | Source Address | Destination Address | Technical Description |
|-------|--------------|----------------|---------------------|-----------------------|
| **Frame 26** | **Client Hello** | 192.168.1.12 | 188.114.99.0 | The client initiates the secure connection by sending the supported TLS versions, cipher suites, extensions, and the Server Name Indication (SNI) for **example.com**. |
| **Frame 28** | **Server Hello** | 188.114.99.0 | 192.168.1.12 | The server selects the TLS version and cipher suite, then sends its digital certificate to authenticate its identity. |

---

# 4. Why Are HTTP Headers Not Visible as Plain Text?

In the standard **HTTP** protocol, all request headers (such as **Host**, **User-Agent**, and **Cookie**) and the message body are transmitted as **plain text**. Anyone capable of capturing the network traffic can read this information.

In contrast, **HTTPS** provides secure communication through the **TLS** protocol.

The encryption process works as follows:

1. TLS is placed between the **TCP Transport Layer** and the **HTTP Application Layer**.
2. During the **TLS Handshake**, the client and server exchange the **Client Hello** and **Server Hello** messages and securely establish shared encryption keys.
3. After the handshake is completed, all HTTP requests and responses are encrypted and transmitted as **TLS Application Data**.
4. Consequently, HTTP headers and message contents become encrypted (**ciphertext**) and are no longer visible in plain text. Wireshark—or any network observer—can only display encrypted data unless the corresponding session keys are available.

---

# 5. Conclusion

In this phase, a secure HTTPS connection was successfully established and captured using Wireshark.

The key **TLS Handshake** messages (**Client Hello** and **Server Hello**) were identified and analyzed, providing a practical understanding of how TLS establishes a secure communication channel.

Furthermore, this phase demonstrated why HTTP headers and application data are encrypted after the handshake process, ensuring confidentiality, integrity, and authentication during secure web communication.