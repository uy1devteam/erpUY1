# Comment contribuer
## Semantique des mots
Nous optons pour des mots ou pour un developpement en anglais 
## Regles de nomenclature  
### Nom des variables et attributs  
Pour la notation des variables et attributs nous utiliserons la notation [lower camel](https://capitalizemytitle.com/camel-case/) avec une preference pour un underscores `_` pour debuter le nom d'un attribut priver ou protected
#### Exemple de definition d'une variavle
``` php
  //variable
  $acountNumber
  
  //attribut priver
  private $_acountNumber
```
### Nom des classes
Nous suivons la notation [upper came](https://capitalizemytitle.com/camel-case/) 
#### Exemple de nomage d'une class
``` php
  class Account
  {
    
  }
```
### Fonctions, procedures et method 
Nous suivons la notation [snake case](https://fr.wikipedia.org/wiki/Snake_case)
``` php
  function inc_account_number()
  {
      
  }
```
### Constantes 
Les constantes sont ecris en majuscule avec des underscores pour separer les parties. pour plus de precision les constantes systems peuvent etre precede de underscores pour plus de distintion
``` php
  define('MAX_ACCOUNT', '100'); 
```
## Definition
### Definition d'une class
Les classes doivent etres commenter pour permettre leur exploitation. Dans le code la docuementation d'une class est faite sous forme de commentaire, il doit y figurer:
- le nom de la class: le nom d'une class est suivit d'une petite description semantique(but) de la class
- le nom de ces attributs: le nom d'un attribut est suivit de son type, de son status(private, public, static ou const) et son sens si possible 
- le nom de des paramettres: le nom des paramettres est suivit de son type de leur status requi ou pas, si oui de la valeur par defaut
- l'auteur: le de nom ou le pseudo de la personne qui a creer la class 
#### Exemple de definition d'une clase
``` php
  /**
    * @autor: fez2000
    * @name: Account 
    * @desciption: classe qui represente le compte d'un user (etudiant, professeur)
    * @params: 
    * -email: email d'un utilisateur
    * @attributes: 
    * -_email: user email
    */
  class Account
{
  private $_email;

  public function __construct($email) 
  {
    $this->_email = $email; 
  }

  // Accesseur chargé de retourner l'attribut $_email.
  public function setForce($force)
  {
  }

  // Mutateur chargé de modifier l'attribut $_email.
  public function set_email($emil)
  {
    this->_email = #email;
  }
}
```
### Definition d'une fonction
Les classes doivent etres commenter pour permettre leur exploitation. Dans le code la docuementation d'une class est faite sous forme de commentaire, il doit y figurer:
- le nom de la fonction
- la description: le nom d'une fonction est suivit d'une petite description semantique(but) de la fonction
- le nom de des paramettres: le nom des paramettres est suivit de son type de leur status requi ou pas, si oui de la valeur par defaut 
- le type de retour: pour preciser le type de retour on ecrit un return suivi du type de retour et d'une description si possible
- l'auteur: le de nom ou le pseudo de la personne qui a creer la fonction 
#### Exemple de definition d'une clase
``` php
  /**
    * @autor: fez2000
    * @name: inc_account_number 
    * @desciption: fonction qui represente le compte d'un user (etudiant, professeur)
    * @params: void
    * @return: void
    */
  function inc_account_number()
  {
      if($_acountNumber < $MAX_ACCOUNT){
        $_acountNumber++;
      }
  }
}
```
# Commit
## regle de commit:
Pour le travail en commun nous optons pour git comme gestionaire de version. le project est de ce fait organiser en trois branches majeurs master, preprod et dev. 
 - master: master est la branche de production, elle est faite pour recevoir les versions du projects qui ont passe les testes. note chaque version de prodution stable apres teste des utilisateurs est tager.
- preprod: proprod est la branche avant production, elle est faite pour recevoir les versions
de l'application a tester. une fois qu'une version passe les testes elle est automatique mise en production.
- dev: dev est la branche de developpement, elle  recoit le code en cour de developpenent. chaque developper dois avoir une sous branche sur dev ou il met sont travail en cour puis la partage avec les autres sur dev.
## hierachie du project:
