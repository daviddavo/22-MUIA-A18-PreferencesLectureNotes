alias:: Marco formal de la negociación
page-type:: [[Término]]

- ## Elementos
	- #+BEGIN_NOTE
	  Entre paréntesis se pone el nombre del término según el Análisis de Decisiones
	  #+END_NOTE
	- Un conjunto $N$ de **negociadores** (*decisores*)
		- $$ N = \{  N_1, N_2, ..., N_m \}$$
	- Un conjunto $X$ de **ofertas factibles** (*alternativas*) que tienen **aspectos a negociar** (*atributos*)
		- $X \subset R^{p}$ (conjunto convexo)
	- **Objetivos** que pueden ser distintos para cada negociador
		- $f_i: X\mapsto Y_i \subset R^{mi}$ (conjunto cóncavo)
		- Es un [[operación de agregación]]
		- Dos paradigmas: **optimización** y **satisfacción**
	- Una **función de utilidad** para cada negociador
		- $u_i: Y_i\mapsto U_i\subset R$
		- También es un [[operador de agregación]]
	- Una **función de utilidad colectiva** para el grupo
		- $u: U\equiv (U_1, ... U_m) \mapsto R$