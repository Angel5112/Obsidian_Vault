*Matriz:*   $A=\begin{pmatrix}a_{11}&a_{12}&\dots&a_{1n}\\a_{21}&a_{22}&\dots&a_{2n}\\\dots&\dots&\dots&\dots\\a_{m1}&a_{m2}&\dots&a_{mn}\end{pmatrix}=A_{m\cdot n}$

*Orden de una Matriz:* $m\cdot n$

*Matriz Cuadrada:*   $m=n$
<br>
## Características de Matrices Cuadradas:

*Diagonal Principal:*   $D(A)=a_{11}, a_{22}, \dots,a_{nn}$

*Matriz Diagonal:*   $A_{3\cdot 3}\begin{pmatrix}a_{11}&0&0\\0&a_{22}&0\\0&0&a_{mn}\end{pmatrix}$

*Matriz Identidad:*   $I_{3}=\begin{pmatrix}1&0&0\\0&1&0\\0&0&1\end{pmatrix}$

*Matriz Triangular Superior:*   $A_{3\cdot3}=\begin{pmatrix}a_{11}&a_{12}&a_{13}\\0&a_{22}&a_{23}\\0&0&a_{33}\end{pmatrix}$

*Matriz Triangular Inferior:*   $A_{3\cdot 3}=\begin{pmatrix}a_{11}&0&0\\a_{21}&a_{22}&0\\a_{31}&a_{32}&a_{33}\end{pmatrix}$

*Matriz Triangular:*   $A_{3\cdot 3}=\begin{pmatrix}a_{11}&0&0\\0&a_{22}&0\\0&0&a_{33}\end{pmatrix}$
<br>
## Algebra de Matrices

*Suma de Matrices:* $A+B=\begin{pmatrix}a_{11}+b_{11}&a_{12}+b_{12}&a_{13}+b_{13}\\a_{21}+b_{21}&a_{22}+b_{22}&a_{23}+b_{23}\\a_{31}+b_{31}&a_{32}+b_{32}&a_{33}+b_{33}\end{pmatrix}$

*Opuesto de una Matriz:*   $-A=\begin{pmatrix}-a_{11}&-a_{12}&-a_{13}\\-a_{21}&-a_{22}&-a_{23}\\-a_{31}&-a_{32}&-a_{33}\end{pmatrix}$

*Resta de Matrices:*   $A-B=\begin{pmatrix}a_{11}-b_{11}&a_{12}-b_{12}&a_{13}-b_{13}\\a_{21}-b_{21}&a_{22}-b_{22}&a_{23}-b_{23}\\a_{31}-b_{31}&a_{32}-b_{32}&a_{33}-b_{33}\end{pmatrix}$

*Producto de Matrices:*   Filas por columnas, solo posible si $n_{A}=m_{B}$, resultando en $C_{m_{A}\cdot n_{B}}$

*Producto por Escalar:*   $\alpha \cdot A_{3\cdot3}=\begin{pmatrix}\alpha \cdot a_{11}&\alpha \cdot a_{12}&\alpha \cdot a_{13}\\\alpha \cdot a_{21}&\alpha \cdot a_{22}&\alpha \cdot a_{23}\\\alpha\cdot a_{31}&\alpha \cdot a_{32}&\alpha \cdot a_{33}\end{pmatrix}$

*Matriz Transpuesta:*   $A^T=\begin{pmatrix}a_{11}&a_{21}&a_{31}\\a_{12}&a_{22}&a_{32}\\a_{13}&a_{23}&a_{33}\end{pmatrix}$
<br>
## Matrices Equivalentes

Dos matrices serán equivalentes entre si una vez realizada algunas de las siguientes operaciones

*Intercambio de Filas:*   $f_{1}\leftrightarrow f_{2}$

*Multiplicación por Escalar:*   $f_{1}\to \alpha \cdot f_{1}$

*Suma o Resta de Filas:*   $f_{1}\to f_{1}\pm f_{2}$
<br>
## Matrices Escalonadas, Reducidas y Escalonadas Reducidas

*Matriz Escalonada:*

1. Filas nulas (si es que existen) deben estar debajo de todas las filas no nulas.
2. Cada entrada principal de una fila esta una columna a la derecha de la entrada principal de la fila anterior.

*Matriz Reducida:*

1. La entrada principal de cada fila diferente de cero (0) es uno (1).
2. Todos los elementos por encima de la entrada principal son ceros (0).

*Matriz Escalonada Reducida:* Toda matriz que cumpla con las 4 reglas a la vez sera escalonada reducida.
<br>
## Determinante de Matrices

*Determinante:*  Numero asociado a cada matriz cuadrada.

*Determinante de Matriz 1x1:*   $A=\begin{pmatrix}a_{11}\end{pmatrix}\to \det(A)=a_{11}$

*Determinante de Matriz 2x2:*   $\det(A)=a_{11}\cdot a_{22}-a_{12}\cdot a_{21}$

*Determinante de Matriz 3x3:*   $A_{3\cdot 3}=\begin{pmatrix}a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33}\end{pmatrix}\to \det(A)=\begin{pmatrix}a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33}\\a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\end{pmatrix}\to \det (A)=(a_{11}\cdot a_{22}\cdot a_{33})+(a_{21}\cdot a_{32}\cdot a_{13})+(a_{31}\cdot a_{12}\cdot a_{23})-[(a_{13}\cdot a_{22}\cdot a_{31})+(a_{23}\cdot a_{32}\cdot a_{11})+(a_{33}\cdot a_{12}\cdot a_{21})]$

## Determinante de Matriz n x n

*Método 1: Gauss-Jordan:*

1. Llevar matriz a forma triangular o escalonada reducida.
2. Por cada operación de filas, se deberá llevar control del siguiente procedimiento:

**Cambio de Filas:**  $\det (A)=-\det (B)$

**Multiplicación por Escalar:**  $\det(A)=\frac{1}{\alpha}\cdot \det(B)$

**Suma o Resta de Filas:**   $\det(A)=\det(B)$

3. Multiplicar los elementos de la diagonal principal y aplicar las operaciones anteriores.

*ij-esimo Menor e ij-esimo Cofactor:*  

$M_{ij}=\det(M)$ (M = Matriz con fila i y columna j removidas)

$C_{ij}=(-1)^{i+j}\cdot M_{ij}$

### Determinante por Desarrollo de Cofactores

*Desarrollo de Cofactores por Fila:* $\det(A)=\sum^n_{k=1}a_{ik}\cdot C_{ik}(A)=a_{i1}\cdot C_{i1}+a_{i2}\cdot C_{i2}+\dots+a_{in}\cdot C_{in}$

*Desarrollo de Cofactores por Fila:*   $\det(A)=\sum^n_{k=1}a_{kj}\cdot C_{kj}(A)=a_{1j}\cdot C_{1j}+a_{2j}\cdot C_{2j}+\dots+a_{nj}\cdot C_{nj}$
<br>
## Rango y Matriz Inversa

*Rango de Matriz:* Cantidad de columnas pivote (Columnas con entrada principal) en la matriz escalonada.

*Matriz Inversa:*

1. Unir la Matriz con la Matriz Inversa de mismo orden.
2. Aplicar el método de Gauss-Jordan para obtener la forma escalonada reducida de la matriz.
3. La matriz A deberá terminar siendo la matriz Identidad, y la Identidad terminara siendo la matriz inversa, si y solo si, la matriz escalonada reducida es la Identidad.
4. La operación debería cumplirse $A\cdot A^{-1}=I$

##### Tags

#clase #class