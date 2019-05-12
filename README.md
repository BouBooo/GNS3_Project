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
