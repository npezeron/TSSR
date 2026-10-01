# Comment convertir du binnaire en décimale

## Décomposer le binaire

J'ai commencer par crée une matrice qui me permet de décomposé l'adresse IP en puissance ^2. Après avoir décomposé le nombre en binaire, il suffit de remplacer les 1 et les 0 par les nombres qui leur son associés dans le tableau

### Exemple 
1. 00001111
**Exemple :** `00001111`

| Position (bit) | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|:---------------|--:|--:|--:|--:|--:|--:|--:|--:|
| Valeur         | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
| Bit            | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 |

Calcul : 8 + 4 + 2 + 1 = **15**
  
 Si on veut convertir une adresse IP de binair à décimale il suffit de décomposé par paquer de 8 bit qui est égale à 1 octet et on recommence.

 ---

 # Convertion décimale à binaire 










# Héxadécimale

## Sa création 

