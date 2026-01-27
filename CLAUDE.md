# CLAUDE.md - AI Assistant Guide for Physique1-Mecanique

## Project Overview

This repository contains LaTeX course notes for **203-20B-QM Physique 1** (Physics 1 - Mechanics) at the Institut Maritime du Québec. The course covers fundamental physics concepts including kinematics, dynamics, and statics with a maritime context.

- **Language**: French (all content and comments)
- **Format**: LaTeX document (book class)
- **Author**: Jean-François Beaudoin
- **Academic Year**: Winter 2026

## Repository Structure

```
Physique1-Mecanique/
├── CLAUDE.md                    # This file - AI assistant guidelines
├── README.md                    # Root README (minimal)
└── Physique1-Mecanique/         # Main project directory
    ├── main.tex                 # Document master file (compile this)
    ├── preamble.tex             # LaTeX packages, environments, commands
    ├── README.md                # Project documentation
    ├── CHANGELOG.md             # Version history and backlog
    │
    ├── chapitres/               # Chapter content
    │   ├── ch0/                 # Chapter 0 - Fundamental Concepts
    │   │   ├── ch0-main.tex     # Chapter master file
    │   │   ├── sec-unites-SI.tex
    │   │   ├── sec-conversions.tex
    │   │   ├── sec-chiffres-sig.tex
    │   │   └── sec-vecteurs.tex
    │   │
    │   ├── ch1/                 # Chapter 1 - Kinematics
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
    │   └── ch2/                 # Chapter 2 - Dynamics & Statics
    │       ├── ch2-main.tex
    │       ├── sec-fondements.tex
    │       ├── sec-forces.tex
    │       ├── sec-methodologie.tex
    │       ├── sec-applications.tex
    │       └── sec-resume.tex
    │
    ├── exercices/               # Exercises by chapter
    │   ├── ex-ch1.tex
    │   └── ex-ch2.tex
    │
    └── figures/                 # Graphics directory
```

## Compilation

```bash
cd Physique1-Mecanique/Physique1-Mecanique
pdflatex main.tex
pdflatex main.tex  # Run twice for table of contents
```

No build tools (Makefile, latexmk) are configured. Use direct `pdflatex` compilation.

## Naming Conventions

### File Naming
- **Chapter masters**: `ch#-main.tex` (aggregates sections)
- **Section files**: `sec-*.tex` (kebab-case descriptive names)
- **Exercise files**: `ex-ch#.tex`
- **Configuration**: `preamble.tex`

### Content Language
- All LaTeX content is in **French**
- Comments in LaTeX files are in French
- Use French typography (comma as decimal separator via `siunitx`)

## Custom LaTeX Environments

These custom environments are defined in `preamble.tex`:

| Environment | Purpose | Styling |
|-------------|---------|---------|
| `definition` | Key definitions | Light blue box with dark blue frame |
| `exemple` | Numbered examples | Gray box (auto-numbered by chapter) |
| `remarque` | Notes and remarks | White box with orange frame |
| `attention` | Warnings and alerts | Light red box with dark red frame |
| `equationimportante` | Important equations | Light blue with thick border |
| `pratiqueautonome` | In-class practice exercises | Light green box (auto-numbered) |

### Usage Examples

```latex
\begin{definition}
La \textbf{position} d'un objet est...
\end{definition}

\begin{exemple}{Calcul de vitesse}
Un bateau se déplace à 20 km/h...
\end{exemple}

\begin{remarque}
L'origine peut être déplacée selon le contexte.
\end{remarque}

\begin{attention}
Ne pas confondre vitesse et accélération.
\end{attention}

\begin{pratiqueautonome}
Calculez la vitesse moyenne du navire.
\espaceresolution[5cm]
\reponsepratique{15 m/s}
\end{pratiqueautonome}
```

## Custom Commands

### Vector Notation
```latex
\vect{A}              % Vector with arrow: A⃗
\vectcomp{A}{A_x}{A_y} % Vector with components: A⃗ = (Ax, Ay)
\comp{3}{4}           % Components only: (3, 4)
\module{A}            % Magnitude: ‖A⃗‖
```

### Unit Shortcuts
```latex
\ms   % m/s (meters per second)
\mss  % m/s² (meters per second squared)
\kmh  % km/h (kilometers per hour)
\rpm  % tr/min (revolutions per minute)
```

### Calculus
```latex
\ddt{x}  % dx/dt (time derivative)
\ddx{v}  % dv/dx (spatial derivative)
```

### Variables
```latex
\Dt  % Δt
\Dx  % Δx
\Dv  % Δv
```

### Other
```latex
\grandeur{nom}        % Physical quantity in italics
\espaceresolution[6cm] % Space for solutions (default 6cm)
\reponsepratique{val}  % Discrete answer display
```

## Color Palette (IMQ Branding)

```latex
bleuimq     % RGB(0, 82, 147)   - Primary blue (IMQ brand)
orangeimq   % RGB(232, 119, 34) - Orange accent
grisimq     % RGB(128, 130, 133) - Gray
vertexemple % RGB(34, 139, 34)  - Green for examples
rougealerte % RGB(178, 34, 34)  - Red for alerts
bleuclair   % RGB(230, 242, 255) - Light blue background
grisclair   % RGB(245, 245, 245) - Light gray background
vertpratique % RGB(46, 125, 50) - Practice green
vertclair   % RGB(232, 245, 233) - Light green background
```

## TikZ Styles

Pre-defined styles for physics diagrams:

```latex
vecteur        % Blue arrow vector
vecteur rouge  % Red arrow vector
vecteur vert   % Green arrow vector
axe            % Coordinate axis
pointille      % Dashed gray line
angle mark     % Angle marking
```

## Guidelines for AI Assistants

### When Editing Content

1. **Write all content in French** - This includes LaTeX comments, labels, and text
2. **Use the custom environments** - Prefer `definition`, `exemple`, `remarque`, `attention` over manual formatting
3. **Use siunitx for units** - Write `\SI{10}{\meter\per\second}` not `10 m/s`
4. **Use custom vector commands** - Use `\vect{v}` not `\vec{v}` or `\overrightarrow{v}`
5. **Follow the modular structure** - Add new sections as `sec-*.tex` files in the appropriate chapter folder
6. **Update chapter masters** - When adding sections, update `ch#-main.tex` to include them

### When Creating New Content

1. **Create section files** in `chapitres/ch#/` following the `sec-*.tex` pattern
2. **Add to chapter master** by editing `ch#-main.tex`
3. **Use maritime examples** when relevant (ships, ports, navigation)
4. **Include practice exercises** using `pratiqueautonome` environment
5. **Mark exercise difficulty** with stars: ★ (easy), ★★ (medium), ★★★ (hard)

### Document Structure Rules

- Chapters start with `\chapter{Title}`
- Sections use `\section{Title}` and `\subsection{Title}`
- Each chapter folder has its own `ch#-main.tex` that aggregates sections
- Exercises are in separate files in `exercices/`

### Backlog Items (from CHANGELOG.md)

**Chapter 1 - Kinematics**:
- Add 3 graph-reading exercises
- Add note about movable origin (page 47)
- Define "Surface Speed" vs "Bottom Speed" (page 54)
- Move boat+current example for vector decomposition (page 88)

**Chapter 2 - Dynamics**:
- Add pulley examples (Atwood machine, pulley + inclined plane)
- Improve skier diagram
- Improve pedagogical progression (1 force → 2 forces → systems)

### Quality Standards

- Ensure mathematical notation is consistent throughout
- Cross-reference equations and figures with `\cref{}`
- All figures should be in the `figures/` directory
- Test compilation after making changes (run pdflatex twice)

## Version Control

- Current branch for development: `claude/claude-md-mkwt94a7hanolatj-9u3kF`
- Document changes in `CHANGELOG.md` for significant updates
- Commit messages should be in English (Git convention)
