# SECURITY  
**PAYCHEKX Vulnerability Reporting Policy**

PAYCHEKX takes security and responsible disclosure seriously.

This document explains how to report security vulnerabilities and what to expect in response.

---

## 1. Scope

This policy applies to:

- paychekx.com  
- All PAYCHEKX static pages  
- All tools located under `/tools/`  
- All client-side JavaScript in this repository  

Because PAYCHEKX has:

- No backend  
- No accounts  
- No databases  
- No APIs  

The primary security surface is **client-side code and delivery integrity**.

---

## 2. What to Report

We welcome reports of:

- Cross-site scripting (XSS)
- Injection vulnerabilities
- Open redirects
- Unauthorized access to restricted tools
- Bypass of tier gating logic
- Malicious script injection risks
- Supply chain or hosting configuration issues

We are especially interested in:

- Any way to bypass Single Tool locking  
- Any way to escalate access between tiers  
- Any way to modify or intercept tool logic  

---

## 3. What Not to Report

Please do not report:

- Issues requiring social engineering  
- Theoretical attacks without proof of concept  
- Issues in browsers, operating systems, or third-party services  
- Denial-of-service attempts  
- Automated scanning reports without manual verification  

---

## 4. Responsible Disclosure

If you believe you have found a vulnerability:

1. Do not exploit it beyond proof of concept  
2. Do not disclose it publicly  
3. Do not share it with third parties  

Instead, report it privately as described below.

---

## 5. How to Report

Send a report by email with the following:

- Product: PAYCHEKX  
- Affected URL or file  
- Description of the issue  
- Steps to reproduce  
- Proof of concept (if available)  
- Your contact information  

Send to:

**security@paychekx.com**  
(or your preferred security contact email)

---

## 6. Response Process

We commit to:

- Acknowledge receipt within 5 business days  
- Investigate all credible reports  
- Communicate status updates as appropriate  
- Credit reporters if requested (optional)

We do not operate a bug bounty program at this time.

---

## 7. Safe Harbor

We consider good-faith security research conducted under this policy to be authorized.

We will not pursue legal action against researchers who:

- Follow this policy  
- Act in good faith  
- Avoid privacy violations  
- Avoid service disruption  

---

## 8. Ownership

PAYCHEKX is governed by:

Artificial Intelligence Capital Ventures (AICV)  
Founder: Elijah L. Cooley  

---

Thank you for helping keep PAYCHEKX safe.
