# T03: Pla de recuperació davant desastres: imatges del sistema 🔐💾

## Breu descripció 📄

### Introducció al cas 🖥️
Recordeu el cas del portàtil al que no es podia accedir? En aquella situació la vostra perícia tant a l’hora de recuperar l’accés com a la posterior fortificació de l’accés, va deixar prou impressionat al client. Per tant, ha requerit que hi participeu en el seu nou encàrrec.

Ha encarregat l’elaboració d’un Pla de Contingència i Continuïtat del Negoci. Dins d’aquest pla, s’ha de posar en marxa el Pla de Recuperació davant Desastres (DRP o Disaster Recovery Plan).

Aquest pla inclou tots els processos de restauració de les dades, hardware i software crític de la organització davant d’un esdeveniment catastròfic per tal de recuperar l’activitat normal el més ràpid possible.

Un dels aspectes que l’esmentat pla contempla és assegurar que els treballadors puguin disposar de forma ràpida dels seus equips de treball en cas de robatori, avaria, etc. Per aquest motiu, se’ns demana la creació d’imatges de restauració del sistema. El temps de posada en marxa és crític per l’àrea de negoci, per aquest motiu, no és viable la solució clàssica de instal·lar el sistema operatiu, aplicar les configuracions, instal·lar les aplicacions, etc.

Cal tenir en compte que els equips del client són GNU Linux, en concret tota l’empresa usa **Zorin OS 18** amb una sèrie d’aplicacions ja configurades.

---

## Fase 1: Anàlisi i Justificació solució tècnica 🔍⚙️

En aquesta primera fase, caldrà que investiguem diverses eines que permetin realitzar la tasca indicada, és a dir, crear una imatge del disc d’un equip, de manera que es pugui restaurar a posteriori mantenint les configuracions, aplicacions, etc. que estaven originalment. Al mercat existeixen moltes solucions tant comercials com de comunitat per resoldre aquest tema.

Elaboreu una petita comparativa entre alguns productes: trieu **2 de comercials** i **2 de comunitat**.  
La comparativa ha d’incloure les característiques destacades i el preu.  
És important que **sigui una comparativa**, no un conjunt de còpies de les pàgines web dels productes.

Finalment, heu d’indicar quina seria la solució que proposeu.  
Recordeu que la proposta ha de ser raonada i justificada, tenint en compte els diversos aspectes la comparativa.

---

## Fase 2: Guia d'Ús Tècnica (Manual Operatiu) 📘🛠️

A partir de la màquina que ens proporciona el client, en aquest cas la simulem amb una OVA, cal que feu els següents processos:

- Crear una imatge completa del sistema.  
- Restaurar aquesta imatge sobre un sistema net, que a efectes de la prova de concepte serà una màquina virtual idèntica a l’original (RAM, processador, xarxa i mida de disc), però sense cap sistema operatiu instal·lat.

Caldrà elaborar una guia tècnica per tal que el personal de manteniment pugui realitzar les dues accions, per tant, procureu documentar de forma acurada, incorporant aquelles imatges que siguin significatives.

Com és una prova de concepte i encara no sabeu si el client accepta la vostra proposta de producte, **usareu Rescuezilla** per fer la següent guia.

> Es tracta d’una tasca individual.

---

## Materials i links de suport 🔗📚

- **INCIBE.** _¿Ya tienes tu Plan de Recuperación ante Desastres?_ (Blog, Agost 2019)  
  https://www.incibe.es/empresas/blog/tienes-tu-plan-recuperacion-desastres  

- **Pàgina oficial de Rescuezilla**

---

## Objectius específics de la tasca / Finalitat de la tasca 🎯

L’objectiu d’aquesta activitat és treballar amb la creació d’imatges de sistemes i la posterior recuperació a partir de les imatges creades, com a part imprescindible d’un DRP.

