# Task-2-Analyze-a-Phishing-Email-Sample.
Case study on phishing email detection with header analysis
##  Phishing Email Analysis – Case Study

###  Summary
This case study analyzes a real phishing email impersonating a Brazilian bank (Bradesco) and reward program (Livelo). The message aims to trick the user into clicking a malicious link by creating urgency around expiring reward points.

---

###  Email Header Analysis

| Field | Value |
|-------|-------|
| **From** | BANCO DO BRADESCO LIVELO `<banco.bradesco@atendimento.com.br>` |
| **Delivered-To** | padmanathan19505@gmail.com |
| **Return-Path** | `<padmanathan19505@gmail.com>` |
| **Received from** | `ubuntu-s-1vcpu-1gb-35gb-intel-sfo3-06` (IP: `137.184.34.4`) via Postfix |
| **Email Provider** | DigitalOcean (Cloud VPS) |
| **SPF** | `temperror` |
| **DKIM** | `none` |
| **DMARC** | `temperror` |
| **Date** | Wed, 16 Jul 2025 00:26:03 -0700 (PDT) |

### ⚠️ Phishing Indicators

- **Fake Domain**: `atendimento.com.br` is not associated with Bradesco or Livelo.
- **IP Origin**: Sent from a cloud-hosted VPS (DigitalOcean), not an official email server.
- **Authentication Failures**:
  - SPF: `temperror`
  - DKIM: `none`
  - DMARC: `temperror`
- **Urgency Tactic**:
  - Subject claims: `Seu cartão tem 92.990 pontos LIVELO expirando hoje!`  
    *(Your card has 92,990 Livelo points expiring today!)*

### Conclusion

This email is **a phishing attempt**. It uses urgency, spoofed sender addresses, and unauthorized mail servers to deceive recipients into clicking potentially harmful links.

###  Recommendation and Prevention

- Do **not** click on any links or attachments.
- Report the email as **phishing** to your email provider.
- Use this as a training sample for phishing detection systems or awareness campaigns.

