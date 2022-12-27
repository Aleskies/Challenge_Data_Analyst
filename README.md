# Challenge_Data_Analyst

El objetivo del presente proyecto es explorar patrones para armar el mejor equipo de fútbol posible. 

## Descripción de la base de datos

Se cuenta con una base de datos con más de 25.000 partidos y 10.000 jugadores de ligas Europeas, del año 2008 hasta el 2016.


<div class= text-align: "center">

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

## Supuestos

  Bajo el supuesto que se desea conformar un  

## Exploración de los datos

## Filtros y Selección de variables
  
  La base de datos que tiene las características de los jugadores está en las tablas Player y Player_Attributes. 


## Selección del equipo ideal

  ### Supuestos y seleción de la muestra
  
  Como ya se mencionó, la base de datos contiene información de los jugadores hasta el año 2016. Con esta información en mente, se considerará que el equipo está construido para la temporada 2017 con las características y valor de indicadores estadísticos de los jugadores, del año 2016.
  
  ### Filtros
  
  Con la información de los jugadores del año 2016, se procede a identificar y tratar las observaciones duplicadas junto con aquellas que tienen alguna información perdida en alguna de sus columnas. Luego se realiza un análisis de correlación, utilizando el coeficiente de Spearman que tiene la característica de ser nás robusta a valores extremos. 
  
  En primer lugar, se excluyen aquellas variables  

## Sugerencias y propuestas de mejora
