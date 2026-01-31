# ⚙️ 03 — Config (Configuration) — 12-Factor App

> **Angol:** Config — Store config in the environment  
> **Magyar:** Konfiguráció — A konfigurációt környezeti változókban tárold
> **Kategória:** Alkalmazás-alapelvek & Cloud-native működés

---

## 🎯 Lényeg
- 🔐 Ne legyen secret a kódban
- 🧪 Dev / test / prod csak **configban** különbözzön
- 🔁 Ugyanaz a build több környezetben

## 🧱 Mi számít config-nak?
- 🌐 DB host, port, user
- 🔑 API kulcsok, tokenek
- 🚩 Feature flag-ek
- ⚙️ Timeoutok, limitek

## ❌ Anti-pattern
- ❌ Hardcode-olt jelszavak
- ❌ Környezetfüggő if-ek a kódban

## ✅ Best practice
- ✅ ENV változók
- ✅ Secrets manager (Vault, AWS SM)
- ✅ Config server

## 🚀 CI/CD
- Pipeline adja be a configot
- Image ugyanaz, csak ENV más

## 📋 Checklist
- [ ] Nincs secret a kódban
- [ ] ENV-ből jön minden config
- [ ] Feature flag támogatott

---

## 📚 Forrás
- https://12factor.net/config
