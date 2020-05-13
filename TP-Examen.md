# TP-E

Examen de technique de test

## Objectifs 
Réaliser, tester et qualifier les 3 sous-parties suivantes
> Date : 13/05/2020
> Version : 1

# Table of Contents
0. [Objectifs](#Objectifs)
1. [Premiere partie](#Premiere-partie)
2. [Deuxieme partie](#Deuxieme-partie)
3. [Troisieme partie](#Troisieme-partie)

# Premiere partie
Concevoir la classe Calculateur, et réaliser les test afin de vérifier son bon fonctionnement.

La classe doit prendre un entier flottant et renvoyer un int en fonction de s'il est strictement positif, null ou négatif.

### Résultats des tests de la fonction du Calculateur

Nompre passée| Entier attendu | Entier sortit| Test
:---|:---|:---|:---
-2| -1| -1| :white_check_mark:
4| 1| 1| :white_check_mark:
0| 0| 1| :white_check_mark:
0.01| 1| 1| :white_check_mark:

# Deuxième partie
Dans ce test nous devons vérifier s'il est possible de : 

* se connecter sans connaître un user, si c'est possible indiquer avec "lequel" vous vous connecter 
* se connecter en tant que ealbert  oui il est possile de se connecter sans connaitre un 'user' avec l'injection suivante : SELECT * FROM user WHERE login = (SELECT login FROM USER where ID = 1 ) --  en suposant que l'user 'ealbert' existe dans la base avec effectuant un injectionSQL il est probablement possible de connecter en mettant dans '$_POST['password']  1=1 -- '

# Troisième partie
Nous avons coder une application qui simuler une partie de Pierre Feuille Ciseaux, la fonction à tester et determinerVainqueur(char P1, char P2) ;

Nous supposons que les char sont correctes et qu'ils correspondent à l'attendu, ils ont été tester dans une autre fonction à part et sont donc valide dans cette fonction.

Joueur 1 | Joueur 2 | Resultat 
:---|:---|:---
P| P| 0
P| F| 2
P| C| 1
F| P| 1
F| F| 0
F| C| 2
C| P| 2
C| F| 1
C| C| 0

Avec cette table de matrice nous avons put créer la méthode determinerVainqueur et créer les méthodes de test. Voici les sorties et les résultat du test.

Joueur 1 | Joueur 2 | Resultat Attendu| Resultat Obtenu| Test
:---|:---|:---|:---|:---
P| P| 0| 0| :white_check_mark:
P| F| 2| 2| white_check_mark:
P| C| 1| 1| white_check_mark:
F| P| 1| 1| :white_check_mark:
F| F| 0| 0| :white_check_mark:
F| C| 2| 2| :white_check_mark:
C| P| 2| 2| :white_check_mark:
C| F| 1| 1| :white_check_mark:
C| C| 0| 0| :white_check_mark:

Comme vous pouvez le voir tous les test sont opérationelles et fonctionelles.
