# she-m1m2m3m4m5-calculator
SHE (Secure Hardware Extension) M1–M5 key update calculator with AES-128-CMAC (RFC4493) and ECU validation support.

# 🔐 SHE M1–M5 Key Update Calculator

A professional tool to generate and validate **SHE (Secure Hardware Extension)** key update messages (M1, M2, M3, M4, M5) based on the HIS specification.

---

## 🚀 Features

- ✅ Full M1–M5 generation
- ✅ AES-128 ECB, CBC, and CMAC (RFC 4493 compliant)
- ✅ Supports real ECU validation (M4/M5 comparison)
- ✅ Counter + FID bit-level packing
- ✅ Clean UI for testing and debugging
- ✅ Ready for automotive security workflows

---

## 🧠 Protocol Overview

SHE key update uses 5 message blocks:
M1 → Identity (UID, ID, AuthID)
M2 → Encrypted new key (AES-CBC)
M3 → Authentication MAC (AES-CMAC)
M4 → Proof of update (AES-ECB with NewKey)
M5 → MAC over M4 (AES-CMAC)


---

## 🔑 Cryptography Used

- AES-128-ECB
- AES-128-CBC (IV = 0)
- AES-128-CMAC (RFC 4493)

---

## 🧪 Validation Mode

You can compare generated values with ECU output:

- Input ECU M4/M5
- Tool shows:
  - ✅ MATCH
  - ❌ MISMATCH

Useful for:
- ECU bring-up
- SHE integration testing
- Debugging key update failures

---

## 🚗 Supported Platforms

- :contentReference[oaicite:0]{index=0}  
- :contentReference[oaicite:1]{index=1}  
- :contentReference[oaicite:2]{index=2}  

---

## 📦 Use Cases

- Secure key provisioning (EOL)
- SecOC key injection
- Secure boot key updates
- OTA key rotation
- Automotive cybersecurity validation

---

## ⚠️ Important Notes

- All inputs must be HEX format
- UID = 120 bits (30 hex chars)
- Keys = 128 bits (32 hex chars)
- Counter = 28-bit value

---

## 💡 Why This Tool?

This tool is designed to:

- Bridge **theory ↔ real ECU implementation**
- Help engineers debug SHE key update failures
- Provide a **practical understanding of M1–M5 protocol**

---

## 🔥 Author

Embedded Software Engineer | Automotive Cybersecurity  
Focused on secure boot, cryptography, and HSM/SHE systems

---

## 📜 License

MIT License
