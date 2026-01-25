# 🩺 16 — Health Checks & SRE Basics

> **Magyar:** Egészségellenőrzés és üzemeltethetőség  
> **Angol:** Health Checks and SRE Basics

---

## 🎯 Lényeg
- ❤️ Liveness: él-e?
- 🧠 Readiness: kiszolgálhat-e?
- 🏗️ Startup check

## 🧱 Miért kell?
- 🤖 Automatikus újraindítás
- ☸️ Kubernetes integráció
- 📉 Kevesebb downtime

## ❌ Anti-pattern
- ❌ Nincs health endpoint
- ❌ Mindig 200 OK

## ✅ Best practice
- ✅ /health /ready
- ✅ Dependency check
- ✅ Timeout figyelés

## 📋 Checklist
- [ ] Van liveness
- [ ] Van readiness
- [ ] Infra használja

---
