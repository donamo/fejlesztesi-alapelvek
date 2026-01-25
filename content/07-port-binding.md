# 🌐 07 — Port Binding — 12-Factor App

> **Angol:** Export services via port binding  
> **Magyar:** A szolgáltatás saját porton legyen elérhető

---

## 🎯 Lényeg
- 🌐 Az alkalmazás **önálló web service**
- 🧱 Nem külső webszerverre van „ráakasztva”
- ⚙️ Saját maga nyit portot és szolgál ki

## ❌ Anti-pattern
- ❌ Apache/Nginx mögé kötött belső app, ami nem önálló
- ❌ Framework-specifikus hostolási függés

## ✅ Best practice
- ✅ App maga indít HTTP szervert
- ✅ Port ENV-ből jön
- ✅ Container / K8s ready

## 📋 Checklist
- [ ] Saját HTTP szerver
- [ ] Port konfigurálható
- [ ] Reverse proxy opcionális

---

## 📚 Forrás
- https://12factor.net/port-binding
