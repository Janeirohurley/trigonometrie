Titre : L’astuce des épicycles pour dessiner un cœur

Objectif : comprendre, pas dériver. Utiliser le minimum de math complexe, maximum d’images mentales.

1. Une courbe, c’est comme un stylo qui bouge
On a un stylo. À chaque instant t, on regarde où est le stylo : il a des coordonnées (x(t), y(t)).
Dessiner une forme (ici un cœur), c’est retrouver la trajectoire de ce stylo.

2. L’idée : mettre des roues dans des roues
Imagine que tu fixes une petite roue au bord d’une grande roue. Le stylo est au bord de la petite roue.
Le mouvement résultant trace une courbe. Avec 1 roue : un cercle. Avec 2 : un petit nœud. Avec 3,4,...
on peut s’approcher d’à peu près n’importe quelle forme fermée (cœur, étoile, carré…).

C’est exactement ça : chaque « cercle » = une roue. Sa taille (rayon) change. Il tourne à sa propre vitesse.
La pointe du DERNIER cercle est l’endroit exact du stylo.

3. Comment ça se transmet ?
- Le cercle 1 a son centre en C₀ (le « point de départ »). Il tourne. Sa pointe devient le centre du cercle 2.
- Le cercle 2 tourne autour de ce nouveau centre. Sa pointe devient le centre du cercle 3.
- Etc.
- La pointe du dernier cercle est (x, y) à l’instant t.

Si tu regardes bien dans l’animation : chaque flèche relie un centre à la pointe suivante.
C’est ça que montre le « Scénario : comment les cercles communiquent ».

4. Pourquoi des vitesses différentes ?
Chaque roue tourne « plus vite » ou « plus lentement ». Certains tournent dans l’autre sens (k négatif).
L’animation te montre k > 0 en bleu-étincelant, k < 0 en rose. Tourner en sens inverse permet
de créer des creux, des pointes, des angles (d’où le besoin de vitesses « inversées » pour un cœur).

5. Pourquoi des diamètres différents ?
Certaines roues sont énormes (les premières). Elles définissent la « silhouette » générale.
D’autres sont minuscules. Elles rajoutent les petites bosses, les courbes fines, le détail.
Regarde l’énergie captée : avec 2–3 roues déjà beaucoup ; avec 8–10 ça devient presque identique au cœur.

6. Le passage du temps (t)
t va de 0 à 300 dans l’animation (M=300). Quand t augmente, TOUTES les roues tournent ensemble,
chacune à son propre rythme. C’est ça qui parcourt toute la forme et referme la boucle.

7. x(t) et y(t) séparés
Le mouvement horizontal x(t) et vertical y(t) sont traités séparément par la formule, puis réunis.
Dans « Vue temporelle x(t)/y(t) », la courbe bleue = x, la rose = y au fil du temps. C’est comme
regarder tes pas à gauche/droite et haut/bas indépendamment, pour recomposer la trajectoire.

8. Lire « Détails pas à pas »
- k : à quelle « vitesse » tourne ce cercle (relatif aux autres)
- r : taille du cercle
- φ (phase) : où il pointe à t=0
- θ_k = k*t + φ : angle à cet instant
- dx,dy = (x1-x0, y1-y0) : ce que ce cercle ajoute
- centre → pointe : la transmission (le pont entre cercles)

9. À observer concrètement (exercice)
- N=1 : un seul cercle → forme la plus grossière (ellipse/cercle approchant)
- N=2–4 : silhouette apparaît (renflement du cœur)
- N=5–8 : détails se dessinent
- mode « Vitesse tortue » (0.01×) : tu vois la transmission centre→pointe en temps réel
- « Scénario » : explique un à un le passage de relais

10. L’essentiel à retenir
« La pointe du précédent devient le centre du suivant. Chacun tourne à sa taille et à sa vitesse.
La pointe du dernier dessine le cœur. »

C’est tout. Pas besoin de maîtriser les exponentielles complexes pour comprendre ce spectacle.


## Exemple concret : le cœur

Regardons ce qui se passe concrètement. Pour le cœur, les plus gros « rouages » sont les premiers.

Voici un extrait des coefficients réels (a_k,b_k,c_k,d_k) tels qu'on les voit dans le tableau :
- k=1 : très gros → donne le mouvement principal
- k=-2, k=2, k=3 etc → tailles plus petites → finitions

Quand tu passes N de 1 à 8, tu vois littéralement la forme se fermer. À N=8, le cœur est déjà très proche de la cible.

Dans l’interface, regarde :
- « Énergie captée % » : combien de « puissance » on a déjà prise avec N cercles
- « Erreur RMS / relative % » : à quel point ça colle encore
- « Convergence » : la courbe qui chute brutalement au début, puis doucement

## Pourquoi PAS tous les cercles ?
Si on prenait TOUS les 300, on reproduirait exactement le tracé point par point (très fidèle).
Mais ça deviendrait illisible. L’intérêt pédagogique est justement : **les 5–8 premiers suffisent à reconnaître un cœur**.
Les 20 suivants ne servent qu’à gommer les derniers petits écarts.

## À faire toi-même
1. Charger « Cœur » → N=1 (un cercle), N=3, N=8. Observer.
2. Mettre « Vitesse tortue » (0.01×) + « Scénario » → voir la transmission centre→pointe.
3. Cocher « Repère orthonormé + grille » → voir que les cercles restent bien ronds.
4. Détacher la « Vue temporelle » → comparer x(t), y(t) avec la trajectoire.
