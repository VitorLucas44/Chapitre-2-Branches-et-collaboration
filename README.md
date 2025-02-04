# Chapitre-2-Branches-et-collaboration


Exercice : Collaboration et Gestion des Branches en Binôme
Objectifs :
Travailler en binôme sur un projet GitHub.
Utiliser les branches pour séparer les tâches.
Fusionner les contributions de chacun.
Gérer les conflits éventuels.
Partie 1 : Mise en place du projet (1 élève crée le dépôt)
Instructions :
Élève A crée un nouveau dépôt GitHub (ex: collaboration-git).

Élève A ajoute Élève B en tant que collaborateur sur GitHub (Settings → Collaborators).

Élève A initialise le dépôt en local :

bash
Modifier
git clone https://github.com/utilisateur/collaboration-git.git
cd collaboration-git
echo "<h1>Projet Collaboration Git</h1>" > index.html
echo "body { font-family: Arial, sans-serif; }" > style.css
git add .
git commit -m "Initialisation du projet"
git push origin main
Élève B clône le dépôt :

bash
Copier
Modifier
git clone https://github.com/utilisateur/collaboration-git.git
cd collaboration-git
Partie 2 : Travailler sur des branches distinctes
Instructions :
Chaque élève crée sa propre branche et y ajoute du contenu :

Élève A (Branche feature/header) :
Crée une branche et bascule dessus :

bash
Copier
Modifier
git checkout -b feature/header
Modifie index.html en ajoutant un <header> :

html
Modifier
<header>
    <h1>Bienvenue sur notre site</h1>
</header>
Ajoute et valide les modifications :

bash
Modifier
git add index.html
git commit -m "Ajout du header"
git push origin feature/header
Élève B (Branche feature/footer) :
Crée une branche et bascule dessus :

bash
Modifier
git checkout -b feature/footer
Modifie index.html en ajoutant un <footer> :

html
Modifier
<footer>
    <p>© 2025 Collaboration Git</p>
</footer>
Ajoute et valide les modifications :

bash
Modifier
git add index.html
git commit -m "Ajout du footer"
git push origin feature/footer
Partie 3 : Fusionner les branches et gérer les conflits
Instructions :
Les élèves doivent fusionner leurs branches dans main :

Élève A se place sur main et fusionne sa branche :

bash
Modifier
git checkout main
git pull origin main
git merge feature/header
git push origin main
Élève B fait la même chose pour sa branche :

bash
Modifier
git checkout main
git pull origin main
git merge feature/footer
git push origin main
Si un conflit apparaît, les élèves doivent le résoudre ensemble :

Git affichera un conflit dans index.html si les modifications se chevauchent.

Ouvrir index.html et choisir la meilleure version.

Ajouter le fichier corrigé :

bash
Modifier
git add index.html
git commit -m "Résolution du conflit entre header et footer"
git push origin main
Partie 4 : Finalisation du projet
Vérifiez que tout fonctionne bien en ouvrant index.html dans un navigateur.

Supprimez les branches fusionnées :

bash
Modifier
git branch -d feature/header
git branch -d feature/footer
Nettoyez le dépôt distant (optionnel) :

bash
Modifier
git push origin --delete feature/header
git push origin --delete feature/footer
Résultat attendu :
À la fin de l'exercice, le fichier index.html doit contenir le header et le footer avec les contributions des deux élèves. Ils auront appris à utiliser les branches, fusionner du code et résoudre des conflits ensemble. ✅