**________________________________________________|TP n°2|_________________________________________________**

**Exercice 1:**

1) Dans quels dossiers bash trouve-t-il les commandes tapées par l’utilisateur?

*printenv PATH*

 -> résultat :

 /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin

2) Quelle variable d’environnement permet à la commande cd tapée sans argument de vous ramener dansvotre répertoire personnel?

La variable ~
Il suffit de taper cd ~
 
3) Explicitez le rôle des variables **LANG,PWD,OLDPWD,SHELLet_.**

LANG -> Détermine le languague utilisé par les logiciels pour communiquer avec l'utilisateur.
PWD -> Affiche le répértoire courant ou on se situe.
OLDPWD -> (echo $OLDPWD) affiche l'avant dernier CD utilisé, par exemple si on utilise succesivement cd /bin puis cd /dev, le résultat de echo $OLDPWD sera /bin.
SHELL -> (echo $SHELL) affiche le chemin du fichier de shell
_. ->

4) Créez une variable locale **MY_VAR** (le contenu n’a pas d’importance). Vérifiez que la variable existe.

5)

6)

7)

8)

9)

10)


