# speed_runs

El repositorio tiene el codigo para obtener los datos de los runs de la api de speed run. EL repositorio tiene diferentes códigos, los cuales se encargan de hacer un scrapper de la inforamación accesible de los juegos, jugadores, etc.

### games.ipynb

El archivo de games.ipynb lo que hace es obtener todos los id's de los juegos de la api, se utiliza maxSizeAPIv1=200 pues es lo máximo que puede obtener de id's por llamads.

### games_info.ipynb

El archivo de games_info.ipynb lo que hace es utilizar Beautiful Soup para poder obtener infomación de los juegos que no esta en la api. La información que se obtiene es:

* Numero de followers
* Numero de Runs
* Numero de Jugadores

### data.ipynb

El archivo de data.ipynb lo que hace es identificar que juegos son los que representan la mediana de jugadores. En este cao fueron 519 juegos. Entonces de estos 519 juegos usnado la api se obtuvieron las categories, levels y variables asociadas al juego.

Puntos a notar aquí:

* Las categorias son la forma en la que se hizo el speedrun. Ej. Si en un juego en un nivel hay 100 monedas por recolectar. Las categorias pueden ser "run consiguiendo 100 monedsas, 75 monedas, 25 monedas, 0 monedas"
* Hay 2 tipos de categorias, las que son de tipo level y las que son de tipo juego completo. Es decir, hay runs que son de pasarse todo el juego y estas categorias son de juego completo y también hay runs por level y este tiene categorias independientes.

Este código tiene todos los runs que se pueden tener por tipo de level o por run de pasarse el juego completo. Estos runs que se obtienen son los mejores runs que se han logrado obtener de cada jugador, es decir, un jugador no puede tener dos runs en un cierto nivel en cierta categoria.

### palatforms.ipynb

El archivo de platforms.ipynb tiene la forma de obtner los nombres a los id's asociados de las plataformas en la que se puede jugar

### all_players.ipynb

El archivo de all_players.ipynb obtiene la información asociada al id del jugador

### obsolate_runs_all_players.ipynb 

Como el archivo de data.ipynb solo obtiene los mejores runs de todos los jugadores quería obtener los runs que se quedaron en el olvido. Entonces el archivo de obsolate_runs_all_players.ipynb obtiene aquellos runs que alguna vez fueron subidos pero quedaron relegados por mejores tiempos del jugador

### joins.ipynb

Se hacen los respectivos joins de los csvs obtenidos para cambiar las id's por nombres reales

### forums.ipynb

El archivo de forums.ipynb lo que hace es extraer la información de los foros de discución de los juegos, esto con la finalidad de saber que tanto interactuan en un juego
