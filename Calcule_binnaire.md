# Comment convertir du binnaire en décimale

## Décomposer le binaire

J'ai commencer par crée une matrice qui me permet de décomposé l'adresse IP en puissance ^2. Après avoir décomposé le nombre en binaire, il suffit de remplacer les 1 et les 0 par les nombres qui leur son associés dans le tableau

### Exemple 
1. Binaire à décimale
**Exemple :** `00001111`

| Position (bit) | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|:---------------|--:|--:|--:|--:|--:|--:|--:|--:|
| Valeur         | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
| Bit            | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 |

Calcul : 8 + 4 + 2 + 1 = **15**

## Convertion de décimal à binaire
2. Décimale à binaire
**Exemple :** `245`

Le principe est le suivant on regarde dans la matrice le plus grand nombre possiblen sans dépacer la valeur du nombre à convertire dans le cas présent 128 est le plus grand nombre disponnible dans la matrice. On le soustrer 245-128 = 117 et recommence le processuce jusqu'a atteindre 0

| Position (bit) | Position (bit) | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|:---------------|--:|--:|--:|--:|--:|--:|--:|--:|
| Valeur         | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
| Bit            | 1 | 1 | 1 | 1 | 0 | 0 | 1 | 1 |

Calcule : 245-128-64-32-16-4-1 = 0
