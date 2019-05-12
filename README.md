# GNS3_Project
 
## Défi 

##### Fournir un réseau stable à un grand nombre de clients sur un même site.

3 Batiments 

Chaque batiment compte 2 étages, avec 5 salles par étage


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
 - 30 + 3 Switchs
 (Caméras, PC etc)

