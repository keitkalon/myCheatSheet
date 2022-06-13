# Javascript

Functions Insectarium


## FETCHING
----------------------

### 1) get Api
![GetApiDisplay](https://user-images.githubusercontent.com/79155265/163145020-f1b78a38-9c02-4f1a-9f56-1e7921ffae84.png)


### 2) get Api with display
![GetApiDisplay2](https://user-images.githubusercontent.com/79155265/163145034-dedd2c45-2968-4404-83a3-e3cc50852765.png)


<br><br><br><br>


## CALLBACK
------------------------

### 1) Callback
![Callback](https://user-images.githubusercontent.com/79155265/163054596-55ab86f9-4b8e-4d60-9e55-2efc1c3ca979.png)


### 2) Closure Callback
![ClosureCallback](https://user-images.githubusercontent.com/79155265/163055137-56793490-ff11-49a8-a2d1-0f5c0d363aa1.png)


<br><br><br><br>


## Closure
-----------------------------

### 1) Closure with a centrelize variable
![ClosureCentralizeVariable](https://user-images.githubusercontent.com/79155265/163054822-630da148-2933-4ac2-aa95-1f6838bce6cb.png)


### 2) Closure Efficency
![ClosureEfficiency](https://user-images.githubusercontent.com/79155265/163054863-8df9645d-5fdb-4e84-b391-cd3b6dd45b16.png) 


### 3) Closure Memoization
![ClosureMemoization2](https://user-images.githubusercontent.com/79155265/163055090-e68cf8f7-ce70-4a91-b8e5-e2e2c683b068.png)


### 4) Closure Memoization
![ClosureMemoization](https://user-images.githubusercontent.com/79155265/163055241-822ff2d8-1438-4eb2-a9b0-7a750ac77e09.png)


### 5) Closure Memoizing the methods of an Object
![ClosureObjectAction](https://user-images.githubusercontent.com/79155265/163055051-7d2e8bac-90dd-4539-bea6-4f1dcd232650.png)


### 6) Closure two step function
![Closure2StepFunction](https://user-images.githubusercontent.com/79155265/163055118-41cd5f09-32e3-4017-ae29-06af7dc04eac.png)


<br><br><br><br>


## HighOrderFunctions
--------------------------------------

### 1) Compose function
![ComposeFunction](https://user-images.githubusercontent.com/79155265/163054925-5e06e6e8-6aa2-458a-85d4-b4af393aa6bc.png)


### 2) Currying function
![CurryingFunction](https://user-images.githubusercontent.com/79155265/163054933-27e8beed-cf38-4ac3-b535-c020560885f8.png)


<br><br><br><br>


## Construction Function
------------------------------------

### 1) Construction Function with methods attach to Prototype
![ConstructorFunctionWithPrototypeMethods](https://user-images.githubusercontent.com/79155265/163156537-764e3a72-887e-4991-949a-5b3eb5d1ea3d.png)


### 2) Construction Function created with Function Object
![ConstructorFunctionCreatedWithFunctionObject](https://user-images.githubusercontent.com/79155265/163157703-5804021c-d22f-4f72-a050-ecf0a78413ed.png)


### 3) Factory Function with methods in object
![FactoryFuncProtoAction](https://user-images.githubusercontent.com/79155265/163154061-0442c0bf-271b-4dfd-9aa2-1096c404938a.png)


### 4) Factory Function with methods in proto
![FactoryFuncProtoAction](https://user-images.githubusercontent.com/79155265/163153771-e5961c5a-efd9-4fb5-928e-2c0a4fb47326.png)


<br><br><br><br>


## Objects
-------------------------------------

### 1) Create a simple object
![CreateSimpleObject](https://user-images.githubusercontent.com/79155265/163055319-6a5ba1c0-b345-4a6e-899e-b51f99cff3ba.png)


### 2) Clone an object created with Class word
![CloneClassObjects](https://user-images.githubusercontent.com/79155265/163054735-b8fee9de-a2c3-4ff6-a0ab-3952b8a0f8db.png)


<br><br><br><br>


## Class
------------------------------------

### 1) Class inheritance
![ClassInheritance](https://user-images.githubusercontent.com/79155265/163054669-58ef70c6-5651-42c5-a995-70ce9166f136.png)


### 2) Class get methods and private variable
![classMethods](https://user-images.githubusercontent.com/79155265/163054764-ccb2f928-b3a1-4326-87e6-6172b32ebfae.png)


<br><br><br><br>


## Algorithms
----------------------------------

### 1) Recursive Factorial
![recursiveFactorial](https://user-images.githubusercontent.com/79155265/163054962-b55b7b0c-fd79-4597-95ee-466ce2e9c9af.png)


### 2) Merge Sort
![mergeSort](https://user-images.githubusercontent.com/79155265/163054302-a1ce9b4d-13ae-4f98-89db-bc1370d5dacf.png)


### 3) Buble Sort
![bubleSort](https://user-images.githubusercontent.com/79155265/163054261-dbbd8353-2621-47b1-98b5-2ab4743f193f.png)


### 4) Selection Sort
![selectionSort](https://user-images.githubusercontent.com/79155265/163054334-9788f5ad-d6c8-496b-ab41-d3720b9c8bb0.png)


### 5) Insertion Sort
![insertionSort](https://user-images.githubusercontent.com/79155265/163054288-690579e8-97bb-4ec1-8369-d83656fe34b1.png)


<br><br><br><br>


## Regex
--------------------------------------




# PostgreSQL 
---------------------------

```postgresql
CREATE TABLE "profile"(
  id SERIAL PRIMAY KEY,
  name VARCHAR(100),
  email VARCHAR(255),
  password TEXT,
  age INT
);

INSERT INTO "profile"(
  email, name, age, password
) VALUES ('troy@fake.email', 'Troy',
26, 'Password123');

UPDATE "profile" SET age = 30 WHERE id = 1;

SELECT name, age, email FROM "profile" WHERE id = 1;

DELETE FROM "profile" WHERE id = 1;

CREATE TABLE post(
  id SERIAL PRIMARY KEY,
  name VARCHAR(255),
  content TEXT,
  CONSTRAINT fk_profile
      FOREIGN KEY(profile_id)
          REFERENCES "profile" (id));
          
  INSERT INTO post (name, content, user_id)
  VALUES ('Dogs', 'I lov Akita', 1)
  
  SELECT "profile".*, post.id, post.name AS
  title, post.content, post.profile_id FROM
  "profile" JOIN post
  ON post.profile_id = "profile".id; 

```
---------------------------

```sql:
SELECT shows.title, count(s.show_id)
from shows
left join seasons s on shows.id = s.show_id
group by shows.id
having count(s.show_id) > 20
order by count(s.show_id) desc;

SELECT s.title,
       count(e.id)
FROM shows s
LEFT JOIN seasons z ON z.show_id = s.id
LEFT JOIN episodes e ON e.season_id = z.id
GROUP BY s.title
HAVING count(e.id) <= 4
ORDER BY count(e.id) DESC;

SELECT title, extract(year from year),  rating
FROM shows
LEFT JOIN show_genres sg on shows.id = sg.show_id
LEFT JOIN genres g on sg.genre_id = g.id
where g.name ilike  'animation'
order by rating  desc
limit 10p

SELECT shows.title,  shows.rating::numeric(9,2),  COUNT(e.id) AS total_episodes
FROM shows
LEFT JOIN seasons s on shows.id = s.show_id
LEFT JOIN episodes e on s.id = e.season_id
GROUP BY shows.title, shows.rating
ORDER BY total_episodes DESC
Limit 10;

SELECT shows.title, extract(year from shows.year) as year,
                   shows.rating::varchar(5),
                   COUNT(e.id) AS total_episodes
            FROM shows
            LEFT JOIN seasons s on shows.id = s.show_id
            LEFT JOIN episodes e on s.id = e.season_id
            GROUP BY shows.title, shows.rating, year
            ORDER BY total_episodes desc
            Limit 10;


SELECT g.name, json_object_agg(actors.name,sc.character_name)
    FROM actors
    INNER JOIN show_characters sc on actors.id = sc.actor_id
    INNER JOIN show_genres sg on sc.show_id = sg.show_id
    INNER JOIN genres g on g.id = sg.genre_id
    WHERE g.name = 'Adventure'
    GROUP BY g.name
    LIMIT 20;

SELECT name, birthday, death
FROM actors
WHERE death is null
limit 100;


SELECT shows.title, COUNT(e.id)
FROM shows
LEFT JOIN seasons s on shows.id = s.show_id
LEFT JOIN episodes e on s.id = e.season_id
GROUP BY shows.id
order by count(e.id) desc;

SELECT actors.name, count(sc.character_name) as number, array_agg(sc.character_name) as characters
FROM actors
left join show_characters sc on actors.id = sc.actor_id
group by actors.id
order by count(sc.character_name) desc
limit 10;

SELECT s.title, s.rating, g.name
FROM shows s
LEFT JOIN show_genres sg ON s.id = sg.show_id
INNER JOIN genres g on g.id = sg.genre_id
WHERE g.name = 'Action'
ORDER BY s.rating desc;

SELECT EXTRACT(YEAR FROM shows.year) AS years,round(avg(shows.rating),2), count(shows.id), array_agg(shows.title)
FROM shows
WHERE EXTRACT(YEAR FROM shows.year) BETWEEN 1970 AND 2021
GROUP BY years;

SELECT name, coalesce(age, 0) as age,  case when (subquery.age is null) then 'unknown' else status end
FROM (SELECT actors.name,
       case when actors.death is null then date_part('year',age(now(),actors.birthday)) when actors.death is not null then date_part('year',age(actors.death, actors.birthday)) end as age,
       case when actors.death is null then 'alive' else 'death'end as status

FROM actors ) subquery;


SELECT shows.id, shows.title, count(seasons.id)
FROM shows
LEFT JOIN seasons ON shows.id = seasons.show_id
group by shows.id
having count(seasons.id) >= 7;

SELECT s.id, array_agg(actors.name)
FROM actors
join show_characters sc on actors.id = sc.actor_id
join shows s on sc.show_id = s.id
where s.id = 10219
group by s.id;

SELECT actors.name, date_part('year',age(now(),actors.birthday))
FROM actors
join show_characters sc on actors.id = sc.actor_id
where sc.show_id = 60300
order by actors.birthday

SELECT Extract(year from shows.year), json_object_agg(a.name , date_part('year', age(now(),a.birthday)))
FROM shows
LEFT JOIN show_characters sc on shows.id = sc.show_id
INNER JOIN actors a on sc.actor_id = a.id
group by shows.year;

SELECT actors.name, date_part('year', age(now(), actors.birthday)) as actor_age, date_part('year', age(now(), s.year)) as show_year, actors.birthday
FROM actors
inner join show_characters sc on actors.id = sc.actor_id
inner join shows s on sc.show_id = s.id
where extract(year from s.year) = 1972 and date_part('year', age(now(), actors.birthday)) - date_part('year', age(now(), s.year)) > 0
order by date_part('year', age(now(), actors.birthday)) desc;

SELECT s.id, s.title, count(sea.id)
FROM shows s
LEFT JOIN seasons sea ON s.id = sea.show_id
GROUP BY s.id, s.title
ORDER BY count(sea.id) desc
limit 1



SELECT shows.id, shows.title, date_part('year',shows.year)
FROM shows
INNER JOIN show_genres ON shows.id = show_genres.show_id
INNER JOIN genres g on g.id = show_genres.genre_id
WHERE date_part('year',shows.year) BETWEEN 2000 AND 2010 and g.name = 'Horror';


SELECT actors.name
FROM actors
RIGHT JOIN show_characters sc on actors.id = sc.actor_id
RIGHT jOIN shows s on sc.show_id = s.id
WHERE show_id = 2
```

# CSharp
---------------------------


## Controller
-----------
### 1) CRUD 

![CRUDController](https://user-images.githubusercontent.com/79155265/173386701-96ab5c5e-4f1b-4ea6-9839-f5a3669b976d.jpg)

![CRUDController2](https://user-images.githubusercontent.com/79155265/173386726-c9e7df81-43a8-4552-8ded-93a05da21acd.jpg)



## TypeConversion
-----------
### 1) is 
![TypeConversion_Is](https://user-images.githubusercontent.com/79155265/172614575-4b6d594c-485b-42bd-9d40-0001d2a16cb3.jpg)

## Microservices
-----------

### 1) Controller
![Services_CreateTrroghServives_Controller1](https://user-images.githubusercontent.com/79155265/173380521-6b1f4446-c23f-4bb9-8c9b-a8b7bd12255e.jpg)

![Services_CreateTrroghServives_HttpConecter](https://user-images.githubusercontent.com/79155265/173380546-6bff53a2-dc3b-41ef-8f3d-6179fec7b287.jpg)

### 3) Start DependecyInjection HttpConecter
![Services_CreateTrroghServives_StartAddDependecyInjection](https://user-images.githubusercontent.com/79155265/173380634-a44ec365-04bd-4e99-b36c-54d7cffff5ea.jpg)

### 4) Start DependecyInjection Mapper
![Services_CreateTrroghServives_Mapper](https://user-images.githubusercontent.com/79155265/173380600-e63417bc-f1e9-46a3-bc15-5f2ba72ac544.jpg)


## JSON Read & Write
![Read_Write_JSON](https://user-images.githubusercontent.com/79155265/173387304-38a5ce8a-a381-44bf-99c7-4aa619fbc353.jpg)



## String
-----------

### 1) StringBuilder
![String](https://user-images.githubusercontent.com/79155265/172612622-2784a771-f8d8-4142-8ae3-d427eb59d55e.jpg)


## Patterns

### 1) Singleton
![Singleton](https://user-images.githubusercontent.com/79155265/172615200-d621df86-94b2-4dcc-9cf8-a677b38c7407.jpg)

### 2) Singleton
![Singleton](https://user-images.githubusercontent.com/79155265/172615270-1d91fa61-1200-45f5-bc7d-80840c106fa2.png)


### 3) Factory


## .Net

### 1) Authorization Controller
![ControllersAuthorization](https://user-images.githubusercontent.com/79155265/173386820-c71427fb-9670-4e5d-ba1d-c057e7803114.jpg)

### 2) Authorization
![Authorize_Authentication](https://user-images.githubusercontent.com/79155265/172615492-21aa8892-b5c3-4891-b684-b74b80d6b505.jpg)

### 3) Authorization
![Authorization](https://user-images.githubusercontent.com/79155265/172615554-4c4f77b7-6e74-4e98-97ac-a0c917dcecc7.jpg)


## Utilities
-----------

### 1) Distances
![Distances](https://user-images.githubusercontent.com/79155265/172614829-01e895bb-c7b1-49fc-82b8-a959b27bdc85.jpg)

### 1) Distances BetweenCities
![DistanceBetweenCities](https://user-images.githubusercontent.com/79155265/172614916-3fb24e95-f52f-4cf6-843e-11dfbcdad918.jpg)



## Delegate & Events
-----------

### 1) Delegate & Event Classic
![Events_Classic](https://user-images.githubusercontent.com/79155265/172613030-23e764c1-3aa9-4f41-a014-ca9ccbca456a.jpg)

### 2) Delegate & Event EventHandler 
![Events_with_EventHandler](https://user-images.githubusercontent.com/79155265/172613652-7287ebf8-e7f8-4ce2-87a3-2ac91483302b.jpg)



### 3) Delegate & Event Action
![Events_Actions](https://user-images.githubusercontent.com/79155265/172613138-c718c7e8-dd2b-403c-8bff-fed7a357a89a.jpg)


### 4) Delegate & Event Action Static
![Events_StaticActions](https://user-images.githubusercontent.com/79155265/172613241-84be17d9-4cc3-4dd6-af35-9f09fde7d8c3.jpg)


### 5) Delegate & Event Action No-Parameters
![Events_with_ActionNoParameter](https://user-images.githubusercontent.com/79155265/172613347-f1118ba4-3b94-4cf7-b292-83c03c99e960.jpg)


### 6) Delegate & Event Action with Parameters
![Events_with_ActionWithParameter](https://user-images.githubusercontent.com/79155265/172613429-f545718e-ba61-4329-af6b-45449d554c63.jpg)

### 6) Delegate & Event Func with returnig string
![Events_with_FuncAndReturningString](https://user-images.githubusercontent.com/79155265/172614041-803ddcbd-591e-4aa0-9ecf-7b40f8c03e9d.jpg)

## Model

![Model](https://user-images.githubusercontent.com/79155265/173387894-cb1c16c6-7e4a-4f44-a87c-5f8323617507.jpg)



## Sample

### 1) Ceas
![Ceas](https://user-images.githubusercontent.com/79155265/172615639-30ad4d89-fcc3-43e4-a346-40f8d563ef93.jpg)

### 1) Ceas
