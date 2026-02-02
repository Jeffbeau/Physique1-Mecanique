# Physique 1 - Mécanique

Notes de cours pour le cours **203-20B-QM Physique 1** à l'Institut Maritime du Québec.

## Structure du projet

```
Physique1-Mecanique/
├── main.tex                 # Document maître
├── preamble.tex             # Préambule LaTeX (packages, environnements)
│
├── chapitres/
│   ├── ch0/                 # Chapitre 0 - Notions fondamentales
│   │   ├── ch0-main.tex
│   │   ├── sec-unites-SI.tex
│   │   ├── sec-conversions.tex
│   │   ├── sec-chiffres-sig.tex
│   │   └── sec-vecteurs.tex
│   │
│   ├── ch1/                 # Chapitre 1 - Cinématique
│   │   ├── ch1-main.tex
│   │   ├── sec-position.tex
│   │   ├── sec-vitesse.tex
│   │   ├── sec-acceleration.tex
│   │   ├── sec-graphiques.tex
│   │   ├── sec-equations.tex
│   │   ├── sec-chute-libre.tex
│   │   ├── sec-mouvement-2D.tex
│   │   ├── sec-projectile.tex
│   │   ├── sec-rotation.tex
│   │   ├── sec-vitesse-relative.tex
│   │   └── sec-resume.tex
│   │
│   └── ch2/                 # Chapitre 2 - Dynamique et statique
│       ├── ch2-main.tex
│       ├── sec-fondements.tex
│       ├── sec-forces.tex
│       ├── sec-methodologie.tex
│       ├── sec-applications.tex
│       └── sec-resume.tex
│
├── exercices/
│   ├── ex-ch1.tex
│   └── ex-ch2.tex
│
├── figures/                 # Figures et images
│
├── CHANGELOG.md             # Historique des modifications
└── README.md                # Ce fichier
```

## Compilation

```bash
# Compiler le document complet
pdflatex main.tex
pdflatex main.tex  # Deux fois pour la table des matières
```

## Conventions

### Nommage des fichiers
- `ch#-main.tex` : Fichier maître d'un chapitre
- `sec-*.tex` : Section d'un chapitre
- `ex-ch#.tex` : Exercices d'un chapitre

### Environnements personnalisés
- `definition` : Encadré bleu pour les définitions
- `exemple` : Encadré gris pour les exemples (numéroté)
- `remarque` : Encadré orange pour les remarques
- `attention` : Encadré rouge pour les avertissements
- `pratiqueautonome` : Encadré vert pour les exercices en classe

### Commandes utiles
- `\vect{A}` : Vecteur avec flèche
- `\ms`, `\mss`, `\kmh` : Unités courantes
- `\Dt`, `\Dx`, `\Dv` : Deltas

## Auteur

Jean-François Beaudoin  
Institut Maritime du Québec  
Hiver 2026
