# Changelog

Toutes les modifications notables de ce projet sont documentées dans ce fichier.

## [1.0.0] - 2026-01-26

### Réorganisation majeure
- Restructuration complète du projet en architecture modulaire
- Séparation des chapitres en dossiers individuels (`ch0/`, `ch1/`, `ch2/`)
- Extraction des exercices dans des fichiers séparés (`exercices/`)
- Création de fichiers maîtres par chapitre (`ch#-main.tex`)
- Standardisation des noms de fichiers (`sec-*.tex`)

### Fichiers renommés
| Ancien nom | Nouveau nom |
|------------|-------------|
| `preambule.tex` | `preamble.tex` |
| `chapitre0_part1.tex` | `chapitres/ch0/sec-unites-SI.tex` |
| `chapitre0_part2.tex` | `chapitres/ch0/sec-conversions.tex` |
| `chapitre0_part3.tex` | `chapitres/ch0/sec-chiffres-sig.tex` |
| `chapitre0_part4.tex` | `chapitres/ch0/sec-vecteurs.tex` |
| `chapitre1_v2_part1.tex` | `chapitres/ch1/sec-position.tex` |
| `chapitre1_v2_part2.tex` | `chapitres/ch1/sec-vitesse.tex` |
| `chapitre1_v2_part3.tex` | `chapitres/ch1/sec-graphiques.tex` |
| `chapitre1_v2_part5.tex` | `chapitres/ch1/sec-acceleration.tex` |
| `chapitre1_v2_part6.tex` | `chapitres/ch1/sec-equations.tex` |
| `chapitre1_v2_part7.tex` | **Découpé en 3 fichiers** |
| `chapitre1_v2_part8.tex` | `chapitres/ch1/sec-chute-libre.tex` |
| `chapitre1_v2_part9.tex` | `chapitres/ch1/sec-projectile.tex` |
| `chapitre1_v2_part10.tex` | `chapitres/ch1/sec-rotation.tex` |
| `chapitre1_v2_part11.tex` | `chapitres/ch1/sec-mouvement-2D.tex` |
| `section1_fondements.tex` | `chapitres/ch2/sec-fondements.tex` |
| `section2_forces.tex` | `chapitres/ch2/sec-forces.tex` |
| `section3_methodologie.tex` | `chapitres/ch2/sec-methodologie.tex` |
| `section4_applications.tex` | `chapitres/ch2/sec-applications.tex` |
| `resume_competences.tex` | **Découpé en 2 fichiers** |

### Fichiers découpés
- `chapitre1_v2_part7.tex` → 
  - `chapitres/ch1/sec-resume.tex` (résumé + compétences)
  - `chapitres/ch1/sec-vitesse-relative.tex` (complément)
  - `exercices/ex-ch1.tex` (exercices)
- `resume_competences.tex` → 
  - `chapitres/ch2/sec-resume.tex` (résumé + compétences)
  - `exercices/ex-ch2.tex` (exercices)

### Documentation
- Ajout de `README.md`
- Ajout de `CHANGELOG.md`

---

## À faire (backlog)

### Chapitre 1 - Cinématique
- [ ] Ajouter 3 exercices de lecture de graphiques
- [ ] Page 47 : Ajouter note "l'origine peut bouger"
- [ ] Page 54 : Définir "Vitesse Surface" vs "Vitesse Fond"
- [ ] Page 88 : Déplacer exemple bateau+courant pour illustrer décomposition vectorielle

### Chapitre 2 - Dynamique
- [ ] Ajouter exemples de poulies (Atwood, poulie + plan incliné)
- [ ] Retravailler le schéma du skieur
- [ ] Améliorer la progression pédagogique (1 force → 2 forces → systèmes)
