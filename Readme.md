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
número de víctimas igual a 2.

El dataset de lesiones_hechos, tiene 23785 filas, el dataset de lesiones_victimas
tiene 27605 filas, por tanto habrá una proporcion de 20 000 puros 1 y el resto se
reparte entre 2, 3, 4, y he visto uno por ahí que es de 16.

---En general, a partir de estas proporciones, decido encaminarme a mirar estas
calles o lugares donde han ocurrido estos sinistestros viales que ha traido consigo
más de una víctima. A mirar que es lo que puede estar ocasionando estos desastres y 
a plantear soluciones particulares para estos lugares---

---Por otro lado, decido, principalmente, agrupar a la ciudad mediante comunas de
tal forma que podamos obtener patrones más visibles y de esta forma poder plantear
soluciones para cada comuna. La idea es agrupar por comunas y en base a esta 
clusterización podríamos utilizar las demás características de los datasets como
lo pueden ser la fecha (hora, dia, mes, año, ...), el vehículo de la víctima y 
del acusado, quizás la gravedad del siniestro, obviamente el número de víctimas,
por qué no el sexo de la víctima y también su edad, y por qué no el rol de la 
víctima e incluso podríamos hacer un mapa de calor para cada comuna en base al 
número de víctimas y de la distancia entre estas de tal forma que establecer 
clusters quizás utilizando algún algoritmo de agrupamiento como lo puede ser 
k-means o optics-algorithm o spectral-clustering.---

---Sin embargo, las conclusiones no parecen ser muy prometedoras, ya que, en mi 
opinión, no hay las suficientes características como para obtener conclusiones 
asertivas. Me interesaría obtener más etiquetas concerniente al tipo del siniestro
(el contexto en general, no en formato de texto plano, sino algo como un conjunto
de etiquetas que sea numeroso),además del perfil tanto de las víctimas y el perfil 
de los acusados y si fuera posible, características concernientes a la geografía 
como tal. En conjunto creo que podríamos obtener conclusiones asertivas en 
practicamente la totalidad de lo que involucra la asertividad lo que claramente 
es muy bueno.---


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

- Trabajar con zonas de mayor peligro
La idea es trabajar con las características disponibles. Entonces lo primero que 
hice fue determinar las zonas donde más siniestros y más víctimas se han dado.
Luego lo que hice fue segmentarlo por comuna ya que 