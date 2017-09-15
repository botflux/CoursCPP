# CoursCPP
Cours sur le c++


# Pointeurs

Un pointeur est une variable qui contient l'adresse d'une case mémoire pour valeur.

## Synthaxe:

Un pointeur sur une case mémoire aura le même type que la case la
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
    

# Structures

## Déclarer une structure

Une structure se définit de la manière suivante:

    typedef struct nom
    {
       // champs de la structure
    } NomDeLaStructure;
    
nom: Un nom à titre indicatif, ce nom ne sera pas utilisé dans le programme.
NomDeLaStructure: Le nom de la structure dans le programme.

### Exemples:

Création d'une structure "Point" qui va représenter un point dans un espace en 2D.

    typedef struct point
    {
        int x;
        int y;
    } POINT;
    
On pourra utilisé point de cette manière:

    POINT p; // création de la variable du type de la structure
    p.x = valueX; // accès au champs x de la structure point
    p.y = valueY; // accès au champs y de la structure point
