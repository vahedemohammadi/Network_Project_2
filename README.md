# Network Project 2

## HTTP Traffic Analysis using Wireshark and cURL

---

## Student Information

**Name:** Vahedeh Mohamadi

**Student ID:** 40217023166

**Course:** Computer Networks

---

## Project Description

This project analyzes HTTP communication using Wireshark and cURL. HTTP packets are generated, captured, filtered, and analyzed according to the TCP/IP protocol stack.

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
│   └── phase1
│       ├── image1_capture.png
│       ├── image2_curl_commands.png
│       ├── image3_http_get_details.png
│       ├── image4_http_request_capture.png
│       └── image5_http_response_200_ok.png
│
├── report
│   └── phase1_report.md
│
└── README.md
```

---

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