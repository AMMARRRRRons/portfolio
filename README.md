# Portfolio - Ons Ammar

Portfolio professionnel moderne et responsive pour Ons Ammar, étudiante en Cybersécurité & Computer Engineering.

## 🚀 Technologies utilisées

- **HTML5** - Structure sémantique
- **CSS3** - Styles personnalisés avec animations
- **JavaScript (Vanilla)** - Interactions et fonctionnalités
- **TailwindCSS** - Framework CSS via CDN
- **FontAwesome** - Icônes

## 📁 Structure du projet

```
portfolio/
│
├── index.html              # Page principale
├── README.md              # Documentation
│
└── assets/
    ├── css/
    │   └── style.css      # Styles personnalisés
    ├── js/
    │   └── script.js      # Scripts JavaScript
    └── images/            # Images (à ajouter)
```

## ✨ Fonctionnalités

- ✅ Design moderne et responsive
- ✅ Mode clair/sombre avec sauvegarde de préférence
- ✅ Navigation fluide avec scroll smooth
- ✅ Menu burger pour mobile
- ✅ Animations au scroll
- ✅ Formulaire de contact (mailto)
- ✅ Sections complètes : Hero, À propos, Compétences, Projets, Parcours, Certifications, Contact
- ✅ Compatible GitHub Pages (fichiers statiques uniquement)

## 🛠️ Installation locale

1. **Cloner ou télécharger le repository**
   ```bash
   git clone <votre-repo-url>
   cd portfolio
   ```

2. **Ouvrir le fichier `index.html`**
   - Double-cliquer sur `index.html` dans votre explorateur de fichiers
   - Ou utiliser un serveur local :
     ```bash
     # Avec Python 3
     python -m http.server 8000
     
     # Avec Node.js (http-server)
     npx http-server
     
     # Avec PHP
     php -S localhost:8000
     ```

3. **Accéder au portfolio**
   - Ouvrir `http://localhost:8000` dans votre navigateur

## 📦 Déploiement sur GitHub Pages

### Méthode 1 : Via l'interface GitHub (Recommandé)

1. **Créer un nouveau repository sur GitHub**
   - Aller sur [GitHub](https://github.com/new)
   - Nommer le repository (ex: `portfolio` ou `ons-ammar-portfolio`)
   - Cocher "Public" (nécessaire pour GitHub Pages gratuit)
   - Ne pas initialiser avec README, .gitignore ou licence

2. **Pousser votre code**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Portfolio Ons Ammar"
   git branch -M main
   git remote add origin https://github.com/VOTRE-USERNAME/VOTRE-REPO.git
   git push -u origin main
   ```

3. **Activer GitHub Pages**
   - Aller dans les **Settings** de votre repository
   - Scroller jusqu'à la section **Pages** (dans le menu de gauche)
   - Sous **Source**, sélectionner la branche `main` et le dossier `/ (root)`
   - Cliquer sur **Save**
   - Votre site sera disponible à : `https://VOTRE-USERNAME.github.io/VOTRE-REPO/`

### Méthode 2 : Via GitHub CLI

```bash
# Installer GitHub CLI si nécessaire
# https://cli.github.com/

# Se connecter
gh auth login

# Créer le repository et activer Pages
gh repo create portfolio --public --source=. --remote=origin --push
gh repo view --web
# Puis activer Pages dans Settings > Pages
```

## 🔧 Personnalisation

### Modifier les informations personnelles

1. **Coordonnées** : Modifier dans la section Contact (`index.html`)
2. **Projets** : Ajouter/modifier les cartes de projets dans la section Projects
3. **Compétences** : Modifier les badges dans la section Skills
4. **Parcours** : Mettre à jour les informations dans la section Education

### Ajouter des images

1. Placer vos images dans `assets/images/`
2. Modifier les chemins dans `index.html` :
   ```html
   <img src="assets/images/votre-image.jpg" alt="Description">
   ```

### Personnaliser les couleurs

Les couleurs principales sont définies via TailwindCSS. Pour les modifier :
- Utiliser les classes Tailwind dans `index.html`
- Ou ajouter des variables CSS dans `assets/css/style.css`

### Modifier le thème

Le mode sombre est géré automatiquement. Pour ajuster :
- Modifier les classes `dark:` dans `index.html`
- Ajuster les couleurs dans `assets/css/style.css`

## 📱 Responsive Design

Le portfolio est entièrement responsive et s'adapte à :
- 📱 Mobile (< 768px)
- 📱 Tablette (768px - 1024px)
- 💻 Desktop (> 1024px)

## 🌐 Compatibilité navigateurs

- ✅ Chrome/Edge (dernières versions)
- ✅ Firefox (dernières versions)
- ✅ Safari (dernières versions)
- ✅ Opera (dernières versions)

## 📝 Notes importantes

- Le formulaire de contact utilise `mailto:` (ouvre le client email)
- Pour un vrai formulaire, il faudrait un backend (ex: Formspree, Netlify Forms)
- Les liens GitHub et LinkedIn doivent être mis à jour avec vos vrais profils
- Les images de projets sont des placeholders - remplacez-les par vos vraies images

## 🔗 Liens utiles

- [Documentation TailwindCSS](https://tailwindcss.com/docs)
- [FontAwesome Icons](https://fontawesome.com/icons)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)

## 📄 Licence

Ce projet est un portfolio personnel. Libre d'utilisation pour inspiration.

## 👤 Auteur

**Ons Ammar**
- Email: ons.ammar@edu.univ-paris13.fr
- LinkedIn: [Votre profil LinkedIn]
- GitHub: [AMMARRRRRons](https://github.com/AMMARRRRRons)

---

⭐ N'hésitez pas à forker ce projet et l'adapter à vos besoins !

