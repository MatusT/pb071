# Písanie dokumentácie

Doxygen podporuje niekoľko formátov, v ktorých je možné dokumentáciu písať. V tomto tutoriále sa obmedzíme na formát JavaDoc. Dokumentácia sa píše iba do **.h** súborov!

## Súbor

V každom súbore začnite jeho opisom, názvom a autorom:

```
/**
 * @brief   description of the file
 * @file    name.h
 * @author  TutorialMaster
 */
```

## Funkcia

Pre zdokumentovanie funkcie sa používa:
- **@brief** pre opis funkcie
- **@param** pre zadefinovanie parametra
- **@return** pre opis toho, čo funkcia vracia

```
/**
 * @brief sums two elements
 * @param a first summand
 * @param b second summand
 * @return sum of two elements
 */
```

## Structure, Enum

Pre zdokumentovanie jednotlivých prvkov vo výčtovom type(**Enum**) alebo štruktúre, sa používa syntax:
** /\*\*< opis prvku \*/ **

```
/**
 * @brief Doubly linked list node.
 */
typedef struct node
{
    struct node *prev; /**< previous node        */
    struct node *next; /**< next node            */
    void        *data; /**< pointer to node data */
} node_t;

typedef enum mode
{
    Read    = 1, /**< read a file or list contents of a directory */
    Write   = 2, /**< modify a file or directory entries          */
    Execute = 4  /**< execute a file or enter a directory         */
} mode_t;
```
# Kam ďalej

Pokračujte [vygenerovaním dokumentácie](./generate.md).