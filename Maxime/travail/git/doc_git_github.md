# Mise en place d'un environnement de travail pour Git:

#### Installer git : 
    # apt install git
- Choisir un **dossier** pour y mettre et recevoir le travail
#### Une fois dans ce **dossier** faire : 
	# git init
	# git config user.name "Prénom NOM"
	# git config user.email "email"
	# git branch -M main
---
## Une fois ces commandes réalisées :  
- **Vérifier** que vous êtes bien un collaborateur du repo distant
	(Seul celui qui a créé le repo distant peut vous inviter en tant que collaborateur)
- Si vous n'êtes pas **collaborateur**, donner votre adresse email à l'hote qui à créé le repo 

Ensuite, il existe deux méthodes pour connecter le repo GitHub à votre dossier.
La première est le **SSH** avec une clé SSH connecter a votre compte **GitHub**. La deuxième 
est en utilisant un **token (https)** d'identification. 

---

## Si vous choisissez le **SSH** :
- Copier le contenu du fichier **~/.ssh/id_rsa.pub** dans GitHub
		**Settings** --> **SSH and GPG keys** --> **New SSH key**.

#### Ensuite, il faudra retourner dans le **dossier** de travail (à l'endroit des commandes précédentes) est y faire :
	# git remote add origin git@github.com:MaximeLBG/Automation-Taches-planifiees-Self-Service.git
	# git pull origin main
Et hop, vous pouvez travailler et partager le travail. 

---

 ## Si vous choisissez le **token (https)** :
- Il faudra d'en un premier temps aller dans **Settings** --> **Developer settings** --> **Personal access tokens** --> **tokens (classic)** --> **generate new token (classic)**
- L'expiration n'est pas très importante (30 days).
- Cocher **repo** et **delete repo**
- Generate new token

#### Ensuite dans le **dossier** de travail (à l'endroit des commandes précédentes) faire :
	# git remote add origin https://votreloginGitHub:token@github.com/MaximeLBG/Automation-Taches-planifiees-Self-Service.git
	# git pull origin main

Et hop, vous pouvez travailler et partager le travail.

---

## Les commandes les plus **importantes** sont :
    # git add . 
        (Pour ajouter tout le nouveau contenu dans une boite)
    # git commit -m "information" 
        (Pour fermer la boite)
    # git push origin main 
        (Pour partager la boite sur le repo distant)
    # git pull origin main 
        (Pour récupérer la boite du repo distant)
