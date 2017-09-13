# CoursCPP
Cours sur le c++


# Pointeurs

Un pointeur est une variable qui contient l'adresse d'une case mémoire pour valeur.

## Synthaxe:

Une variable qui pointe sur une case mémoire aura le même type que la case la
mémoire pointée. Cependant il faut ajouter une étoile (\*) avant l'identificateur.

### Exemple:

La déclaration d'un pointeur sur un entier:

    int *int_Ptr;

La déclaration d'un pointeur sur un double:

    double *dbl_Ptr;

## Assigner une adresse à un pointeur:

Pour pouvoir assigner une adresse à un pointeur, il faut utiliser l'opérateur
(&) avant le nom de la variable. 

### Exemple:

Assignation pour un entier:

    // entier a assigner
    int entier = 2;
    // pointeur
    int *ptr;
    // assignation du poiteur
    ptr = &entier;

## Accéder à la valeur pointée:

Pour accèder à la valeur pointée, il suffit de faire précéder l'identificateur du
pointeur par une étoile (\*).

### Exemple:

    int i = 5; // i = 5
    int *ptr = &i; // ptr vaut l'adresse de i
    int j = *ptr; // j vaut la valeur pointée par ptr soit 5
    
