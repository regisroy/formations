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

## Qu'est-ce que spring ?
* Rod Johnson => réaction aux EJB
* 1ère version : 2004 -> 2016
* Version actuelle : 4.3
* Prochaine version majeure : 5.0
* Pourquoi utiliser spring ?
    - pour faire de l'injection de dépendances => ?
    - pour utiliser des classes utilitaires => ?
    - pour vous simplifier la vie => ?
    - pour avoir un container léger => ?
    - pour bénéficier pleinement de [l'éco-système Spring](https://spring.io/projects)

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

## Spring est un framework qui a une opinion
* Il favorise les appplication par couche
* Il favorise le développement avec des tests (Unitaires, Intégration, Fonctionnels, ...)
* Il favorise le développement par contrat
    * utilisation d'interfaces 

.    
.    
.      
.      

## Configuration dans une classe Java
* déclarer la classe de config : `@Configuration`
* déclarer les beans managés : `@Bean`
* le scope d'un bean : `@Scope("xxxx")`
* Application context :  `JavaBasedApplicationContext`

.    
.    
.      
.      

## Configuration par annotations :
* déclarer un bean :
    - les stéréotypes :  `@Commonent` `@Service` `@Repository` `@Controller` 
* injecter un bean
     - `@Autowired`
* un peu de configuration java tout de même
    - `@ComponenScan ("...")`  
* Application context :  `AnnotationConfigApplicationContext`
* ...

.    
.      
.      
.      

## Configuration en xml
* `<bean id="" class=""/>`
* intection par setter : `<property name="" value|ref=""/>`
* injection par contructeur : `<constructor-arg value|ref="" />`
* Application context :  `FileSystemXmlApplicationContext` ou `ClassPathXmlApplicationContext`

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
 
## Gestion des propriétés
* récupération avec bean `Environment`    
* récupération avec `@Value("${xx}")`    
* d'où viennent les propriétés ?
    - JVM System Properties
    - Java Properties Files
    - Servlet Context Parameters
    - System Environment Variables
    - JNDI  
* propriétés stockées dans un fichier `.properties`
    - `@PropertySource ( “classpath:/com/organization/config/app.properties” )`
    - on doit ajouter un bean
```java
@Bean
public  static  PropertySourcesPlaceholderConfigurer
                                  propertySourcesPlaceholderConfigurer() {
         return new PropertySourcesPlaceholderConfigurer();
}
````
.      
.      
.      
.      
.      
.      
 

