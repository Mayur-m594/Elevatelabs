**Sender Name:**  "Amazon Support"  
**Sender Email:**  order-update@amaz0n-support.com

## Suspicious Domain Name
- The domain **amaz0n-support.com** is NOT an official Amazon domain.
- It replaces the letter **“o”** with **“0”** (zero), a common phishing trick.
- Legit Amazon domains include:
  - amazon.com
  - amazon.in
  - amazon.co.uk

The use of a lookalike domain indicates **domain spoofing**.

---

## Mismatched “From” vs “Reply-To”
- **From:** order-update@amaz0n-support.com  
- **Reply-To:** support@amazon.com  

This mismatch is a major red flag.  
Attackers often use a fake “From” but a legitimate-looking “Reply-To” to bypass simple checks.

---

## No Indicators of Valid SPF/DKIM/DMARC
(Assuming typical phishing behavior)

- The sender domain **amaz0n-support.com** is unlikely to have valid:
  - **SPF** (Sender Policy Framework)
  - **DKIM** (DomainKeys Identified Mail)
  - **DMARC** policies  
- Without these email authentication protocols, the message is highly suspicious.

---

## Untrusted Domain Age
Phishing domains are usually:
- Very new
- Registered for cheap
- Lack legitimate DNS records

Names like **amaz0n-support.com** are often created solely for phishing campaigns.

---

## Suspicious Formatting in Display Name
- Display Name: **“Amazon Support”**
- But domain is not tied to Amazon.

Attackers rely on the display name to trick users while hiding the fake domain.

---

## ✔ Conclusion
The sender address **order-update@amaz0n-support.com** shows multiple phishing indicators:
- Spoofed domain
- Domain impersonation using character substitution
- Mismatch between From and Reply-To
- No authentication records
- Fake branding
