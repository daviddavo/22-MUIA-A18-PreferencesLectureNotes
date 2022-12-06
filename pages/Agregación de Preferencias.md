alias:: main
icon:: 📓

- # Día 1 {{renderer :wordcount_tlmvyif}}
	- ![Preferencias_Dia 1.pdf](../assets/Preferencias_Dia_1_1670337275609_0.pdf) #diapositivas
	- #+BEGIN_NOTE
	  **Nota**: Una buena manera de seguir los apuntes es hacer click en el .pdf para que se abran las diapositivas lado a lado, aunque no es necesario.
	  #+END_NOTE.
	- #+BEGIN_NOTE
	  **Nota**: Cuando encuentres términos entre corchetes como [[Negociación]], puedes abrirlos en la misma página web reemplazando el contenido actual haciendo `Click`, o en un *sidebar* haciendo `Shift + Click`
	  #+END_NOTE
	- ## 1. Introducción
		- La agregación de preferencias nos permite resolver dilemas colectivos que no tienen solución, teniendo en cuenta las preferencias de los individuos que deben resolver el problema
		- El principal objetivo es pasar de lo **multidimensional** (más complejo y difícil de manejar) a lo **unidimensional**, de las *opiniones individuales*, intentar obtener la opinión *global*
		  collapsed:: true
			- > ((638f5398-64df-4fa3-80c4-5ac217c4043c))
			  > En agregación de preferencias, intentamos seguir la *flecha azul*
		- Aun así, tras hacer la agregación, para conseguir mejor estabilidad sería mejor no llegar nunca a quedarse con solamente un punto, sino quedarse en un mínimo de una terna, como por ejemplo:
		  collapsed:: true
			- los tres poderes (legislativo, judicial y ejecutivo)
			- los tres presupuestos que deben conseguirse para justificar una compra en cualquier organización burocrática
			- las tres copias de cualquier parte o reclamación
		- En la agregación de preferencias podemos hacer un paralelismo con la Ciencia de Datos.
		  collapsed:: true
			- ((638f5584-66ff-4183-9f60-30dd14915e46))
			- De un conjunto de **datos** sin ordenar no podemos obtener ningún significado, pero aplicando operaciones que los *agrupen y ordenen* podemos distinguir patrones que nos dan **información**.
			- De comprender las *relaciones* en la **información** surge el **conocimiento** del que podemos tomar decisiones. Entendiendo los *principios* del conocimiento, surge la **sabiduría**.
		- > En resumen, las preferencias individuales se *agregan* para crear una preferencia de grupo $\rightarrow$ las piezas *individuales* forman el *colectivo*
		- collapsed:: true
		  #+BEGIN_WARNING
		  Pero, ¿qué tipo de [[operador de agregación]] usamos? $\rightarrow$ surgen **dilemas**
		  #+END_WARNING
			- Puede que el operador sea más próximo de la minoría que de la mayoría
			- O que no tenga en cuenta los valores sociales, dando por aceptables situaciones que no deberían serlo
			- O primando la individualidad ante la sociedad
			- ¿Qué consideramos más importante en un operador? ¿La correción política o la libertad de expresión?
	- ## 2. [[Decisión colectiva]] vs. [[Negociación]]
		- #+BEGIN_CAUTION
		  Si consideramos tan sólo la opción favorita de cada votate, nos estamos quedando con la punta del iceberg. Puede que haya algo que haga que la mayoría esté más conforme en general si tenemos en cuenta las decisiones en un poco más de profundidad.  
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
		- #+BEGIN_NOTE
		  En mi opinión, por estas razones es tan espinoso en la democracia el implementar sistemas de votación "más avanzados". Si son electrónicos se convierten en *cajas negras*, y si son más complejos es más difícil de entender y relatar los resultados
		  #+END_NOTE
	- ## 3. [[Votación]] vs [[Elección social]]