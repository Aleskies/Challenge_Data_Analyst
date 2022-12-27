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

  La mayor cantidad de partidos jugados en cada una de las ligas, tiene directa relación con la cantidad de equipos participantes en cada uno de los torneos. Las ligas de Inglaterra, Francia y España, son las que presentan mayor cantidad de partidos, y cuentan con 20 equipos, por cada temporada. 


## Exploración de la información de los jugadores. 

### Filtros y Selección de variables, para selección de jugadores.
  
  La base de datos Player y Player_Attributes, presenta características de jugadores de fútbol, de 11 ligas Europeas, donde se extraerá la información necesaria para conformar un equipo. 


  #### - Supuestos y seleción de la muestra.
  
  Como ya se mencionó, la base de datos contiene información de los jugadores hasta el año 2016. Con esta información en mente, se considerará que el equipo que se presenta en este trabajo, está formado para la temporada 2017 con las características y valor de indicadores estadísticos de los jugadores del año 2016.
  
  #### - Filtros
  
  Con la información de los jugadores del año 2016, se procede a identificar y excluir las observaciones duplicadas, junto con aquellas que tienen alguna información perdida en alguna de sus columnas. Luego se realiza un análisis de correlación, utilizando el coeficiente de Spearman que tiene la característica de ser nás robusta a valores extremos. 
  
  Una vez obtenido los valores de las correlaciones, se excluyen aquellas variables que tienen una correlación mayor o igual a 0.70. A continuación, con las variables numéricas que quedaron del paso anterior, se realiza un cluster con 5 agrupaciones, que tiene como finalidad poder escoger un cantidad de jugadores de cada uno de los grupos, de modo que el conjunto obtenido sea un poco más heterogéneo, y puedan complementar sus habilidades.
  
  Un pequeño resumen de las caracteristicas de cada uno de los 5 grupos se presenta a continuación

  ![Cluster](https://github.com/Aleskies/Challenge_Data_Analyst/blob/main/imagenes/resumen_5_cluster.png)


  Obtenido los 5 grupos de jugadores, se realiza la siguiente clasificación en cada uno de ellos.

  Grupo 0. De este grupo no se recluta ningun jugador
  
  En el grupo se observan jugadores de estatura media 189.11 cm, y con valores medios más bajos, ne la mayoria de las características de los jugadores, en comparación a los integrenates de los cuatro grupos restantes. Por ejemplo, los valores de los indicadores free_kick_accuracy y finishing, son 14.313580 y 13.466667, que son los más bajos de los cinco grupos, y que tienen relación con características de definición frente al arco rival. Esto nos suguiere que quizá sus habilidades no estan relacionadas con hacer goles, quizá poseen caracteristicas más defensivas, pero en el caso de los indicadores de marking o standing_tackle, también presentan los valores más bajo de los grupos.

  Grupo 1. Se escogen 2 jugadores

  La media de estatura de este grupo de jugadores es 185.70 cm, y se organizan las siguiente variables en busca de 2 jugadores, con características más defensivas. Se consideran las mayores puntuaciones de las características de 'strength', 'jumping',  'stamina','aggression','sprint_speed' y 'long_passing', la selección corresponden a:


  <div align="center">
  


  
</div>
  
  
  ## Selección del equipo ideal.
  
  El grupo de 11 jugadores corresponde a:
  
  Los primeros de ellos se esogieron en función de 
  
  
  
  


