# Fase 1 — Treball Individual

## ✏️ Preguntes a Respondre
1. **Què copiar? (Priorització)**  
   - Quines dades són més crítiques?
     - ***Documents Usuaris:*** Fitxers personals, informes, projectes, informació laboral, factures... Solen ser insubstituïbles i contenen dades sensibles.
     - ***Bases de dades:*** Clients, vendes, aplicacions, usuaris... Qualsevol pèrdua pot afectar greument el funcionament de l’empresa
     - ***Logs d'un servidor web:***  Registres d’accessos, errors i operacions. Són crítics per la seguretat.
   - ***Cal fer còpia dels 10 equips clients? Justifica-ho.*** No, no cal fer copia dels 10 equips clients, ja que no tots contenens informació indispensable de l'empresa. Només s'ha de fer còpia dels dispositius que tinguin informació crìtica localment.

2. **Periodicitat i Tipus de Còpia**  
   - ***Proposa un calendari:*** Setmanal 
   - ***Tipus de còpia: Completa, Diferencial o Incremental?*** Incremental, ja que és més ràpida de fer i encara que per la recuperació, el temps es més llarg, la còpia es sobreescriu diariament.

3. **Mitjans i Ubicació**  
   - ***Quin mitjà utilitzar? (HDD extern, NAS, Cloud, Cintes…):*** Depenent de la quantitat de dades que es necessiti guardar, en cas que la quantitat sigui gran, cintes magnètiques, si no es molt gran, amb un disc dur val, ja que té una bona relació de preu per capacitat encara que té problemes de vida i fiabilitat
   - ***On guardar la còpia més recent segons la **regla 3-2-1**:*** La còpia més recent s'ha de fer diariament i s'ha de tenir l'arxiu original i dos back-ups localment

**FASE 2: GRUPAL**

Després de comparar las tres respostes hem vist que tenim coses semblants com per exemple:

Tots tres coincidim que les dades més importants són les bases de dades, els documents dels clients/usuaris i tot el que afecta al funcionament de l’empresa (facturació, aplicacions, etc.).

També coincidim que no cal fer còpia sencera dels 10 equips clients, només dels documents importants si en tenen.

Sobre la periodicitat: un de nosaltres proposa un calendari diari/setmanal/mensual, i l’altre una còpia incremental diaria.

PROPOSTA UNIFICADA:

| Element | Proposta dels tres  | Justificació  |
| :---- | :---- | :---- |
| Dades Crítiques |  \- Bases de dades \- Documents dels clients/usuaris \- Facturació i comptabilitat \- Aplicacions del sistema \- Logs del servidor | Són les dades que l’empresa necessita sí o sí per funcionar. Si es perden, l’empresa no pot treballar, pot perdre diners o clients. |
| Periodicitat (BD) | \- Diària \- Setmanal \- Mensual | Ens assegura tenir còpies recents (diàries) i punts de restauració més segurs (setmanals i mensuals). |
| Tipus de Còpia (BD) | \- **Diària:** Incremental \- **Setmanal:** Diferencial \- **Mensual:** Completa | La incremental és ràpida i còmoda. La diferencial dona més seguretat a la setmana. La completa mensual deixa una còpia que ho té tot. |
| Mitjà 1 (Local) | NAS | Serveix per fer les còpies diàries i setmanals. És ràpid, segur i sempre encès dins l’empresa. |
| Mitjà 2 (Local / Recanvi) | Disc dur extern | Per guardar la còpia completa mensual i tenir un suport físic extra en cas de fallada del NAS. |
| Mitjà 3 (Extern / Fora de l’empresa) | cloud | És la còpia “fora de lloc”. Protegeix contra incendis, robatoris, inundacions, etc. Fa que complim la regla 3-2-1. |

**RESULTAT FINAL DEL 3-2-:**

**3 còpies**:

NAS (diària i setmanal)

Disc dur extern (mensual)

Cloud (còpia externa)

**2 tipus de suports diferents**:

NAS \+ Disc dur extern \+ Cloud

**1 còpia fora de l’empresa**:

Cloud

**Document Final (Fase 3\)**

El grup ha de generar un document amb els següents punts resolts:

1\)      Dades Objecte de Còpia

Quines dades es copien i amb quina freqüència (separant Servidor/Clients i crítiques/no crítiques).

| Tipus de dada | Descripció | Crítica? | Freqüència |
| ----- | ----- | ----- | ----- |
| **Base de Dades Comptabilitat** | Informació financera i comptable | **Sí** | **Cada 4 h (incremental)** \+ diària completa |
| **Base de Dades Clients/CRM** | Dades de clients, comandes, contractes | **Sí** | **Cada 4 h (incremental)** \+ diària completa |
| **Fitxers de projectes** | Documents interns, informes, arxius compartits | No | 1 còpia diària |
| **Configuracions del servidor** | Sistemes, usuaris, polítiques | Sí | 1 còpia diària |
| **Sistema complet (imatge)** | Backup complet del servidor | No | 1 còpia setmanal |

### **Equips Clients (PCs d’oficina)**

| Tipus de dada | Descripció | Crítica? | Freqüència |
| ----- | ----- | ----- | ----- |
| **Documents d’usuari** | Word, Excel, PDF | No (sincronitzats al servidor) | 1 còpia diària |
| **Configuracions d’equip** | Perfil Windows, aplicacions | No | 1 còpia setmanal |
| **Emails (si local)** | PST/OST | Sí | 1 còpia diària (si no es fa al servidor) |

2\)      Cronograma Setmanal Detallat 

| Dia | Dades | Tipus de Còpia | Mitjà |
| ----- | ----- | ----- | ----- |
| **Dilluns** | BD Comptabilitat i Clients | Incremental (cada 4 h) | NAS Local |
|  | Fitxers compartits | Completa | NAS Local |
|  | Configuració servidors | Completa | NAS Local |
| **Dimarts** | BD Comptabilitat i Clients | Incremental (cada 4 h) | NAS Local |
|  | Fitxers PC usuaris | Completa | NAS Local |
| **Dimecres** | BD Comptabilitat i Clients | Incremental (cada 4 h) | NAS Local |
|  | Fitxers compartits | Incremental | NAS Local |
| **Dijous** | BD Comptabilitat i Clients | Incremental (cada 4 h) | NAS Local |
|  | Configuracions servidors | Incremental | NAS Local |
| **Divendres** | BD Comptabilitat i Clients | Incremental (cada 4 h) | NAS Local |
|  | Fitxers compartits | Completa | NAS Local |
| **Dissabte** | Imatge completa del servidor | Completa | NAS \+ Cloud |
|  | Replicació setmanal al cloud | Completa | Cloud extern |
| **Diumenge** | Cap còpia operativa | — | Tasques de manteniment/validació |

3\)      Elecció de Mitjans i Ubicació (Regla 3-2-1)

### **Regla 3-2-1 aplicada**

**3 còpies** de cada dada crítica (Producció \+ NAS \+ Cloud)

**2 tipus de mitjà** (Disc/NAS \+ Cloud)

**1 còpia fora de lloc**

### **Mitjà 1 – Local**

**Tipus:** NAS en xarxa (RAID 5 o RAID 6\)

**Model recomanat:** Synology DS923+ o similar

**Freqüència:** Totes les còpies diàries i incrementals

### **Mitjà 2 – Extern**

**Tipus:** Emmagatzematge Cloud xifrat

**Proveïdor:** **Azure Backup** o **Google Cloud Storage Nearline**

**Freqüència:** Còpia completa setmanal \+ còpia incremental diària només de dades crítiques

### **Ubicació Fora de Lloc**

**Entorn:** Cloud públic (redundància multi-region)

**Xifrat:** AES-256 \+ control d’accés MFA

**Responsable:** Administrador TIC / Responsable de Sistemes

**Validació:** Test de restauració mensual documentat

## **Estratègia de Recuperació (RTO / RPO)**

### **Objectius**

**RPO \= 4 hores**  
  No es poden perdre més de 4 h de dades

**RTO \= 4 hores**  
  El sistema ha d’estar restaurat en menys de 4 h

### **Com es garanteix l’RPO (4 hores)**

### 

###  Backups **incrementals cada 4 hores** de BD Comptabilitat i Clients  Sistema de registre continu Replicació del NAS local al cloud diàriament

### **Com es garanteix l’RTO (4 hores)**

###  Imatge completa del servidor al NAS → restauració ràpida amb sistema de **bare-metal restore**

###  Disponibilitat d’un servidor de substitució (físic o virtual) preconfigura

###   Procés automatitzat per restaurar BDs i serveis essencials   

### Procediment documentat \+ proves mensuals de recuperació

### **Temps estimats**

Restauració imatge servidor → 1 hora

Restaura BD Comptabilitat/Clients → 30 minuts

Validació i rengegada serveis → 30-60 minuts  
 ➡ **Total ≤ 4 hores (compliment garantit)**
