*Ecuación Lineal:*   $a_{1}x_{1}+a_{2}x_{2}+\dots+a_{n}x_{n}=b$

*Sistema de m Ecuaciones con n Incógnitas:*   $\begin{cases}a_{11}x_{1}+a_{12}x_{2}+\dots+a_{1n}x_{n}=b_{1}\\a_{12}x_{1}+a_{22}x_{2}+\dots+a_{2n}x_{n}=b_{2}\\a_{m1}x_{1}+a_{m2}x_{2}+\dots+a_{mn}x_{n}=b_{m}\end{cases}$

*Sistema de Ecuaciones Homogéneos:*   $\begin{cases}a_{11}x_{1}+a_{12}x_{2}+\dots+a_{1n}x_{n}=0\\a_{12}x_{1}+a_{22}x_{2}+\dots+a_{2n}x_{n}=0\\a_{m1}x_{1}+a_{m2}x_{2}+\dots+a_{mn}x_{n}=0\end{cases}$

*Matriz de Coeficientes:*   $A=\begin{pmatrix}a_{11}&a_{12}&a_{1n}\\a_{21}&a_{22}&a_{2n}\\a_{m1}&a_{m2}&a_{mn}\end{pmatrix}$

*Matriz Aumentada:*   $A=\begin{pmatrix}a_{11}&a_{12}&a_{1n}&b_{1}\\a_{21}&a_{22}&a_{2n}&b_{2}\\a_{m1}&a_{m2}&a_{mn}&b_{m}\end{pmatrix}$
<br>
## Tipos de Sistemas de Ecuaciones

*Incompatible:*  No tiene solución.

*Compatible Determinado:*  Tiene una única solución.

*Compatible Indeterminado:*  Tiene infinitas soluciones.
<br>
## Solución de un Sistema Lineal

1. Transformar la matriz aumentada a la forma escalonada (Si el sistema es homogéneo, entonces usar la matriz de coeficientes).
2. Hallar el Rango de la matriz aumentada y de coeficientes obtenida de la forma escalonada.
3. Si los Rangos son iguales, entonces el sistema es compatible, de lo contrario, es indeterminado sin solución.
4. Siendo el sistema compatible, si el Rango es igual al numero de variables, entonces es compatible determinado, y se aplica sustitución regresiva.
5. Si el Rango es menor al numero de variables, entonces el sistema es compatible indeterminado, y se debe parametrizar las variables que no tengan columna pivote, y aplicar sustitución regresiva pero con las ecuaciones parametrizadas.

##### Tags

#clase #class