**________________________________________________|TP n°2|_________________________________________________**

**Exercice 1:**

1) Dans quels dossiers bash trouve-t-il les commandes tapées par l’utilisateur?

*printenv PATH*

 -> résultat :

 /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin

2) Quelle variable d’environnement permet à la commande cd tapée sans argument de vous ramener dansvotre répertoire personnel?

La variable ~
Il suffit de taper cd ~
 
3) Explicitez le rôle des variables **LANG,PWD,OLDPWD,SHELL et_.**

**LANG** -> Détermine le languague utilisé par les logiciels pour communiquer avec l'utilisateur.
**PWD** -> Affiche le répértoire courant ou on se situe.
**OLDPWD** -> (echo $OLDPWD) affiche l'avant dernier chemin ou l'utilisateur est allé, par exemple si on utilise succesivement cd /bin puis cd /dev, le résultat de echo $OLDPWD sera /bin.
**SHELL** -> (echo $SHELL) affiche le chemin du fichier de shell
**_**-> (echo $_) sauvegarde le dérnier argument rentrer par l'utilisateur, par exemple si je tape "adadada" puis que j'éxécute echo _ le résultat sera "adadada".

4) Créez une variable locale **MY_VAR** (le contenu n’a pas d’importance). Vérifiez que la variable existe.

**MY_VAR="1" ; printenv MY_VAR
 *puis*
 **echo $MY_VAR**

5)Tapez ensuite la commande bash. Que fait-elle ? La variable MY_VAR existe-t-elle ? Expliquez. A la fin
de cette question, tapez la commande exit pour revenir dans votre session initiale

bash -> Elle permet de rentrer dans l'environement bash, la variable MY_VAR n'existe plus car elle existe uniquement pour la session ou elle à été créer .


6)Transformez MY_VAR en une variable d’environnement et recommencez la question précédente. Expli-
quez.

**export MY_VAR="1" ; printenv MY_VAR**
Si on retourne dans *bash* , la variable existe puisque cette fois-ci on à créer une variable d'environement et non une variable locale (merci le cour).

7)Créer la variable d’environnement NOMS ayant pour contenu vos noms de binômes séparés par un espace.
Afficher la valeur de NOMS pour vérifier que l’affectation est correcte.

**export NOMS="Défossé Défossé" ; printenv NOMS**

résultat : Défossé Défossé

Donc le résultat est correct.


8)Ecrivez une commande qui affiche ”Bonjour à vous deux, binôme1 binôme2 !” (où binôme1 et binôme2
sont vos deux noms) en utilisant la variable NOMS.

**echo "Bonjour à vous deux, $NOMS"**

9)Quelle différence y a-t-il entre donner une valeur vide à une variable et l’utilisation de la commande
unset ?

*Si on met une valeur vide dans la variable, elle ne contient rien mais elle existe toujour.
Si on unest la variable elle est supprimer.*


10)Utilisez la commande echo pour écrire exactement la phrase : $HOME = chemin (où chemin est votre
dossier personnel d’après bash)

**echo '$HOME' = $HOME**


**Programmation Bash**

Pour mettre le dossier script de maniére permanante dans le PATH il faut :

*A la fin du fichier bashrc* -> **PATH=$PATH:~/script**

*Puis source* **~/.bashrc**

**Exercice 2. Contrôle de mot de passe**

*#!/bin/bash

PASSWORD="az12"

read -sp "Saisissez un mot de passe :" mdp

if [ $PASSWORD == $mdp ] ; then

echo "MDP ok"

else

echo "Le mdp Saisi n'est pas le bon"

fi



