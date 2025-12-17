# T02 - DRP: Còpies de Segurtetat

## Windows

![imatgeWindows](IMG/Windows/1.png)

Instal·lem una màquina virtual de Windows 11 amb 8192 MB de Memoria Base

---
![imatgeWindows](IMG/Windows/2.png)

Creem un segon disc dur de 10 GB d'espai

---
![imatgeWindows](IMG/Windows/3.png)

Entrem a dins de la màquina i anem a l'administració de discs

---
![imatgeWindows](IMG/Windows/4.png)

Creem un nou volum en el disc de 10 GB que hem posat

---
![imatgeWindows](IMG/Windows/5.png)

Li assignem la lletra que tindrà l'unitat

---
![imatgeWindows](IMG/Windows/6.png)

L'etiquetem per posar-li un nom

---
![imatgeWindows](IMG/Windows/7.png)

Per últim, finalitzem la creació del volum simple

---
![imatgeWindows](IMG/Windows/8.png)

Busquem **"Duplicati"** a qualsevol navegador per descarregar-lo

---
![imatgeWindows](IMG/Windows/9.png)

I el descarreguem normalment

---
![imatgeWindows](IMG/Windows/10.png)

Quan el tinguem descarregat, l'instal·lem

---
![imatgeWindows](IMG/Windows/11.png)

I començara l'instal·lació de duplicati

---
![imatgeWindows](IMG/Windows/12.png)

Entrarem i afegirem un BackUp

---
![imatgeWindows](IMG/Windows/13.png)

El configurem com vulguem amb el nom i la contrasenya

---
![imatgeWindows](IMG/Windows/14.png)

Assignem la ruta on volem guardar-lo

---
![imatgeWindows](IMG/Windows/15.png)

El guardarem en el disc dur que hem creat i continuarem

---
![imatgeWindows](IMG/Windows/16.png)

Assignarem l'hora, el lapse de temps i els dies que volem que es fagi aquest BackUp

---
![imatgeWindows](IMG/Windows/17.png)

I com podem veure ja tenim la configuració del BackUp feta

---
![imatgeWindows](IMG/Windows/18.png)

Ara crearem un backUp del Google Drive, tambñe li posarem una contrasenya

---
![imatgeWindows](IMG/Windows/19.png)

Escollim el Google Drive perque només és fagi una còpia d'aquest servei

---
![imatgeWindows](IMG/Windows/20.png)

Li assignem el lloc on el volem guardar i continuem

---
![imatgeWindows](IMG/Windows/21.png)

El guardarem en el apartat de Usuaris

---
![imatgeWindows](IMG/Windows/22.png)

Tornarem a configurar quan volem que aquestes còpies es fagin

---
![imatgeWindows](IMG/Windows/23.png)

I ja la tenim creada, ara haurem d'esperar fins que es fagi la còpia

---
![imatgeWindows](IMG/Windows/24.png)

Fem la comprovació de fer la recuperació d'un arxiu

---
![imatgeWindows](IMG/Windows/25.png)

Per fer-ho, anirem a on tenim els backups en el duplicati i farem un "restore"

---
![imatgeWindows](IMG/Windows/26.png)

Sel·leccionem el que vulguem recuperar

---
![imatgeWindows](IMG/Windows/27.png)

I per últim, posem la ubicació on volem recuperar-ho. Farem el mateix amb el Google Drive, les captures no hi son perque s'havia d'esperar un temps a que es fes el backup i no les vaig poder fer, pero el procediment i el resultat hauria de ser el mateix que amb el primer backup

---

## Linux

![imatgeLinux](IMG/Linux/1.png)

Crearem un disc dur en la màquina virtual de Zorin OS com hem fet en la màquina de Windows

---
![imatgeLinux](IMG/Linux/2.png)

Entrarem a la terminal i començarem amb aquesta comanda que ens deixara veure els discs que tenim i el seu espai

---
![imatgeLinux](IMG/Linux/3.png)

Utilitzem aquesta comanda per gestionar la partició del disc que hem creat amb permisos d'adminstrador. Amb les dues linies que escribim, el que fem es crear una taula de particions i creem una nova amb la segona linia

```
sudo parted /dev/sdb
```

`mklabel gpt`

`mkpart primary xfs 1MiB 100%`

---
![imatgeLinux](IMG/Linux/4.png)

Ab aquesta comanda mostra els discs i les particions que té el sistema i els seus punts de muntatge

```
lsblk -f
```

---
![imatgeLinux](IMG/Linux/5.png)

Instal·lem el servei xfprogs

---
![imatgeLinux](IMG/Linux/6.png)

Formatem el disc "/dev/sdb" amb el sistema d'arxius XFS, i forçem a borra qualsevol format que hi hagues anteriorment

```
sudo mkfs.xfs -f /dev/sdb1
```

---
![imatgeLinux](IMG/Linux/7.png)

Creem el directori /media/backup

---
![imatgeLinux](IMG/Linux/8.png)

Instal·lem Duplicity

---
![imatgeLinux](IMG/Linux/9.png)

Creem un usuari que es diu Usuari1

---
![imatgeLinux](IMG/Linux/10.png)

i seguidament, crearem una ltre usuari que es digui usuari2

---
![imatgeLinux](IMG/Linux/11.png)

iniicarem sessió com a usuari i crearem 4 fitxers de 10 MB

---
![imatgeLinux](IMG/Linux/12.png)

Definim una variablle d'entorn que es diu PASSPHRASE amb contrasenya

```
export PASSPHRASE="contrasenya_forta"
```

---
![imatgeLinux](IMG/Linux/13.png)

Creem una còpia de seguretat amb duplicity del directori "/home" i el guardem en la ruta "/media/backup/duplicity"

```
sudo duplicity /home file:///media/backup/duplicity
```

---
![imatgeLinux](IMG/Linux/14.png)

```
sudo fallocate -l 4M /home/usuari/fitxer5.bin
```
Crea un arxiu de 4 MB i reserva espai en el disc

```
export PASSPHRASE="contrasenya_forta"
```
Defineix una contrasenya com a variable d'entorn per utilitzarla en la sessió actual

```
sudo duplicity /home file:///media/backup/duplicity
```
Realitza una còpia de seguretat del directori "/home" en la ruta "/media/backup/duplicity" utilitzant duplicity

---
![imatgeLinux](IMG/Linux/15.png)

Aquesta comanda mostra l'historial de les coppies de seguretat guardades en la ruta "/media/backup/duplicity"

```
duplicity collection-status file:///media/backup/duplicity
```

---
![imatgeLinux](IMG/Linux/16.png)

Despontem el sistema d'arxius muntat en la ruta

```
sudo umount /media/backup
```

---
![imatgeLinux](IMG/Linux/17.png)

info

---
![imatgeLinux](IMG/Linux/18.png)

info

---
![imatgeLinux](IMG/Linux/19.png)

info

---
![imatgeLinux](IMG/Linux/20.png)

info

---
![imatgeLinux](IMG/Linux/21.png)

Crea l'Script "incrementalbackup.sh" per editar-lo amb "NANO"
```
sudo nano /usr/local/bin/incrementalbackup.sh
```
Dona permisos d'execució al script per poder executar-lo com a programa
```
sudo chmod -x /usr/local/bin/incrementalbackup.sh
```

---
![imatgeLinux](IMG/Linux/22.png)

Hem d'escriure el script que munta un disc, fa una còpia de seguretat incremental xifrada de /home amb duplicity, desa el registre i després desmunta el disc en el NANO que hem creat anteriorment.

---
![imatgeLinux](IMG/Linux/23.png)

Amb les dues linies del final, el que estem configurant es que s'executi una còpia de seguretat completa els diumenges a les 23:00 i una còpia incremental de dilluns a dissabte a les 23:00 utilitzant els scripts indicats.

`0 23 * * 0 /usr/local/bin/fullbackup.sh`

`0 23 * * 1-6 /usr/local/bin/incrementalbackup.sh`

---
![imatgeLinux](IMG/Linux/24.png)

Com podem veure, tenim la carpeta de Duplicity està creada

---
![imatgeLinux](IMG/Linux/25.png)

I a dins hi podem trobar els fitxers dels backups

---
![imatgeLinux](IMG/Linux/26.png)

Amb aquesta comanda la terminal ens mostra que el backup amb duplicity s’ha creat correctament, amb una còpia completa i còpies incrementals xifrades guardades al disc de backup.

```
sudo mount /dev/sdb1 /media/backup
```

---
![imatgeLinux](IMG/Linux/27.png)

La primera comanda munta la partició "/dev/sdb1" al directori "/media/backup" perquè el sistema pugui accedir al seu contingut.

```
sudo mount /dev/sdb1 /media/backup
```
I la segona mostra la llista de fitxers i carpetes dins del directori "/media/bacup/duplicity"

```
ls /media/bacup/duplicity
```

---
I amb aixó acabariem la pràctica de la tasca 2 del projecte 4
