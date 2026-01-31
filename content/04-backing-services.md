# 🔌 04 — Backing Services — 12-Factor App

> **Angol:** Treat backing services as attached resources  
> **Magyar:** Háttérszolgáltatások kezelése csatolt erőforrásként
> **Kategória:** Alkalmazás-alapelvek & Cloud-native működés

---

## 🎯 Lényeg
- 🗄️ DB, cache, MQ = cserélhető erőforrás
- 🔁 Konfigból jön az endpoint
- 🧱 Ne legyen hardcode

## 🧱 Példák
- PostgreSQL, Redis, Kafka, S3

## ❌ Anti-pattern
- ❌ Kódba égetett connection string
- ❌ Környezetfüggő build

## ✅ Best practice
- ✅ URL ENV-ből
- ✅ Könnyen cserélhető service

## 📋 Checklist
- [ ] Minden backing service configból jön
- [ ] Könnyen cserélhető
- [ ] Nincs hardcode

---

## 📚 Forrás
- https://12factor.net/backing-services
