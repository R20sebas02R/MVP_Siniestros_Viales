Planteamiento del problema
-------------------------------------------------------------------------------------

Primeros pasos:
	- Los siniestros viales son eventos que involucran vehículos en las vías 
	públicas.
	- Las tasas de mortalidad de siniestros viales se calcula como la cantidad 
	de muertes en un siniestro vial, entre la cantidad total de muertes.

Contexto:
	- Los datos corresponden a la Ciudad de Buenos Aires.
	- En todo Argentina, en cada año, mueren alrededor de 4000 personas en
	siniestros viales (11 personas/día).
	- El periodo de tiempo es desde 2016-2021.
	- Un dataset: Homicidios, Otro dataset: Víctimas. Cada uno tiene dos hojas
	o dos tablas: Hechos y Víctimas.

Lo que se espera:
	- Conclusiones y Estrategias para disminuir la cantidad de víctimas fatales
	o muertes (directamente) de los siniestros viales.


--------------------------------------------------------------------------------------
Primeras impresiones y planteamiento de hipótesis iniciales
--------------------------------------------------------------------------------------

El dataset de homicidios está bien balanceado respecto a la cantidad de víctimas 
y la cantidad de siniestros viales. Lo digo porque la tabla de homicidios_hechos
tiene 696 filas y la tabla homicidios_victimas tiene 717 filas, y además en la 
columna de 'N_victimas' hay puros 1 y unos cuantos 2, habrá 21 registros con 
número de víctimas igual a 2. Esto significa que en cada siniestro lo más probable
es que, si hay muertes, es que el número sea igual a 1.

El dataset de lesiones_hechos, tiene 23785 filas, el dataset de lesiones_victimas
tiene 27605 filas, por tanto habrá una proporcion de 20 000 puros 1 y el resto se
reparte entre 2, 3, 4, y he visto uno por ahí que es de 16.

---En general, a partir de estas proporciones, decido encaminarme a mirar estas
calles o lugares donde han ocurrido estos sinistestros viales que ha traido consigo
más de una víctima. A mirar que es lo que puede estar ocasionando estos desastres y 
a plantear soluciones particulares para estos lugares.
Lo otro que decido plantear es la posibilidad de segmentar áreas geográficas de mayor
tamaño, sin perder la coherencia y consistencia.---



--------------------------------------------------------------------------------------
Camino coherente a seguir para este tipo de caso (Siniestros Viales)
--------------------------------------------------------------------------------------

ChatGPT:

El análisis de un dataset de siniestros viales puede proporcionar una variedad de 
conclusiones y conocimientos útiles para mejorar la seguridad vial y la toma de 
decisiones. Aquí hay algunas conclusiones generales que suelen extraerse de este 
tipo de datasets:

		/Identificación de patrones de siniestros/

Localización: ¿Dónde ocurren con mayor frecuencia los siniestros viales?
Día y hora: ¿Hay momentos específicos del día o de la semana en los que son más 
comunes los accidentes?

Condiciones meteorológicas: ¿Cómo afecta el clima a la ocurrencia de siniestros?
Tipo de carretera: ¿Los accidentes son más frecuentes en carreteras urbanas, 
rurales o autopistas?


		/Factores contribuyentes/

Causas principales: ¿Cuáles son las causas más comunes de los siniestros, como el 
exceso de velocidad, distracciones, consumo de alcohol, etc.?

Conductores involucrados: ¿Qué grupos de edad, género o tipos de licencia están más 
implicados en los accidentes?

Vehículos: ¿Hay modelos o tipos de vehículos que están relacionados con más 
siniestros?

Condiciones de la carretera: ¿La infraestructura vial tiene un impacto en la 
seguridad, como la falta de señalización, mal estado de la carretera, etc.?


		/Lesiones y víctimas/

Gravedad de las lesiones: ¿Qué tipos de lesiones son más comunes en los siniestros 
viales?

Número de víctimas: ¿Cuántas personas resultan heridas o fallecen en promedio en un 
siniestro?

Perfil de las víctimas: ¿Qué características tienen las personas más afectadas, 
como edad, género, etc.?


		/Efectividad de las medidas de seguridad/

Uso de cinturones de seguridad y cascos: ¿Cuántos siniestros ocurren con personas 
que no usan medidas de seguridad?

Cumplimiento de normativas: ¿Se respetan las leyes de tráfico, como los límites de 
velocidad y la prohibición de conducir bajo la influencia del alcohol o las drogas?

Evaluación de sistemas de seguridad vial: ¿Qué impacto tienen las infraestructuras 
de seguridad vial, como rotondas, pasos de peatones y señalización?
Tendencias a lo largo del tiempo:

Evolución de los siniestros: ¿Hay una tendencia al alza o a la baja en la cantidad 
de siniestros a lo largo de los años?

Cambios estacionales: ¿Existen patrones estacionales en la ocurrencia de siniestros?
Análisis geoespacial:

Mapeo de siniestros: Creación de mapas de calor para identificar áreas de alto riesgo.

Zonas problemáticas: Identificación de intersecciones o segmentos de carreteras 
particularmente peligrosos.


		/Estrategias de prevención/

Desarrollo de políticas: Información para la creación o mejora de políticas 
públicas relacionadas con la seguridad vial.

Educación y concientización: Identificación de áreas donde se requiere una mayor 
educación pública sobre seguridad vial.





En resumen, el análisis de un dataset de siniestros viales puede ayudar a 
comprender mejor las causas y las circunstancias que rodean los accidentes de 
tráfico, lo que a su vez puede contribuir a la adopción de medidas más efectivas 
para prevenirlos y mejorar la seguridad en las carreteras.


--------------------------------------------------------------------------------------
Camino que he decidido transitar
--------------------------------------------------------------------------------------

- Lo primero que pensé es en mirar o buscar patrones en el mapa. Para ello segmenté el
dataset mediante comunas de tal forma que pueda obtener conclusiones sobre que zonas 
son las más 'peligrosas'.

- Efectivamente logré encontrar comunas que sobresalían en el número de víctimas y 
siniestros, entonces la siguiente pregunta que surgió fue sobre el tipo de calle dónde
mayor cantidad de siniestros han ocurrido. En este sentido encontré que las Avenidas son
el tipo de calle con mayor número de siniestros y de víctimas.

- Lo siguiente que quise saber es sobre el perfil de la víctima y del acusado. Pude
encontrar perfiles de víctimas de mayor frecuencia así como el perfil del
acusado, y a esto se le suma la combinación de víctima-acusado de mayor frecuencia.

- Lo siguiente que me intrigó fue sobre las proporciones en cuánto al sexo de las 
víctimas, si existía alguna relación razonable entre el número de víctimas y el sexo.
Se me ocurrió también realizar pruebas de hipótesis respecto a la correlación entre el
sexo y el tipo de víctima o el rol que esta cumplía, sin embargo, no pude obtener 
conclusiones ya que sería incorrecta debido al no balanceo del dataset (hay más hombres
que mujeres).

- La otra característica que quise saber es sobre el número de días que pasaron antes 
del fallecimiento de la víctima y después del siniestro vial. En este caso logré 
encontrar de que prácticamente es muy probable de que la persona muera el mismo día 
del siniestro.

- Luego me causó curiosidad respecto al rango de edades de mayor número de víctimas, 
y como era de esperar, el rango oscilaba entre los 20 y 40 años.

- FINALMENTE, es también importante buscar algún patrón estacionario en las series de
tiempo a partir de la fecha del siniestro. Este análisis lo quise hacer en el dashboard
en Tableau, ya que, es más práctico.

Entonces, estos son algunas de las conclusiones:

**¿En qué rango de edad se encuentran el número mayor de víctimas?**
- Entre 20-40 años, es el rango que más víctimas tiene. Se trata de una distribución 
ligeramente sesgada hacia las edades menores.
- Entre 0-10 y 85-100 es poco probable que exista una víctima entre estos rangos.

**¿Y qué pasa con la cantidad de días hasta la muerte de la víctima?**
- Con diferencia, las personas mueren el mismo día en el que ha ocurrido el siniestro.
- Con más presición, diría que a partir de la semana del siniestro, es poco probable que 
la persona sigue viva.

**¿Qué tipo de víctima es la más afectada?**
- Con diferencia, las víctimas que más sufren son las que se transportan en motos y los 
peatones.
- Luego, los que se transportan en vehículos públicos (PASAJEROS), o los que se trasportan 
en ambulancias, autos policiales.... (MOVIL), además de los que se trasportan en vehículos 
de cargas (CARGAS) son los menos afectados.

**¿De este tipo de víctimas, que función cumplían los más afectados?**
- Los conductores y los peatones son los que mayor daño han recibido.

**¿Hombres o Mujeres, cuál de ellos está siendo más afectado?**
- 3/4 partes del total de las víctimas corresponden a que son hombres.

**Sobre el perfil de las víctimas**
- Las motos, los peatones y por ahí los autos, son los que en la mayoría de siniestros son 
las víctimas.
- Coincide también según el número de víctimas.  

**Sobre el perfil de los acusados**
- Los acusados que en mayores siniestros están envueltos son los conductores de autos, de 
vehículo de transporte público y los de vehículos de cargas.
- Coincide lo mismo con el número de víctimas asociadas.

**Sobre las combinaciones que más coinciden**
- Aquí vemos como los peatones coinciden más con los vehículos de transporte público.
- Luego los que manejan moto coinciden más con los autos. 
- Finalmente también hay coincidencias entre peatones y autos. 
Menciono estos ya que presentan mayores diferencias respecto al resto de combinaciones.
Peatones, Autos y Transporte público son los actores que están envueltos en la mayoría de los siniestros.
- Coincide con el número de víctimas.

**¿Qué tipo de calle es la que más siniestros tiene y la que tiene el mayor número de víctimas?**
- Las avenidas son las que más siniestros tienen.
- Coincide según el número de víctimas.

**¿Y qué pasa por comuna?**
- Bueno, ya podemos ver que ciertas comunas son las más afectadas, diría que habría que prestar principal atención a la comuna 1, en los barrios de Retiro, San Nicolás, Puerto Madero, San Telmo, Montserrat y Constitución. El resto de comunas si hay casos de alta urgencia, sin embargo, esta comuna lidera con cierta diferencia.
- Coincide según el número de víctimas.

