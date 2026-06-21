# Optimisation mémoire et parallélisation de matrices creuses

Projet de stage sur la représentation efficace de grandes matrices creuses et l’accélération de leur traitement en Python.

## Ce que fait le projet

- Convertit une matrice dense en format CSR
- Réduit fortement l’utilisation mémoire
- Compare une exécution séquentielle et une exécution parallèle
- Mesure les gains sur plusieurs tailles de matrices

## Résultats clés

### Réduction mémoire

| Taille de matrice | Stockage dense | Stockage CSR | Gain mémoire |
|---|---:|---:|---:|
| 1000 x 1000 | 1 000 000 | 10 007 | ~99.0% |
| 2000 x 2000 | 4 000 000 | 20 010 | ~99.5% |
| 5000 x 5000 | 25 000 000 | 50 013 | ~99.8% |

### Temps d’exécution

| Taille de matrice | Version séquentielle | Version parallèle | Accélération |
|---|---:|---:|---:|
| 1000 x 1000 | 2.34 s | 1.17 s | x2.0 |
| 2000 x 2000 | 9.78 s | 4.89 s | x2.0 |
| 5000 x 5000 | 42.56 s | 21.78 s | x1.95 |

## Structure du dépôt

- `src/` : code source
- `results/` : résultats expérimentaux
- `README.md` : présentation du projet

## Technologies

- Python 3
- NumPy
- SciPy
- multiprocessing

## Contexte

Projet réalisé dans le cadre d’un stage de Master 1 en calcul haute performance et simulation.
