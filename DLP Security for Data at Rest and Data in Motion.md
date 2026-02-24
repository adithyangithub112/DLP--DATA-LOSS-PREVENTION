## DLP Security for Data at Rest and Data in Motion

DLP protects sensitive information in two major states:

1. Data at Rest
2. Data in Motion

Below is a structured explanation of how DLP secures both.

---

# 1. DLP for Data at Rest

Data at Rest refers to data stored on:

□ Laptops and desktops

□ File servers

□ Databases

□ Cloud storage

□ USB drives

This is primarily handled by **Endpoint DLP (EDLP)** and Storage DLP.

---

## 1.1 Objectives

○ Prevent unauthorized copying of sensitive files

○ Stop data theft via USB devices

○ Enforce encryption policies

○ Detect unauthorized file access

○ Protect classified documents

---

## 1.2 How DLP Protects Data at Rest

○ File content scanning

○ Pattern matching (credit card, ID numbers)

○ File fingerprinting

○ Monitoring file access and modification

○ Blocking copy to removable media

○ Restricting printing or screenshot capture

○ Enforcing encryption before transfer

---

## 1.3 Example Scenario

1. Employee tries to copy payroll.xlsx to a USB device
2. DLP agent scans the file
3. Sensitive data is detected
4. Transfer is blocked
5. Alert is sent to SIEM
6. SOC investigates

---

## 1.4 Control Type

□ Preventive Control (blocks unauthorized transfer)

□ Detective Control (alerts SOC on violations)

---

# 2. DLP for Data in Motion

Data in Motion refers to data being transmitted through:

□ Web uploads

□ Email systems

□ Cloud applications

□ FTP transfers

□ API communications

This is handled by **Network DLP (NDLP)** and Email DLP.

---

## 2.1 Objectives

○ Prevent data exfiltration over the internet

○ Stop accidental email leaks

○ Block unauthorized cloud uploads

○ Monitor outbound network traffic

○ Ensure secure communication

---

## 2.2 How DLP Protects Data in Motion

○ Deep Packet Inspection (DPI)

○ Outbound traffic monitoring

○ Email content scanning

○ Attachment inspection

○ Policy-based blocking

○ Automatic email encryption

○ SSL/TLS traffic inspection (in enterprise setups)

---

## 2.3 Example Scenario

1. User uploads financial data to personal cloud storage
2. Network DLP inspects outbound traffic
3. Sensitive patterns are detected
4. Upload is blocked
5. Alert is generated
6. SOC investigates possible insider threat

---

## 2.4 Control Type

□ Preventive Control (blocks transmission)

□ Detective Control (generates alert for SOC)

---

# 3. Comparison: Data at Rest vs Data in Motion

| Category | Data at Rest | Data in Motion |
| --- | --- | --- |
| Location | Stored on device/server | Being transmitted over network |
| DLP Type | Endpoint DLP | Network / Email DLP |
| Risk | USB theft, local copy | Cloud upload, email leak |
| Inspection | File system monitoring | Traffic inspection |
| Main Threat | Insider copying data | Data exfiltration over network |

---

# 4. SOC Perspective

In SOC operations:

□ Data at Rest DLP focuses on insider misuse at endpoints

□ Data in Motion DLP focuses on exfiltration detection

□ Both generate alerts to SIEM

□ Analysts investigate policy violations

---

# Final Summary

DLP protects:

1. Data at Rest → Through Endpoint and Storage monitoring
2. Data in Motion → Through Network and Email inspection

Together, they provide complete data exfiltration protection within an organization.
