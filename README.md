# GNS3_Project
 
## Défi 

### Fournir un réseau stable à un grand nombre de clients sur un même site.

3 Batiments 

Chaque batiment compte 2 étages, avec 5 salles par étage

## Détails projet

#### > Locaux
* 3 bâtiments
  * 2 étages, 5 salles/étages
  * chaque salle supporte au mini 30 clients

#### > Clients du réseau

* ~200 étudiants
  * en moyenne, ils ont 1,5 équipements
    * tous ont un PC
    * certains utilisent smartphone/tablette avec la wifi
* ~50 profs
  * en moyenne, ils ont 1,5 équipements
    * tous ont un PC
    * certains utilisent smartphone/tablette avec la wifi
* ~20 serveurs
* 15 caméras
* 2 admins


## Maquette Infra
```bash

                                                           +-------------+
                                                           |             |
                                                           |     Core    |
                                              +------------+             +---------------+
                 BATIMENT A                   |            +------+------+               |          BATIMENT C
                                       +------+---+               |                  +---+-----+
              +-----------+------------+   IOU1   |               |                  |  IOU2   +----------+----------+
              |           |            +----------+           BATIMENT B             +---------+          |          |
              |           |                                       |                                       |          |
              |           |                                   +---+---+                                   |          |
+-----+    +--+---+   +---+--+   +----+                  +----+  IOU3 +---+                  +-----+   +--+---+    +-+---+    +----+
|Eleve+----+ IOU4 +---+ IOU5 +---+Prof|                  |    +-------+   |                  |Eleve+---+ IOU8 +----+ IOU9+----+Prof|
+-----+    +------+   +------+   +----+                  |                |                  +-----+   +------+    +-----+    +----+
                                                         |                |
                                           +-----+   +---+--+          +--+---+   +----+
                                           |Eleve+---+ IOU6 +----------+ IOU7 +---+Prof|
                                           +-----+   +------+          +------+   +----+

```

## Maquette GNS3

![Alt text](https://github.com/BouBooo/GNS3_Project/blob/master/img/gns3.png?raw=true "")

Afin de simplifier le schéma, tous les éléments ne sont pas présents.
Chaque colonne de swtich représente un batiment, le batiment type étant celui du milieu.
Les caméras et les serveurs possèdent un nom type CAMx-x et SRVx-x. Une caméra reliée à un switch, et portant le nom CAM1-5, signifie que en cas réel, 5 caméras sont reliées à ce switch

## Matériel nécessaire

 - 1 Routeur
 - 33 Switchs
 (Caméras, PC etc)

## Plan d'adressage IP

Batiment 1, étage 1:
```bash
10.33.100.x
10.33.101.x
10.33.102.x
10.33.103.x
10.33.104.x
```

Batiment 1, étage 2:
```bash
10.33.110.x
10.33.111.x
10.33.112.x
10.33.113.x
10.33.114.x
```

Batiment 2, étage 1:
```bash
10.33.200.x
10.33.201.x
10.33.202.x
10.33.203.x
10.33.204.x
```

Batiment 2, étage 2:
```bash
10.33.210.x
10.33.211.x
10.33.212.x
10.33.213.x
10.33.214.x
```

Batiment 3, étage 1:
```bash
10.33.230.x
10.33.231.x
10.33.232.x
10.33.233.x
10.33.234.x
```

Batiment 3, étage 2:
```bash
10.33.240.x
10.33.241.x
10.33.242.x
10.33.243.x
10.33.244.x
```

20 Serveurs:
```bash
10.33.50.x
```

15 Caméras:
```bash
10.33.51.x
```

2 Admins:
```bash
10.33.52.10
10.33.52.11
```
