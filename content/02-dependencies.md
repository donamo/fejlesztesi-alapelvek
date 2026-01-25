# 📦 Dependencies (Függőségek) — 12-Factor App

Ez a fejezet a **12-Factor App – II. Dependencies** elvet magyarázza el gyakorlatias, enterprise szemlélettel.

> **Angol:** Dependencies — Explicitly declare and isolate dependencies  
> **Magyar:** Függőségek — A függőségeket explicit módon deklaráld és izoláld

---

## 🎯 Mit mond a 12-Factor?

> Az alkalmazás **ne támaszkodjon implicit, globálisan telepített csomagokra**.  
> Minden függőség legyen **explicit módon deklarálva**, és az alkalmazás **izolált környezetben** fusson.

Másképp fogalmazva:
- 📄 Minden külső library legyen felsorolva egy manifest fájlban (`package.json`, `requirements.txt`, `pom.xml`, stb.)
- 📦 A futtatókörnyezet **pontosan azt** használja, ami deklarálva van
- 🧪 Nincs „nálam működik” jellegű meglepetés

---

# 🧱 Mit nevezünk függőségnek?

**Függőség minden olyan külső komponens, amit a kód használ:**
- 📚 Library / framework (pl. Express, NestJS, Spring, React)
- 🧰 Utility csomagok (pl. lodash, date-fns)
- 🔐 Security csomagok
- 🧪 Teszt keretrendszerek
- 🏗️ Build toolok

---

# ❌ Rossz gyakorlat (anti-pattern)

- ❌ A kód feltételezi, hogy „a szerveren úgyis fent van”
- ❌ README-ben leírjuk: „installáld fel manuálisan”
- ❌ CI szerveren más verzió van, mint lokálisan
- ❌ Prod környezeten más függőség van, mint dev-en

➡️ Eredmény: **nem reprodukálható build**, random hibák.

---

# ✅ Jó gyakorlat (best practice)

- ✅ Minden függőség deklarálva van
- ✅ Verziószám is rögzítve van
- ✅ Egy paranccsal feltelepíthető minden
- ✅ Ugyanaz a verzió fut dev / CI / prod környezetben

---

# 📦 Hogyan néz ki ez a gyakorlatban?

## 🟢 Node.js / TypeScript

- 📄 `package.json`
- 🔒 `package-lock.json` vagy `pnpm-lock.yaml`

```bash
npm ci
```

➡️ Pontosan azt a verziót telepíti, ami lock fájlban van.

---

## 🟢 Python

- 📄 `requirements.txt` vagy `pyproject.toml`
- 🔒 `poetry.lock` / `pipenv.lock`

```bash
pip install -r requirements.txt
```

---

## 🟢 Java

- 📄 `pom.xml` (Maven) vagy `build.gradle` (Gradle)

---

# 🔒 Miért fontos a lock fájl?

- 🔁 **Reprodukálható build**
- 🧪 Ugyanaz a dependency fa mindenhol
- 🛡️ Védelem supply-chain támadások ellen
- 🐞 Könnyebb hibakeresés

---

# 🧪 Izoláció: virtuális környezet / konténer

## 🧰 Megoldások:

- 🐍 Python: `venv`, `poetry env`
- 🟢 Node: `node_modules` project szinten
- 🐳 Docker: teljesen izolált image
- ☸️ Kubernetes: izolált pod

➡️ Cél: **a projekt ne függjön a gép globális állapotától**.

---

# 🚀 Kapcsolat a CI/CD pipeline-nal

A pipeline-ban:

- 🧹 Clean checkout
- 📦 Függőségek telepítése manifestből
- 🧪 Tesztek futtatása
- 🏗️ Build

➡️ Ha nincs jól deklarálva a dependency: **a pipeline fog először szétesni** (jó esetben).

---

# 🔐 Security szempontok

- 🛡️ Dependency vulnerability scan (Snyk, Dependabot, npm audit)
- 🔁 Rendszeres frissítés
- 🚨 Ne használj elavult, karbantartatlan csomagokat

---

# 🧭 Verziókezelési stratégia

- 📌 Használj **lock fájlt**
- 📌 Tudatosan frissíts (`npm update`, `pnpm up`, `dependabot`)
- 📌 Breaking change előtt teszt

---

# 📋 Checklist — Dependencies

- [ ] Minden függőség deklarálva van
- [ ] Van lock fájl a repo-ban
- [ ] Nincs globális függőségre építés
- [ ] CI mindig tiszta környezetből buildel
- [ ] Van dependency security scan
- [ ] Reprodukálható build

---

# 🧠 Összefoglalás

A **Dependencies** 12-factor elv célja:

> 🧱 Az alkalmazás **önmagában hordozza** a teljes futtatási környezet definícióját.

Ez:
- 📦 stabilabb buildet
- 🧪 kevesebb meglepetést
- 🚀 megbízható deploy-t
- 🔐 jobb security-t

eredményez.

---

# 📚 További olvasnivaló

- 🌐 12-Factor App — Dependencies: https://12factor.net/dependencies
- 🗺️ Git & GitHub Roadmap: https://roadmap.sh/git-github
- 🔐 OWASP Dependency-Check: https://owasp.org/www-project-dependency-check/
