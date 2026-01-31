# 🛠️ 12 — Admin Processes — 12-Factor App

> **Angol:** Run admin/management tasks as one-off processes  
> **Magyar:** Admin feladatok is ugyanabból a kódból fussanak
> **Kategória:** Alkalmazás-alapelvek & Cloud-native működés

---

## 🎯 Lényeg
- 🧱 Migráció, seed, script = ugyanaz az app
- 🔁 Ugyanaz a környezet
- ⚙️ Egyszeri futtatás

## ❌ Anti-pattern
- ❌ Külön script repo
- ❌ Manuális SQL turkálás

## ✅ Best practice
- ✅ CLI parancs az appban
- ✅ Same image, same config
- ✅ Auditálható futás

## 📋 Checklist
- [ ] Admin task appból fut
- [ ] Ugyanaz a környezet
- [ ] Verziózott

---

## 📚 Forrás
- https://12factor.net/admin-processes
