# Studio d’épicycles de Fourier

Un petit studio pédagogique pour comprendre visuellement : **une forme fermée = somme de cercles qui tournent**.

## Qu’est-ce que ça montre ?
- **Des roues dans des roues** : chaque cercle tourne autour du précédent. La pointe du dernier dessine la courbe.
- **Taille & vitesse** : les gros cercles donnent la silhouette, les petits ajoutent les détails. Certains tournent en sens inverse.
- **Transmission** : la pointe d’un cercle devient le centre du suivant (clairement montré par le « Scénario »).
- **Repère orthonormé** : cercles bien ronds, grille centrée sur C₀.
- **Vue temporelle** : x(t), y(t) séparés, synchronisés avec l’animation (intégré ou détachable).
- **Analyse** : énergie captée, erreur RMS/relative, convergence, coefficients a_k,b_k,c_k,d_k.

## Lancer en local
Ouvre simplement `index.html` dans ton navigateur (Firefox/Chrome). Aucun build, aucun serveur requis.

## Déployer sur GitHub Pages
1. Crée un dépôt `trigonometrie` sur GitHub
2. Pousse ce dossier dans la branche `main`
3. Dans Settings → Pages, sélectionne « GitHub Actions »
4. Le workflow `.github/workflows/deploy.yml` se déclenche automatiquement
5. L’URL sera `https://TON-USERNAME.github.io/trigonometrie/`

## Comprendre (pas besoin d’être matheux)
- [docs-explication.md](docs-explication.md) — explication simple, imagée, sans jargon lourd
- [docs-explication-detaillee.md](docs-explication-detaillee.md) — plus concret, avec exemple cœur + exercices à faire

## Astuces
- **Vitesse tortue (0.01×)** + **Scénario** : à regarder en premier pour capter l’idée.
- **Repère orthonormé + grille** : rend évident que ce sont bien des cercles.
- **Détacher la vue temporelle** : pratique pour comparer x(t)/y(t) côte à côte.
- **Dentelle** : parfait pour voir l’apport des petits cercles (fréquences négatives).
