
## 1. Suspicious Sending IP Address
**IP:** 185.203.112.14  
- Not associated with Amazon or AWS.
- Belongs to a foreign hosting provider commonly abused for phishing.
- Amazon legitimate mail IPs belong to AWS SES ranges.

This is the **first strong phishing indicator**.

---

## 2. SPF Failure (Softfail)
- The domain **amaz0n-support.com** does NOT authorize this IP to send emails.
- Softfail is triggered when the sender server is not listed in SPF records.

Meaning: the sender is NOT authentic.

---

## 3. DKIM Missing (dkim=none)
- Legit emails from Amazon always include DKIM signatures.
- Missing DKIM = unauthenticated sender.

Another **major indicator of spoofing**.

---

## 4. DMARC Failure
- DMARC policy of amaz0n-support.com rejects the email.
- This means the domain *itself* is signaling that the header is fake or spoofed.

---

## 5. Mismatch Between From & Reply-To
**From:** order-update@amaz0n-support.com  
**Reply-To:** support@amazon.com  

This mismatch is intentional:
- The attacker wants replies to go to a real-looking address.
- This is a classic tactic to evade detection.

---

## 6. “Received” Chain Shows Anomalies
Problems:
- The server resolves as **unknown**, meaning the IP has no reverse DNS.
- Legit providers always configure reverse DNS.

---

## 7. Timezone & Timestamp Inconsistencies
- Header timestamp matches local time but originating server location (Europe/Eastern Europe) does not.
- Typical of phishing servers hosted on offshore VPS.

---

## Conclusion
The email header contains multiple high-severity phishing indicators:

- Unauthorized sending IP  
- SPF softfail  
- DKIM missing  
- DMARC fail  
- Domain spoofing  
- Reply-To mismatch  
- Untrusted host with no rDNS  