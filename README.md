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
    
## Passer en paramètre une structure

Pour pouvoir passer en paramètre d'une fonction une structure, il faut utiliser
un pointeur sur l'instance de la structure.

### Exemples:

    POINT p;
    POINT *ptr = &p;
    
    funct(ptr);
    
    // signature de la fonction
    void funct (POINT *ptr);
    
# Classes:

Les classes sont les élèments centraux de tout programme C++.Tout les programmes en C++ en sont composés.

## Qu'est ce qu'une classe:

Une classe désigne un type plus complexe que les types valeurs (float, int par exemple). Une classe contient:

- des variables, appelées champs ou attributs de la classe;
- des fonctions, appelées méthodes, qui vont effectuer des opérations sur les champs de la classe;
- des propriétés et des indexeurs.

 ## Les objects:
 
 Une classe consiste en une définition d'informations, à l'usage du compilateur. L'objet tant qu'à lui représente une variable du type de la classe donnée. On parle aussi d'instance et d'instanciation de la classe, qui désigne l'opération de création d'un objet.
 
 Lors de l'instantiation la classe devient concrète, c'est-à-dire que l'instance occupe de la place en mémoire lors de l'éxecution du programme.
 
 ## Définition d'une classe:
 
 La définition d'une classe est séparée en deux fichiers:
 
 - Le fichier d'en-tête, ce fichier contient les champs de la classe c'est-à-dire ses variables membres, ansi que l'en-tête de chaque fonction;
 - Le fichier source, ce fichier contient le corps des éléments définit dans le fichier d'en-tête, par exemple le fichier source va contenir le contenu des méthodes de la classe.
 
 
