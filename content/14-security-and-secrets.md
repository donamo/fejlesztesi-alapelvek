# 🔐 14 — Security & Secrets Management

> **Magyar:** Biztonság és titokkezelés  
> **Angol:** Security and Secrets Management

---

## 🎯 Lényeg
- 🔑 Ne legyen secret a kódban
- 🛡️ Least privilege
- 🔁 Rotálható kulcsok

## 🧱 Területek
- AuthN / AuthZ
- API kulcsok, tokenek
- TLS, titkosítás
- Secrets storage (Vault, AWS SM)

## ❌ Anti-pattern
- ❌ Jelszó a config file-ban
- ❌ Jelszó a Git-ben

## ✅ Best practice
- ✅ Secrets manager
- ✅ IAM role-ok
- ✅ Auditált hozzáférés

## 📋 Checklist
- [ ] Nincs secret repo-ban
- [ ] Secrets manager használva
- [ ] Least privilege elv

---
