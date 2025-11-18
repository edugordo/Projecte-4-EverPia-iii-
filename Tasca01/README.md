# T01 — DRP: Còpies de Seguretat  
## Estudi de Cas Client (Treball Cooperatiu)

---

## 🔹 Breu Descripció
Aquesta activitat introdueix el concepte de còpies de seguretat en entorns empresarials a partir d’un cas realista. Primer es treballen conceptes individualment, després per parelles i finalment en grup per crear una política de còpies definitiva.

---

# 1. Introducció
Durant la primera hora, el responsable de seguretat presenta el tema de les còpies de seguretat. A continuació es treballen els aspectes del tema amb una dinàmica cooperativa 1-2-4.

---

# 2. Cas Client: *Muntatges i Serveis Tècnics SL*
**Sector:** Instal·lació i manteniment d’equips industrials.

## 🖥️ Infraestructura Tècnica
- **Servidor de fitxers (Ubuntu Server)**  
  - *Documents de Projectes*: plànols, especificacions (300 GB, creixement moderat)  
  - *Bases de Dades (Comptabilitat i Clients)*: crítiques, ús diari (20 GB, canvi constant)  
  - *Carpetes Personals*: ús diari (100 GB)

- **10 Equips clients (Windows 10/11)**  
  - La major part del treball es fa al servidor  
  - Alguns tècnics guarden documents importants temporalment a *Documents*

- **Connexió a Internet**  
  - Fibra 600 Mbps (simètrica)

---

# 3. Requisits de Recuperació
- **RTO (Recovery Time Objective):**  
  Les dades de Comptabilitat/Clients han d’estar disponibles en < **4 hores**.

- **RPO (Recovery Point Objective):**  
  - Dades generals → màxim **24 hores** de pèrdua  
  - Comptabilitat/Clients → màxim **4 hores** de pèrdua

- **Retenció mínima:** 1 mes d’històric

---

# 4. Fase 1 — Treball Individual

## ✏️ Preguntes a Respondre
1. **Què copiar? (Priorització)**  
   - Quines dades són més crítiques?  
   - Cal fer còpia dels 10 equips clients? Justifica-ho.

2. **Periodicitat i Tipus de Còpia**  
   - Proposa un calendari setmanal  
   - Tipus de còpia: Completa, Diferencial o Incremental  
   - Especialment per a dades crítiques (BD)

3. **Mitjans i Ubicació**  
   - Quin mitjà utilitzar? (HDD extern, NAS, Cloud, Cintes…)  
   - On guardar la còpia més recent segons la **regla 3-2-1**

---

# 5. Fase 2 — Treball per Parelles

## 🧩 Tasques
1. **Comparació i Discussió**  
   Cada membre exposa les seves respostes de la Fase 1.

2. **Proposta Unificada: Esquema 3-2-1**  
   Heu de consensuar:
   - 3 còpies  
   - 2 mitjans diferents  
   - 1 ubicació externa  

### 📄 Taula de la Proposta de la Parella

| Element | Proposta de la Parella | Justificació |
|--------|--------------------------|--------------|
| **Dades Crítiques** |  |  |
| **Periodicitat (BD)** |  |  |
| **Tipus de Còpia (BD)** |  |  |
| **Mitjà 1 (Local)** |  |  |
| **Mitjà 2 (Extern)** |  |  |

---

# 6. Fase 3 — Treball en Grup

## 🗣️ 1. Debat i Selecció
Cada parella presenta el seu esquema 3-2-1. El grup valora:
- Cost  
- Temps de recuperació  
- Seguretat  
- Simplicitat operativa  

## 🛠️ 2. Política Final de Còpies
El grup redacta el document final que s’entregarà a l’empresa.

---

# [📄 Document Final (Lliurable de Grup)](tasca01.md)

## **1) Dades Objecte de Còpia**
Detallar:
- Quines dades es copien  
- Amb quina freqüència  
- Separar **Servidor / Clients**  
- Diferenciar **crítiques / no crítiques**

---

## **2) Cronograma Setmanal Detallat**

| Dia | Dades | Tipus de Còpia | Mitjà |
|-----|-------|----------------|--------|
| Dilluns |  |  |  |
| Dimarts |  |  |  |
| Dimecres |  |  |  |
| Dijous |  |  |  |
| Divendres |  |  |  |
| Dissabte |  |  |  |
| Diumenge |  |  |  |

---

## **3) Elecció de Mitjans i Ubicació (Regla 3-2-1)**

### 🎛️ Mitjà 1 (Local)
- Tipus: *p. ex. Disc dur USB / NAS / DAS*
- Ubicació: Sala de servidors
- Responsable: Administrador local

### ☁️ Mitjà 2 (Extern)
- Tipus: *Cloud, cinta LTO, servidor extern…*
- Proveïdor proposat: *Azure, Google Cloud, Wasabi, proveïdor local…*

### 📦 Ubicació Fora de Lloc
- On s’emmagatzema la còpia externa
- Com s’hi accedeix
- Responsable de la seva gestió

---

## **4) Estratègia de Recuperació (RTO / RPO)**

Explicar com es garanteix:
- **RTO < 4 hores** per a Comptabilitat/Clients  
- **RPO < 4 hores** per a Comptabilitat/Clients  

Inclou:
- Tipus de còpia utilitzada  
- Tecnologia (snapshots, incremental freqüent…)  
- Procediment de restauració  

---

# 🔗 Materials i Enllaços de Suport

- **Moodle 0226 Seguretat Informàtica – RA2.AA3 Còpies**
- **INCIBE — Copias de seguridad: guía para empresarios**
- **Xataka — El método 3-2-1 (vídeo YouTube)**  
  https://youtu.be/PM_M4Iz6I4o?si=F7DRyDDTZE3hjWn8

---

# 🎯 Objectiu Específic de la Tasca
Treballar la política de còpies de seguretat mitjançant una dinàmica cooperativa **1-2-4** per reflectir una situació real de treball en un equip tècnic.

