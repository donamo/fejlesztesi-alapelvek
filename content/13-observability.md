# 👀 13 — Observability (Logs, Metrics, Tracing)

> **Magyar:** Megfigyelhetőség — Lásd, mi történik a rendszerben  
> **Kategória:** Observability, Monitoring & Láthatóság
> **Angol:** Observability — Know what's happening inside the system

---

## 🎯 Lényeg
- 📜 Logs: mi történt?
- 📊 Metrics: mennyire jól működik?
- 🧵 Tracing: hol lassú?

## 🧱 Miért kell?
- 🔥 Incidentek gyorsabb megoldása
- 📉 Teljesítmény problémák megtalálása
- 🧠 Rendszer viselkedés megértése

## 🛠️ Eszközök
- OpenTelemetry
- Prometheus + Grafana
- Loki / ELK / Datadog
- Jaeger / Tempo

## ❌ Anti-pattern
- ❌ "Majd belenézünk a logba SSH-val"
- ❌ Nincs metrika, csak érzés

## ✅ Best practice
- ✅ Structured logging
- ✅ RED / USE metrikák
- ✅ Distributed tracing

## 📋 Checklist
- [ ] Van metrika
- [ ] Van tracing
- [ ] Van dashboard
- [ ] Van alerting

---
