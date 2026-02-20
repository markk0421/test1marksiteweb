# Bien commencer le gym — site vitrine débutant

Ce projet est un **site web simple** pour apprendre les bases du HTML/CSS.
Le thème est : **"Guide débutant : Bien commencer le gym et la remise en forme"**.

> ⚠️ Le contenu est éducatif et non médical.

## 1) Fichiers du projet

- `index.html` → structure du site
- `style.css` → design et mise en page
- `.nojekyll` → évite un traitement GitHub Pages inutile
- `.github/workflows/deploy-pages.yml` → publication automatique sur GitHub Pages
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

## 5) Publier sur GitHub Pages (méthode la plus fiable)

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

### Étape 3 — Activer Pages avec GitHub Actions

1. Sur GitHub, ouvrez votre dépôt.
2. Cliquez sur **Settings**.
3. Cliquez sur **Pages**.
4. Dans **Source**, choisissez **GitHub Actions**.
5. Faites un push (ou relancez le workflow dans l'onglet **Actions**).

Ensuite GitHub publie automatiquement le site.

URL attendue :

`https://votre-utilisateur.github.io/bien-commencer-gym/`

## 6) Republier après une modification

À chaque changement :

```bash
git add .
git commit -m "Mise à jour du site"
git push
```

Le workflow GitHub Actions republie le site automatiquement.

## 7) Pourquoi "ça ne marche pas" ? (dépannage débutant)

Si le site ne s'affiche pas, vérifiez **dans cet ordre** :

1. **Le nom du fichier est bien `index.html`** (tout en minuscules).
2. **Le CSS est bien lié** dans `index.html` :
   ```html
   <link rel="stylesheet" href="style.css" />
   ```
3. **Le dépôt est public**.
4. Dans **Settings > Pages**, la source est bien **GitHub Actions**.
5. Dans l'onglet **Actions**, le workflow **Deploy static site to GitHub Pages** est en vert (succès).
6. **Vous ouvrez la bonne URL** :
   - Format attendu : `https://VOTRE-UTILISATEUR.github.io/NOM-DU-DEPOT/`
   - `NOM-DU-DEPOT` doit être exactement le nom du repo GitHub.
7. **Vous avez bien push les derniers changements** :
   ```bash
   git add .
   git commit -m "fix"
   git push
   ```
8. Attendez 1 à 3 minutes après un nouveau déploiement.

### Vérifications rapides utiles

```bash
git status
```

```bash
python3 -m http.server 8000
```

Puis ouvrez `http://localhost:8000`.

Si ça marche en local mais pas sur GitHub, c'est presque toujours un problème de réglage Pages ou de workflow Actions.

---

Bon apprentissage 🚀
