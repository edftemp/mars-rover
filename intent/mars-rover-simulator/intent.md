# Intent : Simulateur Mars Rover
Auteur : Charles et Arnaud.

## Problème
L'équipe sur Terre doit piloter un rover sur Mars en lui transmettant des commandes sous forme de ligne de commande, sans pouvoir observer directement le terrain ni le résultat des déplacements.

## Résultat proposé
Un simulateur qui reçoit un point de départ (position x, y et orientation N/S/E/W), une carte représentant les obstacles, et une liste de commandes. Il interprète ces commandes une à une :
- avancer,
- tourner à droite de 90°,
- tourner à gauche de 90°.

Si un obstacle bloque l'avancée du rover, celui-ci reste immobile. Lorsque le rover atteint un bord de la carte, il réapparaît sur le bord opposé (la carte représente la surface d'une planète, donc elle boucle sur elle-même). Le simulateur affiche la position et l'orientation finales du rover, au format `{x,y,Direction}` (par exemple `{2,3,N}`), après exécution de toutes les commandes.

## Utilisateurs et systèmes concernés
L'équipe sur Terre, qui transmet les commandes au simulateur sous forme de ligne de commande.

## Contraintes
- Le rover est représenté sur la carte par l'emoji 🚙.
- La carte utilise des symboles pour représenter le terrain et les obstacles :
  - Terrain libre : 🟩, 🟫
  - Obstacles : 🌳 (arbre), 🪨 (rocher), 🏔️ (montagne), 💧 (lac), 🌊 (mer)
  - Toutes ces paires et obstacles peuvent coexister sur une même carte.
- Le rover peut avancer ou tourner de 90° à droite ou à gauche.
- Le rover reste immobile lorsqu'un obstacle bloque son avancée.
- La carte boucle sur elle-même : un rover qui sort d'un bord réapparaît sur le bord opposé.
- Le format de sortie est `{x,y,Direction}`.

## Questions ouvertes
_Aucune._
