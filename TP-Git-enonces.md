# TP Git

---

## Exercice 1 : Création d'un dépôt Git et premiers commits

**Objectif :** Maîtriser les bases de Git (init, add, commit, log)

### Consignes

1. **Créer un nouveau dossier pour votre projet**
    > Un truc du genre "cci-git-practice"
   
2. **Initialiser un dépôt Git**

3. **Créer un fichier README.md**
- Créez un fichier `README.md`
- Ajoutez le contenu suivant :
  ```markdown
  # Mon super projet git !
 
  Ce projet est un exercice de formation sur Git.
  ```

4. **Effectuer votre premier commit**
- Le message du commit doit être : `"Initial commit: ajout du README"`

5. **Modifier le README et faire un deuxième commit**
- Ajoutez une section `## Objectifs` avec au moins 2 objectifs
- Le message du commit doit être : `"Ajout de la section Objectifs"`

6. **Ajouter du contenu et faire un troisième commit**
- Ajoutez une section `## Technologies utilisées` avec Git & Restic listé
- Le message du commit doit être : `"Ajout des technologies utilisées"`

7. **Vérifier l'historique des commits**

---

## Exercice 2 : Gestion avancée des branches avec Git

**Objectif :** Créer des branches, fusionner et gérer les conflits

### Consignes

1. **Vérifier la branche actuelle**

2. **Créer une nouvelle branche `feature-ajout-contact` et se déplacer dessus**

3. **Modifier le projet sur cette branche**
- Créez un nouveau fichier `contact.txt`
- Ajoutez le contenu suivant :
```
  Email: contact@exemple.com
  Téléphone: 01 23 45 67 89
```
- Committez avec le message : `"Ajout des informations de contact"`

4. **Modifier à nouveau sur la branche feature**
- Modifiez `README.md` : ajoutez une section `## Contact` avec un lien vers `contact.txt`
- Committez avec le message : `"Ajout de la section Contact dans README"`

5. **Retourner sur la branche main**

6. **Modifier le README sur main (créer un conflit volontaire)**
- Sur la branche `main`, modifiez `README.md` : ajoutez une section `## Auteur` avec votre nom
- Committez avec le message : `"Ajout de la section Auteur"`

7. **Fusionner la branche `feature-ajout-contact` dans main**

8. **Résoudre le conflit**
- Ouvrez `README.md` dans un éditeur
- Vous verrez des marqueurs de conflit :
```
    <<<<<<< HEAD
    (votre version sur main)
    =======
    (version de la branche feature)
     >>>>>>> feature-ajout-contact
```
- Conservez les deux sections (Contact ET Auteur)
- Finalisez le merge

9. **Vérifier l'historique**

---

## Exercice 3 : Utilisation des tags pour marquer des versions stables

**Objectif :** Créer et gérer des tags pour versionner le projet

### Consignes

1. **Vérifier l'état actuel du projet**
- Assurez-vous que tous vos changements sont committés

2. **Créer un tag pour la version 1.0.0**
- Le tag doit avoir le message suivant : "Version 1.0.0 - Version initiale avec contact"`


3. **Ajouter une nouvelle fonctionnalité**
- Créez un fichier `CHANGELOG.md`
- Ajoutez le contenu suivant :
  ```markdown
  # Changelog
     
  ## [1.0.0] - 2026-02-10
  - Ajout du README
  - Ajout des informations de contact
  - Section Auteur
  ```
- Committez avec le message : `"Ajout du CHANGELOG"`

4. **Faire des modifications supplémentaires**
- Ajoutez une section "## Installation" dans `README.md`
- Exemple de contenu :
  ```markdown
  ## Installation
     
  1. Cloner le repository
  2. Lire le fichier README
  ```
- Committez avec le message : `"Ajout des instructions d'installation"`

5. **Créer un tag pour la version 1.1.0**
- Créez un tag avec le message suivant : "Version 1.1.0 - Ajout du CHANGELOG et instructions d'installation"`

6. **Afficher les informations d'un tag**
- Afficher les détails du tag `v1.0.0` et `v1.1.0`

7. **Comparer les deux versions**
- Entre les deux versions `v1.0.0` et `v1.1.0`, évidemment...

---

## Exercice 4 : Travail collaboratif avec Git

**Objectif :** Simuler un environnement de développement en équipe

**Note :** Me prévenir afin de s'organiser en groupe de 2 à 3

### Consignes

#### Partie 1 : Configuration initiale (Développeur A)

1. **Créer un compte GitHub/GitLab** (si pas déjà fait)

2. **Créer un repository distant**
- Allez sur GitHub ou GitLab
- Créez un nouveau repository public : `projet-cci`
- **Ne cochez PAS** "Initialize with README" (c'est source de problème si vous en avez un en local)

3. **Lier votre dépôt local au dépôt distant**
- Les commandes vous sont données sur GitHub/GitLab

4. **Pousser votre code sur GitHub/GitLab (et les tags)**

5. **Inviter le Développeur B**
- Donnez-lui les droits "Developer"

#### Partie 2 : Clonage et première contribution (Développeur B)

6. **Cloner le repository**

7. **Créer une branche pour votre fonctionnalité : `feature-documentation`**

8. **Ajouter une documentation**
- Créez un fichier `CONTRIBUTING.md`
- Ajoutez les règles de contribution :
```markdown
    # Guide de contribution
     
    ## Comment contribuer
     
    1. Forker le projet
    2. Créer une branche pour votre fonctionnalité
    3. Committer vos changements
    4. Pousser votre branche
    5. Ouvrir une Pull Request
```
- Message du commit : `"Ajout du guide de contribution"`

9. **Pousser votre branche sur le dépôt distant**

10. **Ouvrir une Pull Request**
- Sur GitHub/GitLab, aller sur "New Pull Request" ou "Create Merge Request"
- Remplir les informations en cochant "Delete source branche"


#### Partie 3 : Code Review et Merge (Développeur A)

11. **Relire la Pull Request**
- Allez sur GitHub/GitLab
- Ouvrez la Pull Request créée par le Développeur B
- Lisez le code
- Ajoutez des commentaires (au moins 1 suggestion d'amélioration)

12. **Demander des modifications** (optionnel)
- Commentez la PR : "Ta documentation est aussi captivante que les Worlds de LoL"

13. **Développeur B : appliquer les modifications**
- Modifiez `CONTRIBUTING.md` localement
- Ajoutez une section "## Style de commit"
- Commit & Push sur la même branche
- La PR sera automatiquement mise à jour

14. **Approuver et merger la PR**
- Le Développeur A approuve la PR

#### Partie 4 : Synchronisation (Développeur A)

15. **Récupérer les changements**

16. **Vérifier que le fichier `CONTRIBUTING.md` est présent**

#### Partie 5 : Développement parallèle (Les deux développeurs)

17. **Développeur A : créer une branche `feature-tests`**
- Créez un fichier `tests.txt` avec du contenu
- Commit & Push

18. **Développeur B : créer une branche `feature-config`**
- Créez un fichier `config.txt` avec du contenu
- Commit & Push

19. **Les deux développeurs : ouvrir des Pull Requests**
- Chacun ouvre une PR vers `main`

20. **Merger les deux PR successivement**
- Mergez d'abord `feature-tests`
- Mergez ensuite `feature-config`
- Vérifiez qu'il n'y a pas de conflit

21. **Les deux développeurs : synchroniser leur dépôt local**

---

## Exercice 5 : Intégration de hooks pour automatiser des tâches avec Git

**Objectif :** Créer un hook pre-commit pour vérifier automatiquement le code

### Consignes

#### Partie 1 : Préparation du projet

1. **Créer des fichiers JavaScript**
   
   **Si vous utilisez JavaScript :**
   ```bash
   # Créer un fichier valide
   echo "console.log('Hello World');" > script.js
   
   # Créer un fichier avec erreur de syntaxe
   echo "console.log('Test'" > script-broken.js
   ```
   
   **Si vous utilisez Python :**
   ```bash
   # Créer un fichier valide
   echo "print('Hello World')" > script.py
   
   # Créer un fichier avec erreur de syntaxe
   echo "print('Test'" > script-broken.py
   ```

2. **Committer le fichier valide uniquement**
   ```bash
   git add script.js  # ou script.py
   git commit -m "Ajout d'un script valide"
   ```

#### Partie 2 : Création du hook pre-commit

3. **Créer le fichier de hook**
```bash
touch .git/hooks/pre-commit
```

4. **Rendre le hook exécutable**
```bash
chmod +x .git/hooks/pre-commit
```

5. **Écrire le script du hook**

- Ouvrez `.git/hooks/pre-commit` dans un éditeur et ajoutez :

```bash
   #!/bin/bash
   
   echo "Vérification des fichiers JavaScript..."
   
   # Récupérer tous les fichiers .js dans le staging
   FILES=$(git diff --cached --name-only --diff-filter=ACM | grep '\.js$')
   
   if [ -z "$FILES" ]; then
       echo "Aucun fichier JavaScript modifié."
       exit 0
   fi
   
   # Vérifier chaque fichier
   ERRORS=0
   for FILE in $FILES; do
       echo "Vérification de $FILE..."
       node --check "$FILE" 2>/dev/null
       if [ $? -ne 0 ]; then
           echo "Erreur de syntaxe dans $FILE"
           ERRORS=1
       fi
   done
   
   if [ $ERRORS -ne 0 ]; then
       echo ""
       echo "Commit annulé : des erreurs de syntaxe ont été détectées."
       echo "Corrigez les erreurs et réessayez."
       exit 1
   fi
   
   echo "Tous les fichiers JavaScript sont valides."
   exit 0
```   
   
#### Partie 3 : Tester le hook

6. **Tester avec un fichier valide**
```bash
echo "console.log('Test OK');" >> script.js
```
- Commit & Push

7. **Tester avec un fichier contenant une erreur**
   ```bash
   git add script-broken.js
   git commit -m "Test hook avec fichier invalide"
   ```
   
   **Résultat attendu :** Le commit doit être **bloqué** avec un message d'erreur

8. **Corriger le fichier et réessayer**
   ```bash
   # Corriger la syntaxe
   echo "console.log('Test fixed');" > script-broken.js
   git add script-broken.js
   git commit -m "Correction du script cassé"
   ```
   
   **Résultat attendu :** Le commit doit passer

#### Partie 4 : Forcer un commit (bypass du hook)

9. **Tester le bypass du hook**
```bash
# Recréer une erreur
echo "console.log('Test'" > script-broken.js
git add script-broken.js

# Forcer le commit en ignorant le hook
git commit --no-verify -m "Commit forcé (bypass hook)"
```
   
   **Résultat attendu :** Le commit passe malgré l'erreur de syntaxe

10. **Corriger le fichier**

```bash
echo "console.log('Final fix');" > script-broken.js
git add script-broken.js
git commit -m "Correction finale"
```

