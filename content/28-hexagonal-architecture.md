# 🧱 28 — Hexagonal Architecture (Ports & Adapters)

> **Magyar:** Hexagonális architektúra  
> **Angol:** Hexagonal Architecture (Ports and Adapters)

---

## 🎯 Mi ez?

A **Hexagonal Architecture** célja:

- 🧠 A domain izolálása
- 🔁 Infrastruktúra cserélhetősége
- 🧪 Könnyű tesztelhetőség

## 🧩 Fő részek

- 🟢 Domain (üzleti logika)
- 🔵 Portok (interface-ek)
- 🟣 Adapterek (DB, HTTP, Kafka, stb.)

```
[ UI ] -> ( Adapter ) -> ( Port ) -> [ Domain ] -> ( Port ) -> ( Adapter ) -> [ DB ]
```

## ✅ Előnyök

- 🔁 Könnyű DB vagy framework csere
- 🧪 Domain izoláltan tesztelhető
- 🧱 Clean boundaries

## ❌ Anti-pattern

- ❌ Framework a domainben
- ❌ Infrastruktúra függőség a core-ban

---

## 🧠 Mikor használd?

- 🏦 Komplex domain
- 🧪 Sok üzleti szabály
- 🔁 Hosszú élettartamú rendszer

---
