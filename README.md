# CV Premium ATS - Développeur Fullstack

CV professionnel LaTeX optimisé pour les systèmes ATS, compatible XeLaTeX et PDFLaTeX.

## 🎯 Caractéristiques

- **Premium Design** : Sobre, moderne et professionnel
- **ATS Compatible** : +95% de compatibilité avec les systèmes de recrutement
- **XeLaTeX & PDFLaTeX** : Compatible avec les deux moteurs LaTeX
- **Modulaire** : Chaque section dans son propre fichier
- **Maintenable** : Commandes réutilisables et code commenté
- **Optimisé Fullstack** : Mots-clés ciblés pour les postes Angular/Node.js

## 📁 Structure du projet

```
cv/
│
├── main.tex              # Fichier principal
├── style.sty             # Styles et mise en page
├── commands.tex          # Commandes réutilisables
├── header.tex            # En-tête avec informations de contact
├── profile.tex           # Profil professionnel
├── skills.tex            # Compétences techniques
├── experience.tex        # Expériences professionnelles
├── projects.tex          # Projets personnels
├── education.tex         # Formation
├── certifications.tex    # Certifications
├── languages.tex         # Langues
├── achievements.tex      # Soft Skills
├── interests.tex         # Centres d'intérêt
├── assets/
│     ├── icons/          # Icônes (FontAwesome)
│     └── fonts/          # Polices personnalisées
└── README.md             # Ce fichier
```

## 🚀 Compilation

### Prérequis

- TeX Live ou MiKTeX installé
- XeLaTeX ou PDFLaTeX disponible
- Pour XeLaTeX : Police Source Sans Pro installée (optionnel)

### Commande de compilation (XeLaTeX - recommandé)

```bash
xelatex main.tex
```

Pour une compilation complète (plusieurs passes pour les références) :

```bash
xelatex main.tex
xelatex main.tex
```

### Commande de compilation (PDFLaTeX - alternative)

```bash
pdflatex main.tex
```

### Sur Windows avec PowerShell

```powershell
xelatex main.tex
# ou
pdflatex main.tex
```

### Sur Linux/macOS

```bash
xelatex main.tex
# ou
pdflatex main.tex
```

## 📝 Personnalisation

### Modifier les informations personnelles

Ouvrir `header.tex` et modifier :
- Nom complet
- Titre professionnel
- Coordonnées (téléphone, email)
- Liens (GitHub, LinkedIn, Portfolio)

### Modifier le profil

Éditer `profile.tex` pour adapter le résumé professionnel à votre profil.

### Ajouter une expérience

Dans `experience.tex`, utiliser la commande :

```latex
\experience{Entreprise}{Poste}{Lieu}{Dates}{Description}{Réalisations}
```

Exemple :

```latex
\experience{Tech Corp}{Développeur Fullstack}{Paris}{2020 - 2022}{Développement d'applications web.}{
    \achievement{Réalisation 1}
    \achievement{Réalisation 2}
}
```

### Ajouter un projet

Dans `projects.tex`, utiliser la commande :

```latex
\project{Nom du projet}{Dates}{GitHub}{Démo}{Technologies}{Description}{Réalisations}
```

Exemple :

```latex
\project{Mon Projet}{2023}{https://github.com/user/project}{https://demo.com}{React, Node.js}{Description du projet.}{
    \achievement{Réalisation 1}
    \achievement{Réalisation 2}
}
```

### Modifier les compétences

Éditer `skills.tex` pour ajuster les catégories et technologies.

### Changer les couleurs

Dans `style.sty`, modifier les définitions de couleurs :

```latex
\definecolor{navyblue}{RGB}{10, 25, 47}      % Couleur principale
\definecolor{emerald}{RGB}{16, 185, 129}     % Couleur d'accent
\definecolor{lightgray}{RGB}{148, 163, 184}   % Gris clair
\definecolor{mediumgray}{RGB}{71, 85, 105}    % Gris moyen
```

### Changer la police

Dans `style.sty`, modifier la section police :

```latex
\setsansfont[
    BoldFont={Source Sans Pro Bold},
    ItalicFont={Source Sans Pro Italic},
    BoldItalicFont={Source Sans Pro Bold Italic}
]{Source Sans Pro}
```

Pour utiliser Inter :

```latex
\setsansfont[
    BoldFont={Inter Bold},
    ItalicFont={Inter Italic},
    BoldItalicFont={Inter Bold Italic}
]{Inter}
```

## 🎨 Design

### Palette de couleurs

- **Bleu marine profond** (#0A192F) : Titres et éléments principaux
- **Vert émeraude** (#10B981) : Liens et accents
- **Gris clair** (#94A3B8) : Textes secondaires
- **Gris moyen** (#475569) : Sous-titres

### Typographie

- **Police** : Source Sans Pro (alternative : Inter)
- **Taille** : 11pt
- **Hiérarchie** : Sections (Large), Sous-sections (large), Texte normal

### Mise en page

- **Format** : A4
- **Marges** : 1.8cm (haut, bas, gauche, droite)
- **Maximum** : 3 pages

## 🔧 Commandes LaTeX disponibles

### `\experience{entreprise}{poste}{lieu}{dates}{description}{réalisations}`
Ajoute une expérience professionnelle

### `\project{nom}{dates}{github}{demo}{technologies}{description}{réalisations}`
Ajoute un projet avec liens

### `\skill{catégorie}{compétences}`
Ajoute une catégorie de compétences

### `\education{diplôme}{établissement}{dates}{mention}`
Ajoute une formation

### `\certification{nom}{organisme}{date}`
Ajoute une certification

### `\language{langue}{niveau}`
Ajoute une langue

### `\achievement{réalisation}`
Ajoute une réalisation dans une liste

## 📊 Optimisation ATS

Ce CV est optimisé pour les systèmes ATS avec :

- ✅ Pas de graphiques ou jauges de compétences
- ✅ Pas de photo
- ✅ Structure hiérarchique claire
- ✅ Mots-clés pertinents pour les postes Fullstack
- ✅ Format standard sans tableaux complexes
- ✅ Police standard et lisible

## 🛠️ Résolution de problèmes

### Erreur de police Source Sans Pro

Si Source Sans Pro n'est pas installée, vous pouvez :
1. Installer la police depuis [Google Fonts](https://fonts.google.com/specimen/Source+Sans+Pro)
2. Ou modifier `style.sty` pour utiliser une autre police

### Compilation échoue

Vérifiez que :
- XeLaTeX est installé et dans le PATH
- Tous les fichiers `.tex` sont dans le même dossier
- Les paquets LaTeX requis sont installés

## 📤 Export PDF

Après compilation, le fichier `main.pdf` est généré dans le même dossier.

## 🤝 Contribution

Ce template est modifiable et adaptable à vos besoins. N'hésitez pas à personnaliser les sections selon votre profil.

## 📄 Licence

Ce template est libre d'utilisation pour des besoins personnels et professionnels.

---

**Bon succès avec vos candidatures !** 🚀
