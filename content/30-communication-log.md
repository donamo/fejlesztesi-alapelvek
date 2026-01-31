# 🗣️ 30 — Communication Log (Kommunikációs napló)

> **Magyar:** Kommunikációs log — Szolgáltatások közti hívások naplózása  
> **Kategória:** Observability, Monitoring & Láthatóság
> **Angol:** Communication Log — Logging inter-service communication

---

## 🎯 Mi ez?

A **communication log** célja:
- 🌐 Minden **bejövő és kimenő** hívás naplózása
- 🧭 Hibák és lassulások visszakövetése
- 🧵 Összekapcsolás tracinggel (correlation id)

---

## 🧱 Mit logolunk?

- ➡️ Request:
  - endpoint, method
  - headers (szűrve!)
  - request id / correlation id
- ⬅️ Response:
  - status code
  - duration
  - error code (ha van)

---

## ❗ Fontos különbség

- 📜 **Application log**: belső események
- 🧾 **Audit log**: üzleti / jogi események
- 🗣️ **Communication log**: hálózati kommunikáció

---

## ❌ Anti-pattern

- ❌ Teljes body logolása PII-vel
- ❌ Nincs request id
- ❌ Nincs időmérés

---

## ✅ Best practice

- ✅ Structured log (JSON)
- ✅ Correlation / Trace ID minden hívásban
- ✅ Request + response summary

---

## 🛠️ Eszközök

- OpenTelemetry instrumentation
- HTTP middleware / interceptor
- Envoy / API Gateway access log

---

## 📋 Checklist

- [ ] Minden bejövő kérés logolva
- [ ] Minden kimenő hívás logolva
- [ ] Van correlation id
- [ ] Nincs PII a logban

---
