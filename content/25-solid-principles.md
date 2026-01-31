# 🧱 25 — SOLID Principles

> **Magyar:** SOLID tervezési elvek  
> **Kategória:** Domain, Üzleti logika & Tervezési elvek
> **Angol:** SOLID Design Principles

---

## 🎯 Mi az a SOLID?

A **SOLID** 5 alapelv gyűjtőneve, amelyek célja:
- 🧠 érthetőbb kód
- 🧪 könnyebb tesztelhetőség
- 🔁 könnyebb bővíthetőség
- 🧱 kisebb coupling

## 🧩 Az 5 elv

### 🅢 SRP — Single Responsibility Principle
> Egy osztálynak csak **egyetlen oka legyen a változásra**.

- ❌ God object
- ✅ Kicsi, fókuszált osztályok

---

### 🅞 OCP — Open/Closed Principle
> Nyitott bővítésre, zárt módosításra.

- ❌ If-else erdők
- ✅ Strategy / Polymorphism

---

### 🅛 LSP — Liskov Substitution Principle
> Az altípus helyettesíthető legyen az ősével.

- ❌ Meglepő override-ok
- ✅ Szerződés betartása

---

### 🅘 ISP — Interface Segregation Principle
> Sok kicsi interface jobb, mint egy nagy.

- ❌ God interface
- ✅ Célzott interface-ek

---

### 🅓 DIP — Dependency Inversion Principle
> Absztrakciótól függj, ne konkréttól.

- ❌ new ConcreteService()
- ✅ Constructor injection

---

## 📋 Checklist

- [ ] Osztályok egy dolgot csinálnak
- [ ] Absztrakciók vannak
- [ ] Könnyű mockolni
- [ ] Kevés ripple effect

---
