# Challenge Data Analyst

El objetivo del presente proyecto es explorar patrones para armar el mejor equipo de fútbol, considerando a los futbolistas de 11 ligas Europeas. 

## Descripción de la base de datos.

Se cuenta con una base de datos con más de 25.000 partidos y 10.000 jugadores de ligas Europeas, del año 2008 hasta el 2016.


<div align="center">

|Tabla            | N° Observaciones| N° columnas |
|:---------------:|:------:|:--:|
|Country	        |11	     |2   |
|League	          |11	     |3   |
|Match	          |25979	 |115 |
|Player	          |11060	 |7   |
|Player_Attributes|183978	 |42  |
|Team	            |299	   |5   |
|Team_Attributes	|1458	   |25  |
  
</div>

## Características de las ligas Europeas. 

  En las tablas Match, League, Country y Team, se encuentra información de 11 ligas Europeas, de las temporadas 2008/2009 hasta 2015/2016. 
  
  Según el informe elaborado por la Federación Internacional de Historia y Estadística de Fútbol (IFFHS), que presnrea una clasificación anual de las ligas del mundo, se presenta a las ligas de España, Alemania, Inglaterra, Francia e Italia, como aquellas que se encuentran entre las mejores ligas del mundo. (Fuente: [Clasificación mundial de ligas nacionales de la IFFHS](https://es.wikipedia.org/wiki/Anexo:Clasificaci%C3%B3n_mundial_de_ligas_nacionales_de_la_IFFHS)).

<div align="center">
  
|País   | N° Partidos|
|:------:|:--------:|
|England        |3040|
|France         |3040|
|Spain          |3040|
|Italy          |3017|
|Germany        |2448|
|Netherlands    |2448|
|Portugal       |2052|
|Poland         |1920|
|Scotland       |1824|
|Belgium        |1728|
|Switzerland    |1422|
  
</div>

  La mayor cantidad de partidos jugados en cada una de las ligas, tiene directa relación con la cantidad de equipos participantes en cada uno de los torneos. Las ligas de Inglaterra, Francia y España, son las que presentan mayor cantidad de partidos, y cuentan con 20 equipos, por cada temporada. Además, en estas 5 ligas se presenta una mayor cantidad de goles en la temporadas señaladas, lo que las hace atractivas para los asistentes a los partidos, televidentes, para quienes emiten estos partidos por televisión. Un caso particular, es la liga de "Netherlands" quien cuenta con 18 equipos en el torneo, con una cantidad importante de goles entre las temporadas desde 2008 al 2016, pero que no esta presente dentro de las ligas más destacadas en el ranking elaborado por IFFHS. 

  
   <div align="center">

  ![goles por liga ](https://github.com/Aleskies/Challenge_Data_Analyst/blob/main/imagenes/total_goles_xpais.png)
   
   </div>

   A continuación, se presenta un resumen de los goles anotados por equipos locales y visitas, en las temporadas que van desde el 2008 hasta el 2016, donde los respetivos promedios de goles están ordenados de forma descendente   

   <div align="center">

  ![goles por liga ](https://github.com/Aleskies/Challenge_Data_Analyst/blob/main/imagenes/resumne_ligas.png)
   
   </div>

   Nuevamente aparece la liga de "Netherlands" destacada con un mayor promedio de goles, mientras que	la liga de "Switzerland" aparece en segundo lugar.	

## Exploración de la información de los jugadores. 

### Filtros y Selección de variables, para selección de jugadores.
  
  La base de datos Player y Player_Attributes, presenta características de jugadores de fútbol, de 11 ligas Europeas, donde se extraerá la información necesaria para conformar un equipo. 


  #### - Supuestos y seleción de la muestra.
  
  Como ya se mencionó, la base de datos contiene información de los jugadores hasta el año 2016. Con esta información en mente, se considerará que el equipo que se presenta en este trabajo, está formado para la temporada 2017 con las características y valor de indicadores estadísticos de los jugadores del año 2016.
  
  #### - Filtros
  
  Con la información de los jugadores del año 2016, se procede a identificar y excluir las observaciones duplicadas, junto con aquellas que tienen alguna información perdida en alguna de sus columnas. Luego se realiza un análisis de correlación, utilizando el coeficiente de Spearman que tiene la característica de ser nás robusta a valores extremos. 
  
  Una vez obtenido los valores de las correlaciones, se excluyen aquellas variables que tienen una correlación mayor o igual a 0.70. A continuación, con las variables numéricas que quedaron del paso anterior, se realiza un cluster con 5 agrupaciones, que tiene como finalidad poder escoger un cantidad de jugadores de cada uno de los grupos, de modo que el conjunto obtenido sea un poco más heterogéneo, y puedan complementar sus habilidades.
  
  Un pequeño resumen de las caracteristicas de cada uno de los 5 grupos se presenta a continuación

  <div align="center">

  ![Cluster](https://github.com/Aleskies/Challenge_Data_Analyst/blob/main/imagenes/resumen_5_cluster.png)
  
  </div>

  Obtenido los 5 grupos de jugadores, se realiza la siguiente clasificación en cada uno de ellos.

  Grupo 0. De este grupo no se recluta ningun jugador
  
  En el grupo se observan jugadores de estatura media 189.11 cm, y con altas puntuaciones en las variables 'reactions', 'jumping' y 'strength', que no tiene relación directa con el dominio del balón. Presenta las más bajas puntuaciones, en la mayoria de las características de los jugadores de los cuatro grupos restantes. Por ejemplo, los valores de los indicadores free_kick_accuracy y finishing, son 14.313580 y 13.466667, que son los más bajos de los cinco grupos, y que tienen relación con características de definición frente al arco rival. Esto nos suguiere que quizá sus habilidades no estan relacionadas con hacer goles, quizá poseen caracteristicas más defensivas, pero en el caso de los indicadores de marking o standing_tackle, también presentan los valores más bajo de los grupos. Al nalizar los datos de este grupo, se presentan nombres de arqueros y quien presenta una mayor puntuación en 'reactions', 'jumping' y 'strength', es

   <div align="center">
  
   ![Grupo 0](https://github.com/Aleskies/Challenge_Data_Analyst/blob/main/imagenes/grupo_0_1.png)

   </div>


  Grupo 1. Se escogen 2 jugadores

  La media de estatura de este grupo de jugadores es 185.70 cm, y se organizan las siguiente variables en busca de 2 jugadores, con características más defensivas. Se consideran las mayores puntuaciones de las características de 'strength', 'jumping', 'stamina','aggression','sprint_speed' y 'long_passing', la selección corresponden a:


  <div align="center">
  
  ![Defensas grupo 1](https://github.com/Aleskies/Challenge_Data_Analyst/blob/main/imagenes/grupo_1_2.png)

  </div>

  Grupo 2. Se escogen 2 jugadores 

  Se escogen 2 jugadores en función de las mejores puntuaciones de las características 
  'finishing', 'heading_accuracy', 'sprint_speed', 'agility', 'reactions', 'aggression' en ese orden de prioridad. El propósito es escoger jugadores que tengan una mejor puntuación en característica relacionadas con jugadores más ofensivos, diferenete a la selección aneterior.  Se obtienen los siguientes resultados.

  <div align="center">
  
  ![Grupo 2](https://github.com/Aleskies/Challenge_Data_Analyst/blob/main/imagenes/grupo_2_2.png)

  </div>

  
  Grupo 3. Se escogen 4 jugadores 

  Este grupo de jugadores se caracteriza por tener tener una mayor habilidad en el dominio del balón y distribución de juego. Son aquellos jugadores que tienen las siguientes características: 'free_kick_accuracy', 'long_passing', 'sprint_speed' y 'agility', que son las que fueron consideradas para la selección de 3 jugadores, que son:

  <div align="center">
  
  ![Grupo 3](https://github.com/Aleskies/Challenge_Data_Analyst/blob/main/imagenes/grupo_3_4.png)

  </div>

  Grupo 4. Se escogen 3 jugadores  

  Este grupo esta integrado por aquellos jugadores que tienen mayor puntuación en las siguientes características 
  'crossing', 'free_kick_accuracy', 'long_passing', 'sprint_speed' y 'reactions', de caracter más ofensivo, complementando la selección realizada en el grupo anterior. 
  
    <div align="center">
  
  ![Grupo 4](https://github.com/Aleskies/Challenge_Data_Analyst/blob/main/imagenes/grupo_4_2.png)

  </div>


  ## Selección del equipo ideal.
  
  El grupo de 11 jugadores corresponde a:
  
  <div align="center">
  
  |     **Jugador**        | Posición |
  |:----------------------:|:-------:|
  |Christopher Samba |defensa     |
  |George Elokobi    |defensa      |
  |Gonzalo Higuain   |delantero     |
  |Javier Hernandez  |delantero    |
  |Alban Meha        |centrocampista    |
  |Andrea Pirlo      |centrocampista     |
  |Christian Eriksen |centrocampista    |
  |Hakan Calhanoglu  |centrocampista      |
  |Aleksandar Kolarov|defensa  |
  |Leighton Baines   |defensa  |
  |Manuel Neuer      |arquero    |
  
  </div>

  En el grupo de jugadores escogidos hay 4 de cuyo pierna más habíl para dominar el balón, es la pierna izquierda. Por otro lado, hay presencia de 4 defensores, 4 mediocampistas, 2 delanteros, y un arquero. Los 4 defensores fueron escogidos del grupo 1 y grupo 4, que tienen características distintas.  

 

  
  
  
  
  


