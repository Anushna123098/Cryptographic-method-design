# 🔐 Secure Communication Using Hybrid Cryptography

This Python project demonstrates a **secure communication protocol** using a **hybrid cryptography** approach—combining **RSA (asymmetric encryption)** for securely sharing an AES key, and **AES (symmetric encryption)** for fast and secure message encryption. It also integrates **digital signature generation and verification** using RSA to ensure message authenticity.

---

## 🛠️ Technologies Used

- **Python 3**
- [PyCryptodome](https://pypi.org/project/pycryptodome/) (for AES, RSA, hashing, and signature)
- Base64 (for encoding outputs)

---

## 🔐 Cryptographic Workflow

### 1. **RSA Key Generation**
- A 2048-bit RSA key pair is generated.
- The public key is used for encryption; the private key for decryption and signing.

### 2. **AES Key Generation**
- A 16-byte AES key is created using a secure random generator.

### 3. **Hybrid Encryption**
- The AES key is encrypted using the **RSA public key** (asymmetric encryption).
- The actual message is encrypted using **AES in EAX mode** (symmetric encryption).

### 4. **Digital Signature**
- The original message is signed using the **RSA private key** and **SHA256 hashing** to ensure integrity and authenticity.

### 5. **Decryption & Signature Verification**
- The encrypted AES key is decrypted using the RSA private key.
- The encrypted message is decrypted using the AES key.
- The digital signature is verified using the RSA public key.

