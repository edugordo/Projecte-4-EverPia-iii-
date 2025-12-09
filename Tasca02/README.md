# 🛡️ T02 — DPR: Còpies de Seguretat · Cas Pràctic

Aquesta tasca consisteix a portar a la pràctica la política de còpies de seguretat dissenyada prèviament per al client **Muntatges i Serveis Tècnics SL**. L’objectiu és crear **guies tècniques amb proves de concepte** perquè el seu personal pugui implementar la política de backup de manera segura i eficient.

---

# 📌 PART 1 — Còpies de seguretat en equips Windows (Duplicati)

## 📝 Introducció
Tot i que la política inicial no contemplava fer còpies dels equips clients, s'ha de fer una excepció amb el **Windows del director**, ja que conté informació sensible que no resideix al servidor.

S'ha de seguir l’esquema **3-2-1**:
- 3 còpies totals
- en 2 suports diferents
- 1 d'elles fora de les instal·lacions (cloud)

## 🖥️ Entorn de proves
Crea una màquina virtual **Windows 11** amb:
- 💽 Disc 1: Sistema operatiu  
- 💽 Disc 2: 10 GB → destí de les còpies locals  

Per al cloud:
- Google Drive (compte personal creat per a l’activitat).

## 🎯 Objectius pràctics
1. **Instal·lar Duplicati** a Windows.  
2. Configurar:
   - Còpia horària del perfil d’usuari cap al disc secundari.
   - Còpia diària a les **18:00** cap a Google Drive.  
3. Afegir arxius a *Documents* (i altres carpetes d’usuari) per observar el funcionament.  
4. **Esborrar Documents** i fer una **restauració** des del disc secundari.  
5. Provar una **restauració des del núvol** (Google Drive).  

---

# 📦 PART 2 — Còpies de seguretat en servidor Linux (Duplicity + Cron)

## 🖥️ Entorn de proves
- VM Ubuntu Server  
- Segon disc de **10 GB** simulat com a unitat externa  
- Muntatge manual a `/media/backup`

---

## 🎯 Objectius específics de la tasca

✔️ Aplicar una política de còpies 3-2-1 real per a un entorn Windows.

✔️ Generar proves de concepte amb Duplicati (Windows) i Duplicity (Linux).

✔️ Crear tutorials tècnics detallats i fiables.

✔️ Automatitzar còpies completes i incrementals utilitzant cron.

✔️ Verificar restauracions tant locals com al cloud.

---

### 🔗 Recursos i enllaços útils

### 🌐 Duplicati: https://duplicati.com/

### 📝 Crear arxius amb fsutil (Windows): https://waytoit.wordpress.com/2015/03/15/creando-archivos-con-fsutil/

###🐧 Crear arxius de prova a Linux:
https://waytoit.wordpress.com/2015/03/21/creando-archivos-de-prueba-en-linux/

### 📚 Manual de duplicity:
http://manpages.ubuntu.com/manpages/trusty/man1/duplicity.1.html

### ⏱️ Programar tasques amb cron:
https://geekytheory.com/programar-tareas-en-linux-usando-crontab

### ✅ [Solució](solucio.md)
