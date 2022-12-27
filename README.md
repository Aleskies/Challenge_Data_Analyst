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

  La mayor cantidad de partidos que se presentan en cada una de las ligas, tiene directa relación con la cantidad de equipos participantes en la respectiva liga. En el caso de las ligas de Inglaterra, Francia y España, cada una de ellas cuenta con 20 equipos. 


## Exploración de la información de los jugadores. 

## Filtros y Selección de variables, para selección de jugadores.
  
  La base de datos Player y Player_Attributes, presenta características de jugadores de fútbol, de 11 ligas Europeas, donde se extraerá la información necesaria para conformar un equipo. 


  ### - Supuestos y seleción de la muestra.
  
  Como ya se mencionó, la base de datos contiene información de los jugadores hasta el año 2016. Con esta información en mente, se considerará que el equipo está construido para la temporada 2017 con las características y valor de indicadores estadísticos de los jugadores del año 2016.
  
  ### - Filtros
  
  Con la información de los jugadores del año 2016, se procede a identificar y tratar las observaciones duplicadas junto con aquellas que tienen alguna información perdida en alguna de sus columnas. Luego se realiza un análisis de correlación, utilizando el coeficiente de Spearman que tiene la característica de ser nás robusta a valores extremos. 
  
  En primer lugar, se excluyen aquellas variables  
  
  ## Selección del equipo ideal.
  
  El grupo de 11 jugadores corresponde a:
  
  Los primeros de ellos se esogieron en función de 
  
  
  
  

## Sugerencias y propuestas de mejora
