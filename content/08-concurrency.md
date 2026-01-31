# 🧵 08 — Concurrency — 12-Factor App

> **Angol:** Scale out via the process model  
> **Magyar:** Skálázás process modell segítségével
> **Kategória:** Alkalmazás-alapelvek & Cloud-native működés

---

## 🎯 Lényeg
- 📈 Nem thread számot növelünk
- 🧱 Process példányokat szaporítunk
- ☁️ Horizontális skálázás

## ❌ Anti-pattern
- ❌ Egy gigantikus monolit process
- ❌ Thread pool tuning mint fő skálázás

## ✅ Best practice
- ✅ Több instance
- ✅ K8s / autoscaling
- ✅ Worker / web szétválasztás

## 📋 Checklist
- [ ] Stateless instance-ok
- [ ] Horizontálisan skálázható
- [ ] Process típusok elkülönítve

---

## 📚 Forrás
- https://12factor.net/concurrency
