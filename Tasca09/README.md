# 📦 T09: Servidor de Fitxers Linux — NFS (tasca individual) 🐧

## 📄 Breu descripció

### 🔧 Introducció

Molt bé, equip de consultors júniors.  
En el nostre projecte ens trobem amb un requisit molt habitual entre els clients: **la centralització de dades en entorns Linux**.

---

## 🏢 El Cas Client: *DevOptimize Solutions*

El nostre client és una petita startup de desenvolupament que treballa **exclusivament amb Linux**.  
Actualment tenen un **problema crític de desorganització**:

- El codi font i els documents del projecte estan dispersos.
- Cada desenvolupador treballa amb còpies locals.
- Hi ha conflictes de versions constants.
- La productivitat cau i el risc d'errors augmenta.

Per això ens han contractat per implementar un **servidor de fitxers centralitzat**.  
Com que tot el seu ecosistema és Linux, la solució més eficient és **NFS (Network File System)**.

> 📝 Nota: El client **no utilitza autenticació centralitzada** i, de moment, **no té previst implementar-la**.

---

## 🧪 La Teva Missió (PoC): Implementar un Servidor NFSv3

Has de crear una demostració funcional formada per:

### 💽 1. **Servidor NFS (NFSv3)**
- Configurar-lo correctament.
- Definir les exportacions a `/etc/exports`.

### 🖥️ 2. **Client Linux que consumeixi els recursos**
- Muntar els directoris compartits via NFS.

### 👥 3. **Simulació d’usuaris i grups**
- Crear usuaris i grups per reproduir l’entorn del client.
- Aplicar permisos utilitzant:
  - `chmod`
  - `chown`
  - opcions d’exportació NFS

L’objectiu és **mostrar al client com quedarà la solució**, però també les **limitacions de no tenir un sistema d'autenticació centralitzada**.

---

## 📁 📌 Repositori de la tasca

Aquí tens la descripció completa del projecte amb passos, requisits i estructura:  
👉 https://github.com/SMX2n/Projecte04-NFS

---

## 📚 Materials i links de suport

- **Material propi:** UD5. AA1. NFS — disponible al Moodle del mòdul de Sistemes Operatius en Xarxa.
- **SomeBooks — instal·lació de NFS:**
  - 🔗 *Servidor Ubuntu 20.04:*  
    https://somebooks.es/nfs-parte-1-instalacion-en-un-servidor-ubuntu-20-04-lts/
  - 🔗 *Client Ubuntu 20.04:*  
    https://somebooks.es/nfs-parte-2-instalacion-en-un-cliente-ubuntu-20-04-lts/
- **Documentació oficial d’Ubuntu:**  
  https://documentation.ubuntu.com/server/how-to/networking/install-nfs/

### 📄 [Solució](solucio.md)
