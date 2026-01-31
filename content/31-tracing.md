# 🧵 31 — Tracing (Distributed Tracing)

> **Magyar:** Tracing — Egy kérés útjának követése microservice-eken át  
> **Kategória:** Observability, Monitoring & Láthatóság
> **Angol:** Distributed Tracing — Following a request across services

---

## 🎯 Mi ez?

A **tracing** megmutatja:

> 🧭 Egy adott kérés **hol járt**, **hol mennyi időt töltött**, és **hol lassult el**.

---

## 🧱 Alapfogalmak

- 🧵 **Trace**: egy teljes kérés életútja
- 🧩 **Span**: egy lépés a trace-ben (pl. DB hívás, HTTP call)
- 🏷️ **Trace ID / Span ID**: azonosítók

---

## 🛠️ Eszközök

- OpenTelemetry
- Jaeger
- Tempo
- Zipkin
- Datadog APM

---

## ❌ Anti-pattern

- ❌ „Majd logból összerakom fejben”
- ❌ Nincs end-to-end visibility
- ❌ Nincs context propagation

---

## ✅ Best practice

- ✅ Automatikus instrumentation (HTTP, DB, MQ)
- ✅ Context propagation minden hívásban
- ✅ Metrics + logs + tracing együtt

---

## 🧠 Mire jó?

- 🐢 Performance bottleneck keresés
- 💥 Hiba forrásának megtalálása
- 🧩 Microservice függőségek megértése

---

## 📋 Checklist

- [ ] Van OpenTelemetry agent
- [ ] Trace ID végigmegy minden híváson
- [ ] Van tracing UI (Jaeger / Tempo)
- [ ] Össze van kötve a logokkal

---

## 📚 Forrás

- https://opentelemetry.io/docs/
- https://www.jaegertracing.io/docs/
