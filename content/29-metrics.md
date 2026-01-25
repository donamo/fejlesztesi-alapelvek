# 📊 29 — Metrics (Mérések)

> **Magyar:** Metrikák — Számokkal mérjük a rendszer állapotát  
> **Angol:** Metrics — Measuring system health with numbers

---

## 🎯 Lényeg

- 📈 **Mit mérünk?** teljesítmény, terhelés, hibaarány, üzleti számok
- 🧠 **Miért?** objektív döntések, trendek, riasztások
- 🤖 **Hogyan?** automatizált gyűjtés + dashboard + alerting

---

## 🧱 Metrika típusok

- 🧰 **Technikai**
  - CPU, memória, GC, thread count
  - QPS / RPS, latency (p50/p95/p99), error rate
- 💼 **Üzleti**
  - rendelések száma, feldolgozott tételek
  - sikeres / sikertelen tranzakciók

---

## 📐 Mérési modellek

- 🔴 **RED** (Rate, Errors, Duration) — API-khoz
- 🟢 **USE** (Utilization, Saturation, Errors) — erőforrásokhoz

---

## 🛠️ Eszközök

- Prometheus (gyűjtés)
- Grafana (dashboard)
- OpenTelemetry (instrumentation)
- Datadog / NewRelic (SaaS)

---

## ❌ Anti-pattern

- ❌ „Majd logból kiderül”
- ❌ Nincs riasztás, csak grafikon
- ❌ Nincs SLI/SLO

---

## ✅ Best practice

- ✅ Standard metrikák minden service-ben
- ✅ Dashboard + alerting együtt
- ✅ SLI / SLO definiálva

---

## 📋 Checklist

- [ ] Van latency, error rate, throughput metrika
- [ ] Van dashboard
- [ ] Van riasztás
- [ ] Van SLO

---

## 📚 Forrás

- https://prometheus.io/docs/practices/naming/
- https://sre.google/sre-book/service-level-objectives/
