# CryptoCred

CryptoCred is a Flask-based academic web application for secure digital credential issuance and verification. It was built for a Cryptography and Network Security AAT/CRP project and demonstrates both:

- `Cryptanalysis`
- `Contemporary cryptography`

The system focuses on one real-world problem: digital certificates can be copied, visually edited, forged, or shared as screenshots, making visual inspection alone unreliable for trust verification.

## Problem Solved

CryptoCred helps an issuer generate event or academic credentials that can later be verified as:

- `Valid`
- `Tampered`
- `Revoked`
- `Unknown`

It does this using:

- random non-sequential credential IDs
- an educational manual hash
- manual RSA digital signatures
- hidden verification payloads
- BMP LSB-style steganographic embedding
- verifier-side revocation and integrity checks

## Teacher Requirement Mapping

### 1. Cryptanalysis

Implemented through:

- Caesar brute-force attack
- predictable credential ID attack
- weak hidden payload attack demonstration

### 2. Contemporary Cryptography

Implemented through:

- educational hash-based integrity verification
- manual RSA digital signatures
- hidden verification payload extraction and verification

## Tech Stack

- `Python`
- `Flask`
- `HTML`
- `CSS`
- `Local JSON storage`

No external crypto libraries are used. The project manually implements the required cryptographic logic for explainability during viva.

## Core Features

- Dashboard with project overview and status counters
- Cryptanalysis Lab
- Batch Credential Issuer
- Certificate Generator
- Invisible Payload / Steganography module
- Credential Verification Portal
- Tamper Detection Demo
- Revocation Management
- Results / Test Cases page
- About / Documentation page

## Cryptographic Methods Used

### Classical / Cryptanalysis Layer

- Caesar cipher encryption, decryption, and brute-force recovery
- predictable sequential identifier attack analysis

### Integrity and Authenticity Layer

- educational deterministic hash
- RSA private-key signing
- RSA public-key verification

### Hidden Verification Layer

- hidden payload construction
- redundant payload copies
- BMP least-significant-bit style embedding
- BMP payload extraction

## Project Structure

```text
CryptoCred/
├── app.py
├── README.md
├── REVIEW_NOTES.md
├── crypto/
│   ├── caesar.py
│   ├── hash_engine.py
│   └── rsa_signature.py
├── services/
│   ├── credential_service.py
│   ├── payload_service.py
│   ├── stego_service.py
│   ├── storage.py
│   └── test_service.py
├── templates/
├── static/
├── data/
├── Report_Images/
└── tools/
