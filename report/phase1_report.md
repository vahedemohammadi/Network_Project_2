# Phase 1 Report

## Objective

The objective of this phase is to generate **HTTP** traffic using the **cURL** command-line tool and capture the generated packets with **Wireshark**. The captured packets will be used for detailed analysis in the subsequent phases of the project.

---

## Tools Used

- Wireshark
- cURL
- Windows Command Prompt

---

## Procedure

### Step 1

The **Wireshark** application was launched, and packet capturing was started on the active network interface (Wi-Fi).

### Step 2

To generate HTTP traffic, the following commands were executed in the **Windows Command Prompt**:

```bash
curl http://example.com
curl http://neverssl.com
```

### Step 3

After the HTTP requests were sent successfully, the packet capture process was stopped, and the captured traffic was saved as a **PCAPNG** file.

### Step 4

To identify and isolate HTTP request packets, the following display filter was applied in **Wireshark**:

```text
http.request
```

### Step 5

Finally, the captured **HTTP GET** request and the corresponding **HTTP/1.1 200 OK** server response were examined and analyzed.

---

## Generated Files

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

---

## Conclusion

In this phase, **HTTP** traffic was successfully generated using **cURL** and captured with **Wireshark**. The captured traffic included an **HTTP GET** request and its corresponding **HTTP/1.1 200 OK** response, both of which were successfully identified and analyzed. The results obtained in this phase provide the foundation for detailed protocol header analysis and TCP/IP layer examination in the subsequent phases of the project.