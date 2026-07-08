# گزارش فاز اول

## هدف

هدف از این فاز، تولید ترافیک HTTP با استفاده از ابزار **cURL** و ضبط آن توسط نرم‌افزار **Wireshark** است تا بسته‌های شبکه برای تحلیل در مراحل بعدی ثبت شوند.

---

## ابزارهای مورد استفاده

- Wireshark
- cURL
- خط فرمان ویندوز (Windows Command Prompt)

---

## مراحل انجام کار

### مرحله ۱

نرم‌افزار **Wireshark** اجرا شد و فرآیند ضبط بسته‌های شبکه (Packet Capture) بر روی رابط شبکه فعال (Wi-Fi) آغاز گردید.

### مرحله ۲

به‌منظور تولید ترافیک HTTP، دستورات زیر در محیط **Command Prompt** اجرا شدند:

```bash
curl http://example.com
curl http://neverssl.com
```

### مرحله ۳

پس از ارسال درخواست‌ها، فرآیند ضبط بسته‌ها متوقف شد و فایل Capture با فرمت **PCAPNG** ذخیره گردید.

### مرحله ۴

برای مشاهده و جداسازی بسته‌های مربوط به درخواست‌های HTTP، از فیلتر زیر در نرم‌افزار Wireshark استفاده شد:

```text
http.request
```

### مرحله ۵

در نهایت، درخواست **HTTP GET** و پاسخ دریافتی از سرور (**HTTP 200 OK**) مورد بررسی و تحلیل قرار گرفتند.

---

## فایل‌های ایجاد شده

### فایل ضبط ترافیک (Capture)

```
captures/phase1_capture.pcapng
```

### تصاویر

```
images/phase1/image1_capture.png
images/phase1/image2_curl_commands.png
images/phase1/image3_http_get_details.png
images/phase1/image4_http_request_capture.png
images/phase1/image5_http_response_200_ok.png
```

---

## نتیجه‌گیری

در این فاز، ترافیک **HTTP** با موفقیت توسط ابزار **cURL** تولید و با استفاده از نرم‌افزار **Wireshark** ضبط شد. سپس درخواست **HTTP GET** و پاسخ سرور (**HTTP 200 OK**) شناسایی و تحلیل شدند. نتایج این مرحله، مبنای بررسی دقیق‌تر هدرهای پروتکل و تحلیل لایه‌های مختلف شبکه در فازهای بعدی پروژه را فراهم کرد.