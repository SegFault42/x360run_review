# x360run

## 1) Présentation de la puce :

![1](https://github.com/SegFault42/x360run/blob/master/img/1.jpg)

![2](https://github.com/SegFault42/x360run/blob/master/img/2.jpg)

J'avoue qu'à première vu elle peut faire peur ^^. Mais ne vous fiez pas au apparence vous verrez que finalement cette puce en a dans le ventre.

La puce est uniquement compatible Xbox Slim, et pré-programmer pour Corona et Trinity :).

Il y a 6 points à souder. Il n'y a pas de point à souder au CLK de la console vu qu'elle embarque un Oscillateur de 96MHz.

La puce est par default configurer pour Corona.

Penser à isoler l’arrière de la puce ;)



## 2) Configuration de la puce pour Trinity :

SI vous voulez la monter sur une Trinity il y à 2 solutions :
1) Changer les 2 condensateur, le 330pf par un 220pf et le 15pf par un 25pf.
Dans ce cas le 220pf ce place sur C1 et le point D :

![2](https://github.com/SegFault42/x360run/blob/master/img/3.jpg)

 Suivre ce tableau pour les pontages :
 
 ![3](https://github.com/SegFault42/x360run/blob/master/img/4.jpg)
 
 Donc pour la mettre en Trinity par default on ponte M1 et M0.

2) Laisser les condo 330pf et 15pf et ponter en Trinity ADD-ons delay.

![4](https://github.com/SegFault42/x360run/blob/master/img/5.jpg)

On peut maintenant changer le Delay. Voila ci dessous le tableau avec les differents montage pour changer le Delay :

![5](https://github.com/SegFault42/x360run/blob/master/img/6.png)

Ayant tout tésté sur 3 consoles trinity différentes j'obtient les meilleurs résultats en -3.

Ensuite on peut aussi changer le width trimming. Voila ci dessous le tableau avec les differents montage pour changer le width :

![6](https://github.com/SegFault42/x360run/blob/master/img/7.jpg)

La je me suis mis à défaut donc le W0,W1 et W2 ouvert.

La puce est maintenant prête pour votre console. 

Voila la config qui pour moi fonctionne le mieux sur Trinity.

![7](https://github.com/SegFault42/x360run/blob/master/img/8.jpg)

## 3) Installation de la puce dans la console :

L'emplacement de la puce n' à pas de grande importance. Généralement je la pose içi :

![8](https://github.com/SegFault42/x360run/blob/master/img/9.jpg)

Pour corona voila les points à souder :

 Corona V1 - V2 :

![8](https://github.com/SegFault42/x360run/blob/master/img/10.jpg)

![8](https://github.com/SegFault42/x360run/blob/master/img/11.jpg)

 Corona V3 - V4 :

![8](https://github.com/SegFault42/x360run/blob/master/img/12.jpg)
 
 Sur Trinity :

![8](https://github.com/SegFault42/x360run/blob/master/img/13.jpg)

![8](https://github.com/SegFault42/x360run/blob/master/img/14.jpg)

Sur cette puce comme sur les autres la longeur du CPU_Reset est trés importante.

Contrairement au autre puce ou le cpu reset doit généralement être à environ 55CM, le CPU_Reset doit être entre 3 et 7 cm.

J'ai testé avec un CPU_Reset à plus de 7cm, résultats les ventilo tourne à fond, et la puce ne reset pas. Avec un CPU_Reset à moin de 3 cm la console démarre entre 1min et 2 min.

La longueur du POST_OUT est aussi importante. Généralement le POST_OUT doit faire à peut prés la même longueur que le CPU_Reset.

Sur la dernière trinity que j'ai faite le CPU_Reset fait 5 cm et le POST_OUT environ 6 cm.

Voila ce que donne la puce sur Trinity :

![8](https://github.com/SegFault42/x360run/blob/master/img/15.jpg)

et sur Corona:

![8](https://github.com/SegFault42/x360run/blob/master/img/16.jpg)

Le fil rouge sur la résistance n'est pas à prendre en compte.

### Les points positifs de la X360run :

- Pas cher
- Puce de bonne qualité
- Quartz de 96 MHz intégré à la puce
- Pas de programmation
- Pas de long CPU_RESET qui tourne autour du ventilo
- Temps de boot plus que satisfaisant.

### Les points négatif de la X360run :

- Uniquement compatible slim
- Pas de câblage ni de double face fournis. ( ça dépend du revendeur )

