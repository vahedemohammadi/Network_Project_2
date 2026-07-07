# Phase 1 Report

## Objective

The objective of this phase is to generate HTTP traffic using cURL and capture it using Wireshark.

---

## Tools

- Wireshark
- cURL
- Windows Command Prompt

---

## Procedure

### Step 1

Started packet capture on the active Wi-Fi interface using Wireshark.

### Step 2

Generated HTTP traffic using the following commands:

```bash
curl http://example.com
curl http://neverssl.com
```

### Step 3

Stopped packet capture and saved the capture file.

### Step 4

Filtered HTTP packets using:

```text
http.request
```

### Step 5

Analyzed the HTTP GET request and HTTP response (200 OK).

---

## Files

### Capture

```
captures/phase1_capture.pcapng
```

### Images

```
images/phase1/image1_capture.png
images/phase1/image2_curl_commands.png
images/phase1/image3_http_get_details.png
images/phase1/image4_http_request_capture.png
images/phase1/image5_http_response_200_ok.png
```

---

## Result

HTTP traffic was successfully generated using cURL.

The HTTP GET request and the HTTP response were captured and analyzed successfully using Wireshark.