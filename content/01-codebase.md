> **Angol:** Codebase  
> **Magyar:** Verziókezelés, Release és CI/CD – Enterprise Alapok

# 🧱 1. Mi az a Codebase?

> Egy alkalmazás = egy codebase, több deploy.

---

## 🎯 Miért fontos? – Előnyök

- 🕒 Teljes változástörténet (ki, mikor, mit módosított)
- 👥 Csapatmunka támogatása
- ⏪ Visszagörgetés (rollback) lehetősége
- 🤖 CI/CD, tesztelés, automatizmusok alapja
- 🧾 Auditálhatóság

---

# 🗂️ 2. Verziókezelés (Git)

## 🧠 Mi a Git?

A **Git** egy elosztott verziókezelő rendszer, ami:
- ⚡ gyors
- 🛡️ megbízható
- 🌿 párhuzamos fejlesztést tesz lehetővé

**Git ≠ GitHub**

- 🧰 Git: verziókezelő eszköz
- ☁️ GitHub / GitLab / Bitbucket: platform a repo hostolására + csapatfunkciók + CI/CD

---

## 📌 Alapfogalmak

### 🧱 Commit
- 📸 Egy pillanatkép a kódról
- 🔑 Egyedi hash azonosító
- ⏪ Bármely commitra vissza lehet térni

---

### 🌿 Branch (ág)

**Mire jó?**
- 🧩 Párhuzamos fejlesztés
- 🏗️ Feature-ök elkülönítése
- 🛡️ Stabil main ág védelme

**Tipikus branch nevek:**
- `main` / `master`
- `feature/login`
- `bugfix/nullpointer`
- `release/1.2.0`
- `hotfix/urgent`

**Előnyök:**
- 🔒 Izolált munka
- 💥 Kevesebb konfliktus
- 🧭 Áttekinthető fejlesztési folyamat

---

### 🏷️ Tag

**Mi az?**
- 📌 Egy commit rögzített megjelölése
- 📦 Tipikusan release-ekhez: `v1.0.0`, `v1.2.3`

**Miért kell?**
- 🎯 Pontosan tudod, mi volt a release-ben
- ⏪ Könnyű rollback
- 🔁 Reprodukálható build

> ℹ️ A tag nem mozog, a branch igen.

---

# 🧮 3. Verziózás (Semantic Versioning)

Formátum:  
```
MAJOR.MINOR.PATCH
```

Példa:  
```
1.4.2
```

- 🚨 MAJOR: breaking change
- ✨ MINOR: új feature
- 🐞 PATCH: bugfix

---

# 🔁 4. Kapcsolat a Pipeline-nal (CI/CD)

## 🗺️ Fejlesztési flow

```
feature branch → PR → main → pipeline → staging → prod
```

---

## 🧪 CI (Continuous Integration)

Minden push-ra:

- 🏗️ build
- 🧪 test
- 🧹 lint
- 🔐 security scan

---

## 🚀 CD (Continuous Delivery / Deployment)

Main vagy tag esetén:

- 📦 build artifact
- 🧪 deploy staging
- 🔍 smoke test
- 🚀 (manual vagy auto) deploy prod

---

# 📦 5. Release Flow (ajánlott)

1. 🌿 Feature branchek bemennek main-be
2. 🏷️ Létrejön egy `release/x.y.z` branch
3. 🧪 QA, utolsó fixek
4. 🏷️ Tag: `vX.Y.Z`
5. 🤖 Pipeline:
   - 🏗️ build
   - 📤 publish
   - 🚀 deploy

---

# 📚 6. Tanulási anyagok

- 🗺️ Roadmap: https://roadmap.sh/git-github
- 📖 Pro Git könyv: https://git-scm.com/book
- 📘 GitHub Releases Docs: https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository

---

# 🧠 Összefoglalás

A **Codebase + Git + CI/CD + Release flow** együtt adja:

- 🏗️ a stabil fejlesztési alapot
- 🧾 az auditálhatóságot
- 📈 a skálázhatóságot
- 🚀 a biztonságos és gyors szállítást

Ez az egész minden **enterprise-grade** rendszer alapja.
