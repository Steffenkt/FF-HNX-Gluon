# Installation von Gloue und anpassung für FF-HNX Community
  
### Download der aktuellen Gluon Version STABLE (v2017.1.x)
```bash
git clone https://github.com/freifunk-gluon/gluon.git gluon -b v2017.1.x
cd gluon
```
### Einstellungen der Community einbinden
```bash
git clone https://github.com/ffruhr/site-ffhnx.git site -b 2016
```
### Update der Pakete
```bash
make update
```
### Wichtige Einstellungen setzen (Versionsnummer|Branch| Priprität|Geräte|Sprachen)
Geräte:  
* ar71xx-generic = Für die meisten Router
* ar71xx-nand = Für spezielle Router
* mpc85xx-generic = Für spezielle Router
* x86-generic = Für Virtualisierung
* x86-kvm_guest = Für Virtualisierung
```bash
export GLUON_RELEASE=0.7-nightly-`date +%Y-%m-%d`
export GLUON_BRANCH=experimental
export GLUON_PRIORITY=0
export GLUON_TARGET=ar71xx-generic
export GLUON_LANGS="de en"
```
### Kompilieren (Zahl = CPU Kerne zum kompilieren)
```bash
make -j 4
```
Sollte dieses fehlschlagen (passiert leider häufiger) muss man es so lange probieren bis es funktioniert, eventuell hilft es auch die CPU Kerne zu reduzieren (statt 4 nur 3 oder weniger).  
### Grundinstallation FERTIG
