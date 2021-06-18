# projet-c_chiffrement

projet-c_chiffrement est un programme en C permettant le chiffrement et déchiffrement de messages.

## Objectif

L'objectif de ce programme est chiffrer / dechiffrer des messages simples en choisissant entre 2 algorithmes proposés.

* Algorithme de César
    * Le chiffrement de César fonctionne par décalage des lettres dans l'alphabet. Le décalage choisi doit être un entier positif et correspondra à la clé de chiffrement 
    * Pour plus d'informations : https://fr.wikipedia.org/wiki/Chiffrement_par_d%C3%A9calage

* Algorithme de Vigenère
    * La clé de chiffrement est une chaine de caractère préalablement choisi par l'utilisateur. Pour pouvoir chiffrer notre texte, pour chaque caractère nous utilisons une lettre de la clé pour effectuer la substitution.
    * Pour plus d'informations : https://fr.wikipedia.org/wiki/Chiffre_de_Vigen%C3%A8re

## Utilisation

Pour utliser le programe il faut executer les commandes suivante dans la console
```bash
make all
./main
```

## Documentation des Fonctions
```c 
int verifAlphaNum(wchar_t *message)
```
* Retourne 0 s'il y a des caractères spéciaux et 1 sinon.
* Paramètres :
    * *message* représente le message à (dé)chiffrer.

```c
int verifAlpha(wchar_t *message)
```
* Retourne 0 s'il y a des caractères non alphabetiques et 1 sinon.
* Paramètres :
    * *message* représente le message à (dé)chiffrer.

```c   
void replaceAccents(wchar_t *message)
```
* Remplace les accents du message par son équivalence sans accents.
* Paramètres :
    * *message* représente le message à (dé)chiffrer

```c 
void chiffrageCesar(wchar_t *message, int code)
```
* Chiffre le message selon le code
* Paramètres :
    * *message* représente le message à chiffrer
    * *decalage* représente la clé de chiffrement 

```c
void dechiffrageCesar(wchar_t *message, int code)
```
* Dechiffre le message selon le code
* Paramètres
    * *message* représente le message à déchiffrer
    * *decalage* représente la clé de déchiffrement 

```c   
void chiffrageVigenere(wchar_t *message, wchar_t *code)
```
* Chiffre le message selon le code
* Paramètres :
    * *message* représente le message à chiffrer
    * *cle* représente la clé de chiffrement 

```c  
void dechiffrageVigenere(wchar_t *message, wchar_t *code)
```
* Dechiffre le message selon le code
* Paramètres :
    * *message* représente le message à déchiffrer
    * *cle* représente la clé de déchiffrement 

```c   
void affichage(wchar_t *message, wchar_t mode);
```
* Enregistre le message dans un fichier texte
* Paramètres :
    * *message* représente le message à (dé)chiffrer
	* *mode* représente mode de traduction (chiffrage/dechiffrage)

## Cas d'erreurs

A cause de quelques incompréhensions, quelques erreurs de buffer concernant le dépassement des entrées utilisateurs sont présentes.
Lorsque l'on se trompe dans la saisie du décalage, une boucle infinie se crée.

## Auteurs

> [COLOME Charlotte]
> [POMIES Guillaume]

https://framagit.org/LudOo/message_encryption
