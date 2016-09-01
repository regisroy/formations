# Partage sur Spring core #1

* Qu'est-ce que Spring ?
* Configurer spring, 3 façons
    - dans des classes java
    - par annotations
    - dans les fichiers des configuration xml
* Utiliser des propriétés avec spring
    - qu'est-ce qu'une propriété dans spring ?
    - comment récupérer une propriété
.    
.    
.    
.      
.      
.      

## Qu'est-ce que spring ?
* Pourquoi utiliser spring ?
    - pour faire de l'injection de dépendances => ?
    - pour utiliser des classes utilitaires => ?
    - pour vous simplifier la vie => ?
    - pour avoir un container léger => ?
.        
.    
.    
.      
.      

## Le pattern Injection de dépendances
* DI
    - exemple
    - injection de dépendance par 
        - par ...
        - par ...
        - par ...
.     
.    
.    
.      
.      

## Spring est un framework qui a une opinion
* Il favorise les appplication par couche
* Il favorise le développement avec des tests (Unitaires, Intégration, Fonctionnels, ...)
* Il favorise le développement par contrat
.    
.    
.    
.      
.      

## Configuration dans une classe Java
* déclarer la classe de config
* déclarer les beans managés
* Application context
.    
.    
.    
.      
.      

## Configuration par annotations
* déclarer un bean
* injecter un bean
     - injection par méthode
     - injection par paramètre
* un peu de configuration java tout de même
* ...
.    
.    
.    
.      
.      

## Configuration en xml
* <bean id="" class=""/>
* intection par setter : <property name="" value|ref=""/>
* injection par contructeur : <constructor-arg value|ref="" />
.    
.    
.    
.      
.      

## Pourquoi une configuration Xml ou par annotation ou Java ?
* ...
.      
.      
.      
.      
.      
 

