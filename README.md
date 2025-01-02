# techchallenguemeli
Este proyecto permite leer datos de la API de Mercado Libre para su posterior análisis
En el archivo challenge_getData se encuentra el código python que hace la llamada hacia la API y por cada categoría se descarga apróximadamente 1000 rows de información
teniendo en cuenta que existen 32 categorías, eso nos da un aproximado de 32000 rows para analizar. Estos rows se cargan a un dataframe y después se escribe en un csv para
analizarlo en powerBI
En el archivo challenge_eda se hizo el análisis exploratorio para entender los datos, posteriormente se hizo un sistema de score para poder evaluar que perfil tiene un determinado
seller, en este archivo se encuentra la asignación de scores de acuerdo a 5 conceptos que encontré interesantes como son
1)Cantidad de productos ofertados en la suscripción gold_pro
2)Cantidad de meses
3)Tasa de interés
4)Diversificación de sellers en distintas categorías
5)Disponibilidad de productos
Cada uno de esos conceptos determina un score entre 0 y 1, es decir, si un seller tiene muchos productos ofertados como gold_pro, tendrá una calificación de 1. Para asignar esos scores,
se hizo un cálculo sacando el máximo y mínimo de valores y con eso se hizo un cálculo.
Para la categoría de disponibilidad de productos, se hizo uso de un algoritmo de clusterización de densidad, esto porque en esa categoría se encontraron valores muy altos en algunos casos, y estos valores podrían sesgar el análisis.
Por último, se realizaron algunas gráficas sencillas en power BI para poder tener una visualización más rápida del análisis hecho.