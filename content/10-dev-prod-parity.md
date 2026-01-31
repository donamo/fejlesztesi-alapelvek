# ⚖️ 10 — Dev/Prod Parity — 12-Factor App

> **Angol:** Keep development, staging, and production as similar as possible  
> **Magyar:** Fejlesztés és éles környezet legyen minél hasonlóbb
> **Kategória:** Alkalmazás-alapelvek & Cloud-native működés

---

## 🎯 Lényeg
- 🧪 Ne legyen „meglepi” prodon
- 🧱 Ugyanaz a stack mindenhol
- 🚀 Ugyanaz a pipeline

## ❌ Anti-pattern
- ❌ SQLite dev, Oracle prod
- ❌ Kézi deploy prodra

## ✅ Best practice
- ✅ Docker mindenhol
- ✅ Ugyanaz az infra
- ✅ Automata deploy

## 📋 Checklist
- [ ] Azonos stack
- [ ] Azonos deploy mód
- [ ] Nincs kézi hackelés

---

## 📚 Forrás
- https://12factor.net/dev-prod-parity
