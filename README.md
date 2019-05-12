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

