# API

<p class="emphase">Application Programming Interface</p>

- References:

- [Open Classroom](https://openclassrooms.com/fr/courses/6573181-adoptez-les-api-rest-pour-vos-projets-web/6816951-initiez-vous-au-fonctionnement-des-api)

- [Github Rest API Doc](https://docs.github.com/en/rest/pages?apiVersion=2022-11-28)


- [API to generate tables from github issues](https://datatables.net/examples/plug-ins/api.html)

## Introduction

Les API créent des méthodes **standardisées** et **réutilisables** qui permettent aux développeurs d’accéder à des données spécifiques lors de la construction d’applications.

```{figure} Docs/web_API_OC.png
---
width: 100%
name: API-Explained
---
Une conversation entre le client, l'API et la base de données
```

### API Privés

> Une API privée permet uniquement aux utilisateurs autorisés au sein de votre entreprise ou de votre application d'utiliser l’API qui peut accéder à la base de données.

Une API permet un niveau de sécurité supplémentaire pour mieux gérer l’accès et les modifications des données, en attribuant ce qu’on appelle des droits aux personnes qui en ont besoin. Ainsi, on s’assure de contrôler les utilisateurs qui auront ou non accès à la base de données.


### API Publics

Contrairement aux API privées, les API que l’on appelle publiques sont utilisables par d’autres personnes, qu’elles soient sur votre application ou non. Elles permettent aux développeurs de récolter les données d’une autre application pour améliorer ou enrichir leurs propres projets sans autorisation stricte. Il existe de nombreuses manières d’utiliser des données provenant d’API tierces (ou externes).


- [Liste API publiques](https://github.com/toddmotto/public-apis?tab=readme-ov-file)

```{note}

Checker pour voir si il y en a que l'on peut utiliser

- API 1
- API 2

```


### API SOAP

- Simple Object Access Protocol



### API REST

- Representation state transfer

Il y a six lignes directrices architecturales clés pour les API REST. Voyons ensemble de quoi il s’agit:


#### Client-serveur separation


#### Stateless

#### Cacheable 

(ou sauvegardable, en français)


#### Uniforme Interface



#### Layered system 

(système de couches)

#### Layered system (système de couches)



#### Code on demand (code à la demande)



## API Rest


### URI and Endpoint

- [Exemple](https://anapioficeandfire.com/)


### XML and JSON

Les données des API REST peuvent utiliser deux langages : XML et JSON. Si une API renvoie un set de données en XML ou en JSON, le contenu restera le même, mais la forme change. Le format de données est différent.

#### XML

En XML, chaque élément de donnée a une balise ouvrante et une balise fermante qui peut également avoir des balises imbriquées:

```xml

<series>
  <serie>    <titre>Game Of Thrones</titre>
    <realisateur>Random</realisateur>
  </serie>
       <serie>    <titre>Peaky Blinders</titre>    
<realisateur>Random</realisateur>  </serie>
</series>


<series>
  <serie>
     <titre>Game Of Thrones</titre>
     <realisateur>Random</realisateur>
  </serie>
  <serie>
     <titre>Peaky Blinders</titre>
     <realisateur>Random</realisateur>
  </serie>
</series>


```

#### JSON

```json

{ "series": [
  {   "titre": "Game Of Thrones",
    "realisateur": "Alan Taylor" },  {   "titre": "Peaky Blinders",
    "realisateur": "Otto Bathurst" }  ]
}

```


## Formuler une requette

- On utilise le logiciel [Postman](https://www.postman.com/)

```{note}

Checker les alternatives et analyser quel est la meilleure solution

```

### La structure d’une requête

Chaque requête a une structure spécifique qui a cette forme :

- Verbe HTTP + URI + Version HTTP + Headers + Body (facultatif)


```{figure} Docs/requette-OC.png
---
width: 100%
name: requette-OC
---
Une structure de requête typique
```

#### Le verbe

Commençons avec le verbe. Les verbes HTTP correspondent à différents types d’actions que vous pouvez accomplir avec votre requête. Ceux que vous rencontrerez le plus couramment sont GET (obtenir), PUT (mettre), POST (publier), et DELETE (supprimer). Ne vous y attardez pas trop pour le moment, nous les étudierons tous plus en détail plus tard !

- Get
- ...

#### L’URI