> **Angol:** Version Control - codebase  
> **Magyar:** Verziókezelés, Release és CI/CD – Enterprise Alapok
> **Kategória:** Alkalmazás-alapelvek & Cloud-native működés

# 🧱  Verziókezelés (Version Control)

A **verziókezelés (version control)** egy olyan rendszer, ami **nyomon követi és kezeli a fájlok változásait az időben**. Lehetővé teszi, hogy **többen dolgozzanak ugyanazon projekten párhuzamosan**, miközben **minden módosítás története megmarad**.

A verziókezelő a változásokat (kód, dokumentáció, konfiguráció stb.) egy **repozitóriumban (repository)** tárolja. Ennek köszönhetően:

- ⏪ vissza tudsz térni korábbi állapotokra (rollback),
- 🔍 össze tudod hasonlítani a verziók közti különbségeket (diff),
- 🧾 követhetővé válik a projekt „evolúciója” (mit-miért változtattunk).


---

## 🎯 Miért használjunk verziókezelést?

A verziókezelés **alapvető** szoftverfejlesztésben, mert:

- 🕒 **követhetővé teszi** a módosításokat (ki, mikor, mit),
- 👥 **támogatja a csapatmunkát** és a párhuzamos fejlesztést,
- 🧾 **megőrzi a projekt történetét** (auditálhatóság),
- 🧩 csökkenti a káoszt release-eknél és hotfixeknél,
- 🤖 stabil alapot ad a **CI/CD** és automatizmusok számára.


---

## 📌 Alapfogalmak

### 🧱 Commit
- 📸 Egy pillanatkép a kódról
- 🔑 Egyedi hash azonosító
- ⏪ Bármely commitra vissza lehet térni

---

## 🔀 Merge stratégiák (ágak összefésülése)

Amikor egy branchet (pl. `feature/...`) egy másikba (pl. `main`) integrálsz, a Git többféle megközelítést ad. Ezek a stratégiák segítenek abban, hogy **a történet (history) mennyire marad lineáris**, mennyire látszanak a fejlesztési lépések, és mennyire könnyű később hibát keresni.

### 1) Fast Forward (FF)

- Akkor lehetséges, ha a cél ág (`main`) **nem haladt előre**, csak a feature branch tartalmaz új commitokat.
- Ilyenkor a `main` „előreteker” a feature branch végére.
- ✅ Tiszta, egyszerű history  
- ⚠️ Nem látszik külön merge commit, kevésbé „jelzi”, hogy egy feature integrálva lett

### 2) Non-Fast Forward (merge commit)

- Mindig létrehoz egy **külön merge commitot**, még akkor is, ha FF is lehetne.
- ✅ Jól látszik, *mikor* és *milyen ág* lett beolvasztva  
- ✅ Audit / trace szempontból előnyös  
- ⚠️ Zajosabb history (több merge commit)

### 3) Rebase

- A feature branch commitjai „rákerülnek” a `main` aktuális végére, mintha **mindig is onnan indult volna**.
- ✅ Szép, **lineáris** history  
- ⚠️ **Átírja a commit történetet** (hash-ek változnak), ezért megosztott branch-en óvatosan  
- ✅ Jó fejlesztés közben (lokálisan / saját branchen), hogy rendezett legyen a PR

### 4) Squash

- A feature branch több commitját **összenyomja egyetlen committá** a merge során.
- ✅ Tiszta `main`: “1 feature = 1 commit” jelleg  
- ✅ Egyszerűbb visszagörgetés egy feature-re  
- ⚠️ Elvész a részletes commit történet (finomabb nyomozás nehezebb)

### 5) Cherry-picking

- Nem az egész branchet olvasztod be, csak **egy vagy néhány konkrét commitot** emelsz át.
- ✅ Nagyon célzott (pl. hotfixet gyorsan átvinni release/prod ágra)  
- ⚠️ Könnyű duplikációt vagy konfliktust okozni, ha nem következetes a folyamat  
- ⚠️ History szempontból „szétszórja” a változások eredetét

---

## 🏢 Enterprise best practice: döntések és irányelvek

Enterprise környezetben a verziókezelési döntések célja tipikusan: **auditálhatóság, kiszámítható release, gyors hibajavítás, és a konfliktusok minimalizálása**.

### Ajánlott irányelvek

- 🧭 **Legyen egyértelmű alapelv**: a `main` history legyen **lineáris** (pl. *Squash* vagy *Rebase+Merge*), vagy legyen **explicit merge commit** (Non-FF) – és ezt a csapat tartsa is.
- 🔐 **Protected branch + kötelező PR/MR**: direkt push tiltás `main`/`release` ágakra.
- ✅ **Kötelező CI státuszok**: tesztek, lint, security scan, build.
- 🧾 **Kötelező review szabályok**: minimum 1–2 jóváhagyó, CODEOWNERS a kritikus részekre.
- 🏷️ **Release tagging**: minden éles release **tag-elve** legyen (pl. `v1.4.2`), hogy rollback és reprodukálhatóság garantált legyen.
- 🚑 **Hotfix stratégia**: kritikus javításnál gyakran **cherry-pick** vagy külön `hotfix/...` branch → gyors release.
- 📝 **Commit/PR standard**: konzisztens címek (pl. Conventional Commits), linkelt Jira ticket, értelmes leírás – ez auditnál aranyat ér.

### Gyakori, működő kompromisszum (sok csapatnál bevált)

- Feature branch fejlesztés közben: **rebase** (hogy rendezett legyen a PR)
- `main`-be merge: **squash merge** (tiszta `main`, könnyű revert)
- Release/hotfix: célzottan **cherry-pick**, ha sürgős és kontrollált kell legyen

---


### 🌿 Branch (ág)

**Mire jó?**
- 🧩 Párhuzamos fejlesztés
- 🏗️ Feature-ök elkülönítése
- 🛡️ Stabil main ág védelme

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

# 📚 Tanulási anyagok

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
