# 🧠 32 — Domain Layer mint Single Source of Truth

> **Magyar:** Az üzleti logika egy helyen  
> **Angol:** Domain Layer as Single Source of Truth

---

## 🎯 Alapelv

**Minden üzleti szabály egyetlen helyen éljen: a Domain rétegben.**

Ez azt jelenti, hogy:
- ❌ nincs üzleti döntés controllerben
- ❌ nincs üzleti logika repository-ban
- ❌ nincs „okos” UI workaround
- ✅ minden szabály újrahasznosítható

---

## 🧱 Rétegek felelőssége

### 🌐 Controller / Adapter
- HTTP / MQ / CLI input-output
- Auth, validation (technikai)
- DTO ↔ Domain mapping

👉 **Nem tartalmaz üzleti döntést**

---

### 🧩 Application / Use Case réteg
- Üzleti folyamat vezérlése
- Tranzakció határok
- Több domain objektum összehangolása

👉 **Orkesztrál, de nem dönt**

---

### 🧠 Domain réteg (AZ IGAZSÁG FORRÁSA)
- Üzleti szabályok
- Invariánsok
- Állapotváltozások

👉 **Itt dől el minden „mi történhet” kérdés**

---

### 🗄️ Infrastructure
- DB, HTTP client, message broker
- Technikai implementációk

👉 **Cserélhető, nem tartalmaz szabályt**

---

## 🧩 Domain építőelemek

- 🧱 **Entity** – állapot + szabály
- 💎 **Value Object** – immutable, validált érték
- 🔧 **Domain Service** – szabály, ami nem fér entitásba
- 📣 **Domain Event** – üzleti esemény

---

## ❌ Anti-pattern: Anemic Domain Model

Jellemzők:
- Entity csak getter/setter
- Logika service-ekben szétszórva
- Nehéz újrahasznosítás

👉 **Kerülendő enterprise környezetben**

---

## ✅ Előnyök

- 🧪 Könnyű unit tesztelés
- 🔁 Több belépési pont (API, batch, event)
- 🧠 Üzleti szabályok egy helyen
- 🔐 Kevesebb regresszió

---

## 📋 Checklist

- [ ] Nincs üzleti if controllerben
- [ ] Domain objektumok tartalmaznak logikát
- [ ] Repo csak perzisztál
- [ ] Domain tesztelhető infra nélkül

---
