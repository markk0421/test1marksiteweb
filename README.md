# Bien commencer le gym — site vitrine débutant

Ce projet est un **site web simple** pour apprendre les bases du HTML/CSS.
Le thème est : **"Guide débutant : Bien commencer le gym et la remise en forme"**.

> ⚠️ Le contenu est éducatif et non médical.

## 1) Fichiers du projet

- `index.html` → structure du site
- `style.css` → design et mise en page
- `.nojekyll` → évite un traitement GitHub Pages inutile
- `README.md` → guide d'utilisation

## 2) Ouvrir le site en local (très simple)

### Option A (la plus facile)
1. Ouvrez le dossier du projet.
2. Double-cliquez sur `index.html`.
3. Le site s'ouvre dans votre navigateur.

### Option B (petit serveur local, optionnel)
Si vous avez Python installé :

```bash
python3 -m http.server 8000
```

Puis ouvrez : `http://localhost:8000`

## 3) Modifier le texte du site

1. Ouvrez `index.html` avec un éditeur de texte (VS Code par exemple).
2. Cherchez la section que vous voulez modifier : titre, paragraphes, listes, etc.
3. Remplacez le texte entre les balises HTML.

Exemple :

```html
<h1>Bien commencer le gym</h1>
```

## 4) Changer les couleurs facilement

1. Ouvrez `style.css`.
2. En haut du fichier, modifiez les variables dans `:root`.

Exemple :

```css
:root {
  --primary: #2563eb;
  --bg: #f8fafc;
}
```

- `--primary` = couleur principale des boutons
- `--bg` = couleur de fond générale

## 5) Publier sur GitHub + activer GitHub Pages (pas à pas)

### Étape 1 — Créer un dépôt GitHub

1. Connectez-vous à GitHub.
2. Cliquez sur **New repository**.
3. Nom conseillé : `bien-commencer-gym`.
4. Laissez le dépôt en **Public**.
5. Cliquez sur **Create repository**.

### Étape 2 — Envoyer vos fichiers sur GitHub

Dans le dossier du projet, lancez ces commandes :

```bash
git init
git add .
git commit -m "Premier site vitrine gym"
git branch -M main
git remote add origin https://github.com/VOTRE-UTILISATEUR/bien-commencer-gym.git
git push -u origin main
```

### Étape 3 — Activer GitHub Pages

1. Sur GitHub, ouvrez votre dépôt.
2. Cliquez sur **Settings**.
3. Dans le menu de gauche, cliquez sur **Pages**.
4. Dans **Build and deployment** :
   - Source : **Deploy from a branch**
   - Branch : **main**
   - Folder : **/ (root)**
5. Cliquez sur **Save**.

Après 1 à 3 minutes, GitHub affiche un lien du type :

`https://votre-utilisateur.github.io/bien-commencer-gym/`

## 6) Republier après une modification

Chaque fois que vous modifiez vos fichiers :

```bash
git add .
git commit -m "Mise à jour du site"
git push
```

GitHub Pages se mettra à jour automatiquement.

## 7) Pourquoi "ça ne marche pas" ? (dépannage débutant)

Si le site ne s'affiche pas, vérifiez **dans cet ordre** :

1. **Le nom du fichier est bien `index.html`** (tout en minuscules).
2. **Le CSS est bien lié** dans `index.html` :
   ```html
   <link rel="stylesheet" href="style.css" />
   ```
3. **Le dépôt est public** (sinon Pages peut être limité selon votre plan GitHub).
4. **GitHub Pages est activé** sur `main` + `/ (root)`.
5. **Vous avez bien push les derniers changements** :
   ```bash
   git add .
   git commit -m "fix"
   git push
   ```
6. **Vous ouvrez la bonne URL** :
   - Format attendu : `https://VOTRE-UTILISATEUR.github.io/NOM-DU-DEPOT/`
   - `NOM-DU-DEPOT` doit être exactement le nom du repo GitHub.
7. **Attendre 1 à 3 minutes** après activation (parfois un peu plus).

### Vérifications rapides utiles

Voir l'état Git local :

```bash
git status
```

Voir si vos fichiers sont bien présents :

```bash
ls
```

Tester localement sans GitHub :

```bash
python3 -m http.server 8000
```

Puis ouvrez `http://localhost:8000`.

Si ça marche en local mais pas sur GitHub Pages, le problème vient presque toujours des paramètres **Pages** ou de l'URL.

---

Bon apprentissage 🚀
