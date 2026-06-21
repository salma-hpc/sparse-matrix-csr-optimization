# Implémentation du format CSR pour matrices de connectivité

Projet de stage portant sur l’implémentation du format **CSR (Compressed Sparse Row)** pour la représentation et la manipulation de matrices creuses de connectivité.

## Objectif

- Convertir une matrice dense vers le format CSR
- Réduire l’empreinte mémoire
- Accélérer certaines opérations
- Tester une version parallèle avec `multiprocessing`

## Fonctionnalités

- Conversion Dense \(\rightarrow\) CSR
- Stockage via `values`, `col_indices`, `row_ptr`
- Benchmark séquentiel vs parallèle
- Génération de résultats expérimentaux

## Résultats

### Réduction mémoire

| Taille | Dense | CSR | Gain |
|---|---:|---:|---:|
| 1000 x 1000 | 1 000 000 | 10 007 | ~99.0% |
| 2000 x 2000 | 4 000 000 | 20 010 | ~99.5% |
| 5000 x 5000 | 25 000 000 | 50 013 | ~99.8% |

### Performance

| Taille | Séquentiel | Parallèle | Speedup |
|---|---:|---:|---:|
| 1000 x 1000 | 2.34 s | 1.17 s | x 2.0 |
| 2000 x 2000 | 9.78 s | 4.89 s | x 2.0 |
| 5000 x 5000 | 42.56 s | 21.78 s | x 1.95 |

## Structure

- `src/` : implémentation Python
- `results/` : logs, graphes, sorties expérimentales
- `.gitignore`
- `README.md`

## Technologies

- Python 3
- NumPy
- SciPy
- multiprocessing

## Contexte

Stage de Master 1 — Calcul Haute Performance et Simulation
