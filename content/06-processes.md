# 🏗️ 05 — Build, Release, Run — 12-Factor App

> **Angol:** Strictly separate build and run stages  
> **Magyar:** Build, release és run fázisok szétválasztása

---

## 🎯 Lényeg
- 🏗️ Build = artifact készítés
- 📦 Release = config hozzárendelés
- 🚀 Run = futtatás

## ❌ Anti-pattern
- ❌ Build prod-on
- ❌ Kódmódosítás deploykor

## ✅ Best practice
- ✅ CI buildel
- ✅ Artifact verziózott
- ✅ Release immutable

## 📋 Checklist
- [ ] Build külön fázis
- [ ] Release tag-elt
- [ ] Run csak futtat

---

## 📚 Forrás
- https://12factor.net/build-release-run
