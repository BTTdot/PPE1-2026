# Journal de bord du projet encadré

## Travail sur git:
-Nouveau dépôt public créé (avec son README.md)  
-Clonage de ce dépôt dans mon environnement local avec la commande "git clone < URL >". Vérifications avec la commande "git status".  
-Création d'un fichier (journal.md) depuis le dépôt sur github.  
-Synchronisation de mon dépôt en ligne avec celui sur ma machine (avec la commande "git pull"), notamment afin de pouvoir obtenir le fichier journal.md.  
<br>
Pour ajouter mes modifications à mon dépôt en ligne :  
-git add journal.md  
-git commit -m "ajout de la sous-section sur le travail sur git"  
-git push  
<br>
Pour créer un tag du dernier commit:  
-git tag -a -m "version finie intro git" gitintro  
-git push origin gitintro  
<br>
<br>
## Exercice pipelines:
<br>
[Pour cet exercice, mon terminal est situé dans le dossier PPE1-2026]  
<br>
Commandes que j'ai exécuté pour obtenir les réponses aux questions :  
<br>
- mkdir -p Exercices  
- git add Exercices/  
- git commit -m "ajout du dossier Exercices"  
- git push  
- git status  
<br>
J'ai executé les commandes ci-dessus, mais rien ne semble avoir été déposé sur mon git en ligne.  
<br>
Exercice 1 :  
<br>
Exercice 1.a:  
<br>
J'ai d'abord voulu ajouter le dossier Exercices à mon git. Pour cela, il ne devait pas être vide, alors j'y ai créé au préalable le fichier comptes.txt :  
- touch Exercices/comptes.txt  
- git add Exercices  
- git commit -m "ajout du dossier Exercices"  
- git push  
<br>
Pour répondre à l'exercice :  
<br>
- echo "Annotations en 2016 :" > Exercices/comptes.txt  
- cat ../Exercice1/ann/2016/*/*.ann | wc -l >> Exercices/comptes.txt  
<br>
- echo "Annotations en 2018 :" >> Exercices/comptes.txt  
- cat ../Exercice1/ann/2018/*/*.ann | wc -l >> Exercices/comptes.txt  
<br>
- echo "Annotations en 2017 :" >> Exercices/comptes.txt  
- cat ../Exercice1/ann/2017/*/*.ann | wc -l >> Exercices/comptes.txt  
<br>
<br>
- git add Exercices #autre possibilité : "git add comptes.txt"  
- git commit -m "maj du dossier Exercices (comptes)"  
- git push  
<br>
Exercice 1.b :  
<br>
- echo "Annotations en 2016 :" > Exercices/locations.txt  
- cat ../Exercice1/ann/2016/*/*.ann | grep "Location" | wc -l >> Exercices/locations.txt  
<br>
- echo "Annotations en 2018 :" >> Exercices/locations.txt  
- cat ../Exercice1/ann/2018/*/*.ann | grep "Location" | wc -l >> Exercices/locations.txt  
<br>
- echo "Annotations en 2017 :" >> Exercices/locations.txt  
- cat ../Exercice1/ann/2017/*/*.ann | grep "Location" | wc -l >> Exercices/locations.txt  
<br>
- git add Exercices  
- git commit -m "maj du dossier Exercices (locations.txt)"  
- git push  
<br>
<br>
Exercice 2 :  
<br>
Exercice 2.a :  
<br>
- cat ../Exercice1/ann/2016/*/*.ann | grep "Location" | cut -f 3 | sort | uniq -c | sort -n | tail -n 15 > Exercices/classement_2016.txt  
- cat ../Exercice1/ann/2017/*/*.ann | grep "Location" | cut -f 3 | sort | uniq -c | sort -n | tail -n 15 > Exercices/classement_2017.txt  
- cat ../Exercice1/ann/2018/*/*.ann | grep "Location" | cut -f 3 | sort | uniq -c | sort -n | tail -n 15 > Exercices/classement_2018.txt  
<br>
- git add Exercices  
- git commit -m "maj du dossier Exercices (ajout des fichiers classement)"  
- git push  
<br>
Exercice 2.b :  
<br>
- cat ../Exercice1/ann/*/08/*.ann | grep "Location" | cut -f 3 | sort | uniq -c | sort -n | tail -n 15 > Exercices/classement_mois.txt  
<br>
<br>
L'ajout du fichier résultant à l'exercice 2.b dans le git en ligne n'ayant pas été spécifié, les commandes suivantes ne sont pas à prendre nécessairement en compte.  
- git add Exercices/classement_mois.txt  
- git commit -m "ajout fichier classement_mois.txt"  
- git push  
<br>
<br>
<br>
---
<br>
Pour la création et l'édition du fichier pipelines.txt:  
<br>
- nano Exercices/pipelines.txt #ctrl + O puis Entrée pour sauvegarder puis ctrl + X pour quitter l'édition.  
<br>
<br>
Pour l'ajout du tag :  
<br>
Ajout des dernières modifications de mon dossier Exercices :  
- git add Exercices  
- git commit -m "ajout des dernieres modifs du dossier Exercices"  
- git push  
<br>
Création du tag :  
- git tag -a -m "fin exercice pipelines" fin-ex-pipelines  
- git push origin fin-ex-pipelines
