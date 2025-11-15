
# 1. Link Analysis

### **Displayed Link (what user sees):**
`Track Your Order & Verify Payment`

### **Actual Hyperlink (hidden behind text):**
### Why this link is suspicious:

#### 1. Uses an Untrusted, Fake Domain
- Real Amazon links always start with:
  - https://amazon.in/
  - https://www.amazon.com/
- The link here uses **amaz0n-secure-checkout.xyz**, which is:
  - Not owned by Amazon  
  - Cheap domain extension (.xyz) commonly used in phishing  
  - Contains “amaz0n” with a zero → character substitution attack  

#### 2. Uses HTTP Instead of HTTPS
- No encryption
- Credentials can be stolen (MITM attack)
- Legit Amazon pages always use HTTPS with certificates

#### 3. Suspicious Path `/login`
Typical for:
- Credential harvesting  
- Fake login page  
- Session stealing  

#### 4. Tracking Parameter (`uid=5478123`)
- Attackers use such IDs to track victims  
- Helps verify which users clicked


# 2. Mismatched Link Behavior

The email creates **trust** using brand-like text:
- “Track Your Order”
- “Verify Payment”
- Order number looks real (#5478123)

But actual destination takes user to a **non-Amazon website**.

This intentional mismatch is one of the strongest phishing indicators.


# 3. Attachment Analysis
###  Why this attachment is suspicious:

#### 1. Unexpected Invoice  
User did NOT order anything recently → typical bait.

#### 2. Could Contain Malware  
Attackers often embed:
- Malicious JavaScript in PDFs  
- Exploit payloads  
- Ransomware droppers  
- Fake invoice forms asking for personal data  

#### 3. Used as a Psychological Trick  
The term “invoice” triggers urgency → user opens it without thinking.

#### 4. No legitimate email from Amazon sends invoices as attachments  
Amazon always provides:
- In-app invoice  
- Direct Amazon website link  
Never PDFs from external domains.


# Conclusion

Both the link and attachment in this email show strong phishing indicators:

- Fake domain pretending to be Amazon  
- HTTP instead of HTTPS  
- Credential-stealing `/login` path  
- Tracking parameter  
- Malicious-looking invoice PDF  
