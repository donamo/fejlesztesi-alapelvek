# 🧭 33 — Architektúrális és Domain-alapú szemléletek áttekintése

> **Magyar:** DDD, Clean, Hexagonal, Transaction Script – mikor melyik?  
> **Angol:** Overview of Domain and Architectural Patterns

---

## 🧠 Domain-Driven Design (DDD)

**Miről szól?**
- Üzleti domain a középpontban
- Ubiquitous language
- Bounded context

**Mikor jó?**
- Komplex üzleti szabályok
- Hosszú életű rendszer

---

## 🧱 Transaction Script (TS)

**Miről szól?**
- Use-case = egy szkript
- Kevés domain objektum

**Mikor jó?**
- Egyszerű CRUD
- Kevés szabály

---

## 🧩 Hexagonal Architecture

**Miről szól?**
- Domain izolálása
- Portok és adapterek

**Mikor jó?**
- Több interfész (HTTP, MQ)
- DB / framework cserélhetőség

---

## 🧅 Clean / Onion Architecture

**Miről szól?**
- Rétegek befelé mutató függőséggel
- Domain a középpontban

**Mikor jó?**
- Nagy csapat
- Hosszú távú karbantartás

---

## 🧱 Layered Architecture

**Miről szól?**
- Controller → Service → Repo

**Mikor jó?**
- Kisebb projektek
- Kevés üzleti komplexitás

---

## ⚖️ Döntési segédlet

| Helyzet | Ajánlott |
|------|---------|
| Egyszerű CRUD | Transaction Script |
| Komplex domain | DDD + Domain Model |
| Több interfész | Hexagonal |
| Nagy csapat | Clean / Onion |
| Gyors indulás | Layered → később refaktor |

---

## 🧠 Fontos felismerés

> **Nem minden rendszernek kell full DDD**,  
> de **minden rendszernek kell egy hely, ahol az üzleti szabályok élnek.**

---
