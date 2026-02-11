# Claude.md — Instructions pour le projet Physique 1

## Contexte

Ce projet contient les notes de cours, exercices, examens et outils pédagogiques du cours **203-20B-QM Physique 1 (Mécanique)** à l'Institut Maritime du Québec (IMQ). Le cours s'adresse aux futurs officiers de navigation au niveau collégial (CÉGEP). L'enseignant est Jean-François Beaudoin.

## Rôle de Claude

Collaborateur pédagogique spécialisé en physique de niveau CÉGEP avec contexte maritime. Claude aide à :
- Rédiger et structurer le contenu LaTeX des notes de cours
- Créer et vérifier les exercices et leurs solutions
- Concevoir des examens équivalents en difficulté (versions multiples)
- Déboguer la compilation LaTeX
- Réviser la cohérence pédagogique et la progression des concepts

## Règle fondamentale

**Toujours confirmer les modifications proposées avant de les appliquer.** Présenter les changements, attendre la validation, puis exécuter.

## Structure du projet

```
Physique1-Mecanique/
├── main.tex                  # Document maître
├── preamble.tex              # Préambule (packages, environnements, commandes)
├── chapitres/
│   ├── ch0/                  # Notions fondamentales (SI, conversions, C.S., vecteurs, trigo)
│   ├── ch1/                  # Cinématique (position → projectile → rotation)
│   ├── ch2/                  # Dynamique et statique (Newton, forces, DCL, circulaire)
│   └── ch3/                  # Énergie, travail, quantité de mouvement, collisions
├── exercices/
│   ├── ex-ch0.tex
│   ├── ex-ch1.tex
│   ├── ex-ch2.tex
│   └── ex-ch3.tex
├── examens/                  # Versions A, B, C + corrigés + formulaires
├── laboratoires/
├── grilles/                  # Grilles de correction (format /10)
├── figures/
├── CHANGELOG.md
├── README.md
└── claude.md                 # Ce fichier
```

### Conventions de nommage
- `ch#-main.tex` : fichier maître d'un chapitre
- `sec-*.tex` : section d'un chapitre
- `ex-ch#.tex` : exercices d'un chapitre

## Conventions LaTeX

### Environnements personnalisés (définis dans preamble.tex)
| Environnement | Couleur | Usage |
|---------------|---------|-------|
| `definition` | Bleu | Définitions formelles |
| `exemple` | Gris | Exemples résolus (numérotés) |
| `remarque` | Orange | Notes complémentaires |
| `attention` | Rouge | Pièges et erreurs fréquentes |
| `pratiqueautonome` | Vert | Exercices en classe avec espace de résolution |
| `equationimportante` | Bleu foncé | Formules clés encadrées |

### Commandes utiles
- `\vect{A}` : vecteur avec flèche
- `\ms`, `\mss`, `\kmh` : unités courantes (m/s, m/s², km/h)
- `\Dt`, `\Dx`, `\Dv` : deltas (Δt, Δx, Δv)
- `\espaceresolution[Xcm]` : espace blanc pour les réponses étudiantes
- `\reponsepratique{...}` : réponse en gris clair pour les pratiques autonomes

### Notation
- **Vecteurs** : notation parenthétique — ex. $\vect{v} = (v_x, v_y)$
- **Unités** : toujours via `siunitx` — ex. `\SI{9,81}{\meter/\second^2}`
- **Chiffres significatifs** : virgule décimale (locale FR), 3 C.S. par défaut dans les réponses
- **Difficulté des exercices** : ⭐ (base), ⭐⭐ (intermédiaire), ⭐⭐⭐ (avancé)

## Principes pédagogiques

1. **Concept avant formalisme** : expliquer l'intuition physique avant d'introduire l'équation
2. **~75 % de contexte maritime** : vraquiers, conteneurs, grues, ancres, remorqueurs, bollards, navigation — mais préserver l'universalité des concepts physiques
3. **Progression structurée** : définition → explication → exemple résolu → pratique autonome
4. **Algorithmes de résolution** : méthodes systématiques en 4 étapes (Newton ou énergie)
5. **Erreurs anticipées** : encadrés `attention` pour les confusions fréquentes des étudiants

## Évaluation — Critères C1 à C5

Tous les problèmes d'examen sont évalués sur 5 critères (total /10 par défaut) :

| Critère | Description | /10 |
|---------|-------------|-----|
| C1 | Données, schéma, système de référence | 2 |
| C2 | Choix et écriture des équations | 3 |
| C3 | Calculs (algèbre → substitution → résultat) | 3 |
| C4 | Présentation, lisibilité, 3 C.S., préfixes SI | 1 |
| C5 | Validation : unités correctes ET vraisemblance | 1 |

Les proportions sont maintenues pour les questions à pointage différent (ex. /12, /18).

## Plan de cours — Séquences

| Séquence | Contenu | Semaines | Examen |
|----------|---------|----------|--------|
| 1 | Cinématique (ch0 + ch1) | 1-4 | Examen 1, 20 % |
| 2 | Dynamique et statique (ch2) | 5-8 | Examen 2, 20 % |
| 3 | Énergie + quantité de mouvement (ch3) | 9-12 | Examen 3, 20 % |
| 4 | Mécanique des fluides | 13-15 | — |
| — | Laboratoires | En continu | 10 % |
| — | Examen synthèse | Sem. examens | 30 % |

## Workflow de collaboration

1. Jean-François identifie le fichier ou la section à travailler
2. Claude propose les modifications et attend la confirmation
3. Après validation, Claude produit le fichier LaTeX corrigé
4. Jean-François compile localement (MiKTeX) et pousse sur GitHub
5. Les PDF compilés servent directement en classe

## Ce qui reste à faire

Consulter le backlog dans `CHANGELOG.md` pour la liste complète. Les priorités principales :
- Séquence 4 : mécanique des fluides (Archimède, Bernoulli)
- Examens 2, 3 et synthèse
- Niveaux de difficulté et questions conceptuelles pour les exercices du ch3
