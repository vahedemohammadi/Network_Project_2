# Network Project 2

## HTTP Traffic Analysis using Wireshark and cURL

---

## Student Information

**Name:** Vahedeh Mohamadi

**Student ID:** 40217023166

**Course:** Computer Networks

---

## Project Description

This project analyzes HTTP communication using Wireshark and cURL. HTTP packets are generated, captured, filtered, and analyzed according to the TCP/IP protocol stack. The project consists of multiple phases, including packet capture, protocol header analysis, and network communication inspection.

---

## Tools

- Wireshark
- cURL
- Windows Command Prompt
- Git
- GitHub

---

## Project Structure

```text
Network_Project_2
│
├── captures
│   └── phase1_capture.pcapng
│
├── images
│   ├── phase1
│   │   ├── image1_capture.png
│   │   ├── image2_curl_commands.png
│   │   ├── image3_http_get_details.png
│   │   ├── image4_http_request_capture.png
│   │   └── image5_http_response_200_ok.png
│   │
│   └── phase2
│       ├── image1_http_filter.png
│       ├── image2_http_get_request.png
│       ├── image3_application_layer.png
│       ├── image4_transport_layer.png
│       └── image5_network_layer.png
│
├── report
│   ├── phase1_report.md
│   └── phase2_report.md
│
└── README.md
```

---

# Phase 1

## Phase 1 Objectives

- Capture HTTP traffic using Wireshark.
- Generate HTTP traffic using cURL.
- Save the captured packets.
- Analyze HTTP GET requests.
- Analyze HTTP 200 OK responses.

---

## Commands Used

```bash
curl http://example.com
curl http://neverssl.com
```

---

## Wireshark Display Filters

```text
http.request
```

```text
http.response
```

```text
http
```

```text
tcp.port == 80
```

---

## Files

### Capture File

```text
captures/phase1_capture.pcapng
```

### Images

```text
images/phase1/image1_capture.png
images/phase1/image2_curl_commands.png
images/phase1/image3_http_get_details.png
images/phase1/image4_http_request_capture.png
images/phase1/image5_http_response_200_ok.png
```

### Report

```text
report/phase1_report.md
```

---

## Result

HTTP traffic was successfully generated using cURL and captured using Wireshark. The HTTP GET request and the HTTP response (200 OK) were identified successfully. The captured packets are ready for further analysis in the next phase.

---

# Phase 2

## Phase 2 Objectives

- Apply HTTP display filters in Wireshark.
- Locate the first HTTP GET request.
- Analyze the Application, Transport, and Network layers.
- Extract protocol header information.
- Understand the encapsulation of HTTP over TCP/IP.

---

## Wireshark Display Filter

```text
http
```

or

```text
tcp.port == 80
```

---

## Packet Analysis

### Application Layer (HTTP)

| Field | Value |
|------|------|
| HTTP Method | GET |
| HTTP Version | HTTP/1.1 |
| Host | neverssl.com |
| User-Agent | curl/8.13.0 |

### Analysis

The captured packet is an HTTP GET request generated using the **cURL** command-line tool. The request uses **HTTP/1.1**, and the **Host** header specifies the destination server (**neverssl.com**). The **User-Agent** header identifies the client application as **curl version 8.13.0**.

---

### Transport Layer (TCP)

| Field | Value |
|------|------|
| Protocol | TCP |
| Source Port | 10840 |
| Destination Port | 80 |

### Analysis

The communication uses the **Transmission Control Protocol (TCP)**. The source port (**10840**) is a temporary client port automatically assigned by the operating system, while the destination port (**80**) is the standard port for HTTP communication.

---

### Network Layer (IPv4)

| Field | Value |
|------|------|
| Source Address | 192.168.1.12 |
| Destination Address | 34.223.124.45 |

### Analysis

The source IP address (**192.168.1.12**) belongs to the client machine within the local network. The destination IP address (**34.223.124.45**) belongs to the remote web server hosting **neverssl.com**. IPv4 is responsible for routing packets between the client and the server.

---

## Images

```text
images/phase2/image1_http_filter.png
images/phase2/image2_http_get_request.png
images/phase2/image3_application_layer.png
images/phase2/image4_transport_layer.png
images/phase2/image5_network_layer.png
```

---

## Report

```text
report/phase2_report.md
```

---

## Phase 2 Result

The HTTP packet was successfully analyzed using Wireshark. Header information from the Application, Transport, and Network layers was extracted and examined. The analysis demonstrates how an HTTP request is encapsulated within the TCP/IP protocol stack and transmitted from the client to the destination web server.

---

## Conclusion

The first two phases of this project demonstrate the complete process of generating, capturing, filtering, and analyzing HTTP traffic. Phase 1 focused on packet capture, while Phase 2 examined the protocol headers across different TCP/IP layers. These activities provide a practical understanding of network communication and protocol encapsulation using Wireshark and cURL.