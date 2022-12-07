alias:: main, página principal
icon:: 📓

- # Día 1 {{renderer :wordcount_tlmvyif}}
  id:: 638f52a9-5666-4bf2-a3ff-a95fbea033dc
	-
	- ![Preferencias_Dia 1.pdf](../assets/Preferencias_Dia_1_1670337275609_0.pdf) #diapositivas
	- #+BEGIN_NOTE
	  **Nota**: Una buena manera de seguir los apuntes es hacer click en el .pdf para que se abran las diapositivas lado a lado, aunque no es necesario.
	  #+END_NOTE.
	- #+BEGIN_NOTE
	  **Nota**: Cuando encuentres términos entre corchetes como [[Negociación]], puedes abrirlos en la misma página web reemplazando el contenido actual haciendo `Click`, o en un *sidebar* haciendo `Shift + Click`. Si mantienes el ratón encima se muestra una previsualización del contenido.
	  #+END_NOTE
	- ## 1. Introducción
		- La agregación de preferencias nos permite resolver dilemas colectivos que no tienen solución, teniendo en cuenta las preferencias de los individuos que deben resolver el problema
		- El principal objetivo es pasar de lo **multidimensional** (más complejo y difícil de manejar) a lo **unidimensional**, de las *opiniones individuales*, intentar obtener la opinión *global*
		  collapsed:: true
			- > ((638f5398-64df-4fa3-80c4-5ac217c4043c))
			  > En agregación de preferencias, intentamos seguir la *flecha azul*
		- Aun así, tras hacer la agregación, para conseguir mejor estabilidad sería mejor no llegar nunca a quedarse con solamente un punto, sino quedarse en un mínimo de una terna, como por ejemplo:
			- los tres poderes (legislativo, judicial y ejecutivo)
			- los tres presupuestos que deben conseguirse para justificar una compra en cualquier organización burocrática
			- las tres copias de cualquier parte o reclamación
		- En la agregación de preferencias podemos hacer un paralelismo con la Ciencia de Datos.
			- ((638f5584-66ff-4183-9f60-30dd14915e46))
			- De un conjunto de **datos** sin ordenar no podemos obtener ningún significado, pero aplicando operaciones que los *agrupen y ordenen* podemos distinguir patrones que nos dan **información**.
			- De comprender las *relaciones* en la **información** surge el **conocimiento** del que podemos tomar decisiones. Entendiendo los *principios* del conocimiento, surge la **sabiduría**.
		- > En resumen, las preferencias individuales se *agregan* para crear una preferencia de grupo $\rightarrow$ las piezas *individuales* forman el *colectivo*
		- #+BEGIN_WARNING
		  Pero, ¿qué tipo de [[operador de agregación]] usamos? $\rightarrow$ surgen **dilemas**
		  #+END_WARNING
			- Puede que el operador sea más próximo de la minoría que de la mayoría
			- O que no tenga en cuenta los valores sociales, dando por aceptables situaciones que no deberían serlo
			- O primando la individualidad ante la sociedad
			- ¿Qué consideramos más importante en un operador? ¿La correción política o la libertad de expresión?
	- ## 2. [[Decisión colectiva]] vs. [[Negociación]]
		- #+BEGIN_CAUTION
		  Si consideramos tan sólo la opción favorita de cada votante, nos estamos quedando con la punta del iceberg. Puede que haya algo que haga que la mayoría esté más conforme en general si tenemos en cuenta las decisiones en un poco más de profundidad.  
		  #+END_CAUTION
		- Del fragmento de la película *12 hombres sin piedad* saco la conclusión de que los operadores de agregación no lo son todo, y debería primar el diálogo dentro de lo posible. (cuando el número de agentes es reducido).
		- En la agregación de preferencias hay que tener en cuenta: #.ol
			- La estructura del problema
				- No puedes modelar lo que no conoces
			- Definición de las unidades
				- No sumar cosas que no tienen nada que ver
			- Naturaleza de la información cuantitativa
				- ¿Escala nominal? ¿ordinal? ¿intervalos? ¿racional?
			- Modelos paramétricos en lugar de "cajas negras" (interpretable)
			- Que sea posible hacer un relato
		- #+BEGIN_WARNING
		  Surgen problemas cuando usamos funciones de agregación sin tener en cuenta la naturaleza de la información o las unidades, sumando cosas que no tienen que ver, o haciendo restas y divisiones con escalas nominales y ordinales.
		  #+END_WARNING
		- #+BEGIN_NOTE
		  En mi opinión, por estas razones es tan espinoso en la democracia el implementar sistemas de votación "más avanzados". Si son electrónicos se convierten en *cajas negras*, y si son más complejos es más difícil de entender y relatar los resultados
		  #+END_NOTE
			- Y ya ni hablemos de usar algun modelo basado en *redes neuronales* o *bayesianas*, pues **perderíamos la narrativa** y sería imposible averiguar por qué ha salido elegida esa decisión global.
	- ## 3. [[Votación]] vs [[Elección social]]
		- En ambas cada agente $i$ tiene preferencias $\succeq_i$ (escala ordinal) sobre el conjunto de alternativas $X$
			- Véase [[Marco formal de la negociación]]
		- En la [[Votación]] solo se tiene en cuenta la *mejor alternativa* de cada decisor, mientras que en la [[Elección social]] cada decisor hace un *ranking* de las alternativas.
		- #+BEGIN_NOTE
		  La [[votación]] es la punta del iceberg de la [[elección social]]
		  #+END_NOTE
		- Las principales diferencias son que la [[elección social]] es normativa e ideal, mientras que la [[Votación]] es más realista (sencilla de implementar en la realidad)
	- ## 3. [[Sistemas de votación]]
		- De los distintos sistemas podemos observar que cada uno tiene sus problemas, y que surgen al tener más de dos elecciones posibles.
		- En la [segunda vuelta](((638f8ced-5510-422e-8aee-68b566923a51))) se intenta paliar este problema en una segunda vuelta, pero en la primera el problema sigue ahí
		- En [First-Past-The-Post](((638f8b49-ea3a-4435-8002-b9ac63f85fd2))) no se tienen en cuenta el resto de candidatos o sus afiliaciones (pues no es [[elección social]]), lo que puede llevar a elegir al odiado por la mayoría.
		- En cada uno de los [sistemas de listas](((638f8b8d-a89f-41e3-ac90-305cf74c495b))) se puede encontrar una lista desfavorecida, siempre habrá acusaciones de *injusticia*
		- En [approval voting](((638f8b91-fa79-428e-b711-0eec174652f7))) sí que se pueden mostrar varias preferencias, pero estas *no están ordenadas*.
	- ## 3. Sistemas de [[Elección social]]
		- Con las mismas puntuaciones asignadas, aplicando distintas reglas de elección social obtenemos distintos *ránkings*, distintas *opiniones globales*
		- #+BEGIN_WARNING
		  **Cuidado**: Las puntuaciones son un *ránking*, simplemente *ordinales*, no deberíamos hacer operaciones aritméticas con ellas (como elegir al que mejor *media* tenga)
		  #+END_WARNING
		- A pesar de ello, el métodos de *Cook & Seiford* efectúa restas
			- > En mi opinión, esto no es un problema tan grave si explicamos a los decisores cómo funciona el sitema, y que 4 es **el doble** que 2.
		- El método de *Copelan* tiene en cuenta la propiedad *transitiva* de las preferencias de los agentes para hacer comparación por pares (perspectiva **local**), y contar cuantas veces es preferida cada alternativa para hacer un *ranking* (agregación a **global**).
		- A pesar de ello, al pasar de lo *local* a lo *colectivo* surgen problemas pues no todo el mundo está *en la misma escala*. Estamos, básicamente, **aplicando cálculo a las humanideades**
		- #+BEGIN_PINNED
		  Parece ser que no hay un método de agregación perfecto
		  #+END_PINNED
- # Día 2 {{renderer :wordcount_kccwhkctk}}
	- ![Preferencias_Dia 2.pdf](../assets/Preferencias_Dia_2_1670353486220_0.pdf) #diapositivas
	- ## 3. [[Elección social]] (cont.)
		- > El [día anterior](((638f52a9-5666-4bf2-a3ff-a95fbea033dc))) se hizo una presentación y vimos intuitivamente los problemas de los distintos [[Sistemas de votación]] y de [[Elección social]]. Hoy se explicará *por qué* surgen dichos problemas.
		- Dados los 6 axiomas del [[Teorema de Arrow]], el teorema concluye que:
			- ((638f96c4-ad51-43dd-914b-1c964b8538a2))
		- Es decir, siempre va a haber un caso en el que el método es *injusto* porque no se verifica algún axioma
		- id:: 638f9829-3613-45dd-90d8-286ae304fd2b
		  > De aquí saco la conclusión de que, aplicando el [[Teorema de Arrow]], no existe ni existirá nunca una app que pueda decidir las cosas por nosotros. Siempre va a ser necesario el diálogo para las cosas importantes.
			- #+BEGIN_TIP
			  El [[Teorema de Arrow]] es a la política lo que el *Problema de la Parada* a la programación
			  #+END_TIP
	- ## 4. [[Bienestar social]]
		- Aunque tengamos una regla de [[Elección social]] que siga casi todos los axiomas del [[Teorema de Arrow]], podemos encontrarnos con dilemas para los que la elección social no es suficiente.
		- En el caso de los Ying y los Yang, la preferencia de los Yang a no sufrir debería tener **mucho más peso** que la satisfación de los Ying.
			- Por mucho que cumplan los axiomas, seguiría **no siendo justo**
		- Para comparar esos pesos se usa la [[Comparación Interpersonal de Utilidades]]
			- Es muy difícil obtener esta información, por lo que no se ha usado mucho entre los economistas
		- > Además, esta información será una función $U_{i}$ dependiente de muchas variables, una de ellas la altamente variable experiencia del decisor hasta el momento
		- ### [[Bienestar social]] vs. [[Elección social]]
			- El objetivo es el mismo, pero en el [[Bienestar social]] la naturaleza de la información es *cardinal*, mientras que en la [[Elección social]] es *ordinal*
		- Tenemos una [[Función de Bienestar Social]] $W$ que recibe los valores de las funciones $U_i$ de cada agente y proporciona un orden racional de alternativas.
			- Además, si *maximizamos* esta función podemos obtener un **óptimo social**
		- > Esta función $W$ es un *dictador benevolente* que tiene en cuenta las opiniones de todos para llegar a un óptimo
		- La más utilizada suele ser *la suma de todos*, en la que la sociedad se queda indiferente, siguiendo principios individualistas.
			- > Si una persona gana 10.000€ y otra persona pierde 10.000€ no importa, aunque muchos coincidiremos en realidad no es lo mismo perderlo todo o perder un poco. El **óptimo social** es independiente de las condiciones individuales.
				- Sin embargo, sí que podríamos debatir sobre dónde poner ese límite. ¿Cuanto es mucho? ¿Cuanto es poco? ¿Que alguien lo pierda todo para que algunos ganen lo suficiente es aceptable?
		- Con *el producto* se genera una función convexa en la que se promociona la solidaridad. Si el otro tiene muy poco, al multiplicarse con lo tuyo, saldrá un valor bajo, y viceversa.
			- Para llegar al **óptimo social** es más sencillo hacer que al que peor le va le vaya mejor, que mejorar al que mejor le va.
		- Sin embargo, la máxima solidaridad se da con la función *min*. Solo irá bien si todos y cada uno de los $u_i$ salgan bien.
			- El **óptimo social** se alcanza cuando se maximizan dichos mínimos.
	- ## Dilema de la mayoría-minoría
		- Si usamos como función de agregación la *mediana* o la *moda*, se tachan los valores atípicos y prima el principio de la mayoría. Mientras que si se usa la *media* se sensibiliza el valor atípico acercándose a la minoría.
		- Una función interesante no muy conocida es el *punto medio del rango*.
			- Al considerarse el máximo, se fomenta la *especialización*
			- Pero como también se considera el mínimo, no puede descuidarse el resto de aspectos.
- # Caso curioso: DAOs
	- ## Sobre mí
		- Trabajo de Personal de Apoyo a la Investigación en el Grupo de investigación en Aplicaciones Sociales e Interdisciplinares basadas en Agentes ([GRASIA](https://grasia.fdi.ucm.es/)) del Dpto de Software e Inteligencia Artificial (DISIA) de la Universidad Complutense de Madrid (UCM)
		- En mi trabajo investigo sobre Algocracia, en concreto sobre 
		  [[Organizaciones Autónomas Descentralizadas]] (DAOs)
			- ((6390526a-2e5f-4bba-b408-c54f13fdcf23))
		- Y, más en concreto, en el mecanismo de [Consenso Holográfico](https://p2pmodels.eu/holographic-consensus-a-scalable-voting-system/) de DAOstack (plataforma que facilita el despliegue de DAOs)
	- En las [[DAOs]] cualquiera puede realizar una propuesta, pero sólo puede votar aquel que posea *Reputación* (un *token* personal e intransferible).
	- Aunque las propuestas pueden tener varias alternativas, la mayoría tienen sólo dos: aprobar y rechazar, y son en las que nos centraremos.
	- El resultado de la votación es mediante *la suma de todos*, pero ponderada por *reputación*.
		- La reputación la concede la [[DAO]], por lo que dependiendo de su propósito habrá distintas maneras de conseguirla
		- Por ejemplo, en una [[DAO]] sobre proyectos de programación, puede que tenga más reputación el que haya completado más proyectos
		- O, en una implementación de una empresa cooperativa, la reputación puede ser simplemente proporcional al capital social aportado
	- Se trata, por lo tanto, de un enfoque puramente liberal e individualista
	- Además, en la mayoría de [[DAOs]] desplegadas se pueden observar distribuciones muy desiguales en la reputación.
	- En varios casos menos de un 10% de los usuarios controla más del 50% de los votos, por lo que pueden llegar a la mayoría absoluta sin tener en cuenta al otro 90% de participantes.
	  id:: 63905472-8d9d-430b-b22d-e7db96eec93a
	- En las [[DAOs]] también surgen varios problemas relativos a la abstención, pues aunque sean usuarios inactivos, siguen poseyendo reputación y *contando* para el total.
	- Para solucionarlo, el consenso holográfico implementa un complejo mercado de predicción en el que se puede *apostar* por el resultado de una propuesta (y si acaba saliendo, recibes una recompensa)
	- Cuando se apuesta *a favor* por encima de un umbral, en lugar de ser necesario llegar a la mayoría absoluta, la propuesta *puede* ser aprobada por **mayoría relativa**
	- > La *idea* es crear un filtro humano que incentive las *propuestas interesantes*
	- Aunque estas predicciones tienen alta precisión en DAOs grandes, tienen muy poco recall.
	- Además, esa alta precisión también puede deberse a que al ser necesaria la mayoría absoluta si nadie apuesta por esa propuesta, sumado a la gran abstención, es muy difícil que se llegue al quórum. Es decir, si no se usa el mercado de predicción, es imposible que una propuesta sea aprobada. (Esta es mi hipótesis)
	- Además, antes si quiera de hacer la propuesta suele haber una extensa discusión *off-chain* (en otros medios como Foros, Discord, grupos de Telegram...), y las pocas personas que tienen reputación hacen de *dictadores benevolentes* agregando las opiniones recabadas de esas discusiones
	- > Por lo tanto, en las DAOs no se cumplen algunos axiomas del [[Teorema de Arrow]]
		- No se cumple la [no trivialidad](((638f970c-f525-4b09-bed4-153b4d99b635))), pues tan sólo hay 3 alternativas, y en muchas ocasiones el voto de 2 personas ya forma el 50%
		- Tampoco se cumple el principio de [no dictadura](((638f97cb-b912-4ea4-abb4-08dbb0759f27)))
			- ((63905472-8d9d-430b-b22d-e7db96eec93a))
	- Pero esto ya lo sabíamos, pues...
		- ((638f9829-3613-45dd-90d8-286ae304fd2b))
	- Más info: https://github.com/Grasia/dao-analyzer#publications