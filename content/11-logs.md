# 📜 11 — Logs — 12-Factor App

> **Angol:** Treat logs as event streams  
> **Magyar:** A logokat eseményfolyamként kezeld
> **Kategória:** Observability, Monitoring & Láthatóság

---

## 🎯 Lényeg
- 📤 App stdout-ra ír
- 🗂️ Környezet gyűjti
- 🔍 Központilag kereshető

## ❌ Anti-pattern
- ❌ File-ba logolás appból
- ❌ Saját log rotáció

## ✅ Best practice
- ✅ STDOUT
- ✅ Central log (ELK, Loki)
- ✅ Strukturált log

## 📋 Checklist
- [ ] Nincs file log
- [ ] STDOUT logging
- [ ] Központi gyűjtés

---

## 📚 Forrás
- https://12factor.net/logs
