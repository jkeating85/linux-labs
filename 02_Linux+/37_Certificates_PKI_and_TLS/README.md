# Linux+ Lab 37 — Certificates, PKI, and TLS

---

## Objective

The purpose of this lab was to understand how Public Key Infrastructure (PKI) works by generating cryptographic keys, creating a certificate signing request (CSR), issuing a self-signed certificate, and analyzing certificate details using OpenSSL.

This lab simulates real-world tasks performed by system administrators, cloud engineers, and security professionals when configuring HTTPS and secure communications.

---

## Environment

* Ubuntu Linux (VirtualBox VM)
* Bash Terminal
* OpenSSL Toolkit
* Windows Host Machine
* GitHub Repository (IT_Labs)

---

## Commands Used

| Command                                                                                 | Description                                   |
| --------------------------------------------------------------------------------------- | --------------------------------------------- |
| `sudo apt update`                                                                       | Updates package lists from repositories       |
| `sudo apt install openssl -y`                                                           | Installs OpenSSL for cryptographic operations |
| `openssl genrsa -out private.key 2048`                                                  | Generates a 2048-bit RSA private key          |
| `openssl req -new -key private.key -out request.csr`                                    | Creates a Certificate Signing Request (CSR)   |
| `openssl x509 -req -days 365 -in request.csr -signkey private.key -out certificate.crt` | Generates a self-signed certificate           |
| `ls -l`                                                                                 | Lists files and permissions                   |
| `chmod 600 private.key`                                                                 | Secures the private key by restricting access |
| `openssl x509 -in certificate.crt -text -noout`                                         | Displays certificate details                  |

---

## Command Breakdown Example

### Generating a Private Key

```bash
openssl genrsa -out private.key 2048
```

| Part               | Meaning                      |
| ------------------ | ---------------------------- |
| `openssl`          | Cryptographic toolkit        |
| `genrsa`           | Generates an RSA private key |
| `-out private.key` | Output file name             |
| `2048`             | Key size in bits             |

---

## Workflow

1. Updated system packages using `apt update`
2. Installed OpenSSL
3. Generated a 2048-bit RSA private key
4. Created a Certificate Signing Request (CSR)
5. Entered certificate identity details (Country, State, City, Organization, Common Name)
6. Generated a self-signed certificate valid for 365 days
7. Verified generated files using `ls -l`
8. Secured the private key using proper permissions (`chmod 600`)
9. Inspected certificate contents using OpenSSL

---

## Screenshots and Explanations

### Screenshot 01 — System Update

Updated package lists using apt to ensure the system has the latest repository information before installing OpenSSL.

### Screenshot 02 — OpenSSL Installation

Installed OpenSSL, which is required for generating cryptographic keys and certificates.

### Screenshot 03 — Private Key Generation

Generated a 2048-bit RSA private key using OpenSSL. This key is used for encryption and signing.

### Screenshot 04 — CSR Creation

Created a Certificate Signing Request (CSR) containing identifying information such as country, state, organization, and common name.

### Screenshot 05 — CSR Details Entered

Entered certificate details including location (Illinois, Chicago), organization (IT_Labs), and common name (localhost), which are embedded into the certificate.

### Screenshot 06 — Self-Signed Certificate Creation

Generated a self-signed certificate using the private key and CSR, simulating a Certificate Authority (CA) process.

### Screenshot 07 — Files Created

Verified the creation of:

* private.key (private key)
* request.csr (certificate signing request)
* certificate.crt (self-signed certificate)

### Screenshot 08 — Securing Private Key

Applied `chmod 600` to restrict access to the private key, ensuring only the owner can read and write it. This follows security best practices.

### Screenshot 09 — Certificate Inspection

Used `openssl x509` to inspect the certificate details, including issuer, subject, validity period, and encryption algorithm.

---

## Key Concepts

* **PKI (Public Key Infrastructure):** Framework for managing digital certificates and encryption keys
* **Private Key:** Secret key used for encryption and signing (must be protected)
* **Public Key:** Shared key used for encryption and verification
* **CSR (Certificate Signing Request):** Request sent to a Certificate Authority (CA)
* **Self-Signed Certificate:** Certificate signed by its own private key (used for testing)
* **TLS (Transport Layer Security):** Protocol for secure communication over networks

---

## Real-World Relevance

This lab simulates how HTTPS certificates are created and managed in real environments such as:

* Web servers (Apache, Nginx)
* Cloud platforms (Azure, AWS)
* Kubernetes TLS configurations
* Internal enterprise security systems

Understanding PKI is critical for roles in:

* Cloud Security
* DevOps Engineering
* System Administration
* Cybersecurity

---

## What I Learned

* How to generate cryptographic keys using OpenSSL
* How to create and sign certificate requests
* How certificates are structured and validated
* How to secure sensitive files using Linux permissions
* How to inspect and analyze certificate details

---

## Troubleshooting

### Issue: Directory Not Found

Initially received "No such file or directory" when navigating to the lab folder.
Resolved by verifying the correct path and creating the directory manually.

### Issue: File Permissions Too Open

Private key initially had overly permissive access (`rw-rw-r--`).
Fixed using:

```bash
chmod 600 private.key
```

### Explanation:

Restricting private key access is critical to prevent unauthorized users from accessing sensitive cryptographic material.

---

## Interview Explanation

In this lab, I generated a private RSA key, created a certificate signing request, and issued a self-signed certificate using OpenSSL. I verified the certificate details and secured the private key using strict Linux file permissions. This process simulates how TLS certificates are created and managed in real-world environments.

---
