### Première mise en place

1. Connecter le **nPM2100 EK** à un PC via un câble **USB-C**
2. Mettre une batterie dans l’un des slots prévus à cet effet
3. Connecter la carte batterie au **dev kit**
4. Ouvrir le logiciel **nRF Connect for Desktop**
5. Ouvrir l’interface **nPM PowerUP**, cliquer sur **Select Device**, puis sélectionner **nPM2100 EK**

À ce stade, vous devriez voir dans le logiciel **nRF Connect** le niveau de tension de votre pile.  
Sur la carte de développement, vous devriez aussi voir des LEDs indiquant la tension, ainsi qu’une LED clignotante signalant le bon fonctionnement de la carte.

---
### Phase de Tests

#### Test 1

**Mise en place :** carte batterie connectée au dev kit, **pas de branchement USB**, aucune modification matérielle.  
**Données :**

- Consommation : **15 µA**
- Tension VOUT : **3,11 V**
- Tension sortie LDO : **0 V**

> Il s’agit du branchement de base. Par défaut, la sortie VOUT est à 3 V, d’où une légère consommation.

---
#### Test 2

**Mise en place :** carte batterie connectée au dev kit, **branchement USB**, pas de sortie LDO active, **pas de modification matérielle**.  
**Données :**

- Consommation : **75 à 130 µA**
- Tension VOUT : **3,11 V**
- Tension sortie LDO : **0 V**

> Dans ce cas, certaines LEDs sont allumées pour indiquer le niveau de charge de la pile, ce qui augmente logiquement la consommation.

---
#### Test 3

**Mise en place :** carte batterie connectée au dev kit, **pas de branchement USB**, sortie LDO inactive, **sortie VOUT désactivée par hardware** (via le jumper P9 connecté au GND).  
**Données :**

- Consommation : **9,5 µA**
- Tension VOUT : **0 V**
- Tension sortie LDO : **0 V**

> Ce test vise à mesurer la consommation minimale quand aucune sortie n’est active. On constate une consommation légèrement inférieure à celle du Test 1.

---
#### Test 4

**Mise en place 1 :** carte batterie connectée au dev kit, **USB branché**, **sortie LDO active en mode high**, **VOUT actif**.  
**Données :**

- Consommation : **75 à 130 µA**
- Tension VOUT : **3 V**
- Tension sortie LDO : **1,5 V**

> Deux sorties actives. La consommation est plus élevée, probablement en raison des LEDs allumées et du transfert de données via USB.

**Mise en place 2 :** appuyer **2 secondes** sur le bouton **SHPHLD** pour mettre en **hibernation**.  
**Données :**

- Consommation : **2,5 µA**
- Tension VOUT : **0 V**
- Tension sortie LDO : **0 V**

> En hibernation, toute communication avec le logiciel **nPM PowerUP** est coupée. Les deux sorties sont désactivées et la consommation chute fortement, preuve que le mode hibernation fonctionne bien.

**Mise en place 3 :** appuyer **2 secondes** sur le bouton **SHPHLD** pour **revenir en mode normal**.  
**Données :**

- Consommation : **75 à 130 µA**
- Tension VOUT : **3 V**
- Tension sortie LDO : **0 V**

> Le mode normal est rétabli. Par défaut, seule VOUT est active, la sortie LDO reste désactivée.

---
#### Test 5

**Mise en place :** carte batterie connectée au dev kit, **USB branché**, **sortie LDO active**, **sortie VOUT active**.  
**Données :**

- Consommation : **75 à 130 µA**
- Tension VOUT : **3,3 V**
- Tension sortie LDO : **3 V**

> Ce test vise à observer la **chute de capacité de la pile**, afin de vérifier si la puce fonctionne comme elle le devrait.

![[Pasted image 20250616141118.png]]
>À ce stade, nous pouvons constater une belle décharge. Nous allons encore attendre afin d’avoir des données plus complètes.

---
### Informations complémentaires

**Info 1 —** La sortie **VOUT** semble uniquement **modifiable en tension** mais **non désactivable** via l’interface logicielle. En revanche, on peut la désactiver **par hardware** en connectant sa pin de sortie au **GND via le jumper P9**.

**Info 2 —** Lorsqu’on active la **sortie LDO**, on **perd la communication** avec le logiciel, ce qui suggère que la puce se concentre alors sur sa tâche principale plutôt que sur le transfert des données. Cela a un **impact sur la consommation**.

**Info 3 —** Le bouton **SHPHLD** sert à **mettre la puce en hibernation**, qui est son **mode de consommation le plus faible**. Pour revenir au mode normal, il suffit d’appuyer à nouveau **2 secondes** sur le bouton.

**Info 4 —** Pour mesurer la consommation en courant, un **multimètre Wavetek** a été placé **en série au niveau du jumper P6**, ce qui permet de s’intercaler entre la batterie et la pin d’entrée de la puce sans montage complexe.

---
**Corentin Coueron — 2025-06-16**
