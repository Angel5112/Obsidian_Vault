### Vectores en el Plano
#### Conceptos Básicos

**Requisitos de un vector en el Plano:**  $P(a_{1}, b_{1})$ y $Q(a_{2},b_{2})$ 

**Vector dado dos Puntos:**  $\vec{PQ}=Q - P=(a_{2}-a_{1}, b_{2}-b_{1})=(a, b)=ai+bj$

**Vector Opuesto:**  $-\vec{PQ}= (-a, -b)=-ai-bj$
<br>
#### Álgebra de Vectores

Sean los vectores -> $\vec{u}=(a_{1},b_{1})$ y $\vec{v}=(a_{2},b_{2})$

**Multiplicación por Escalar:**  $\alpha \cdot\vec{u}=(\alpha \cdot a_{1}, \alpha \cdot b_{1})$

**Suma de Vectores:**  $\vec{u}+\vec{v}=(a_{1}+a_{2}, b_{1}+b_{2})$

**Diferencia de Vectores:**  $\vec{u}-\vec{v}=(a_{1}-a_{2},b_{1}-b_{2})$
<br>
#### Paralelidad de Vectores

Dos vectores son **paralelos** si existe un escalar $\vec{u}=\alpha \cdot\vec{v}$

#### Norma o Magnitud de un Vector y Vectores Unitarios

**Norma. Modulo o Magnitud:**  $\mid \vec{v}\mid=\sqrt{ a^2+b^2 }$

**Vector Unitario:**  Todo vector con $\mid \vec{v}\mid=1$

**Vector Unitario con misma dirección a otro vector:**  $\vec{u}=\frac{\vec{v}}{\mid \vec{v}\mid}$

**Desigualdad Triangular:**  $\mid \vec{u} + \vec{v}\mid\leq \mid \vec{u}\mid+\mid \vec{v}\mid$
<br>
#### Ángulo de un Vector

$\theta=\begin{cases}\tan^{-1}\left( \frac{b}{a} \right), 0^{\circ}\leq \theta\ <90^{\circ}\\90^{\circ}, a=0, b>0\\tan^{-1}\left( \frac{b}{a} \right)+180^{\circ}, 90^{\circ} \leq \theta\leq 270^{\circ}\\270^{\circ}, a=0, b<0\\tan^{-1}\left( \frac{b}{a} \right)+360^{\circ}, 270^{\circ}\leq \theta<360^{\circ}\end{cases}$
<br>
#### Combinación Lineal de Dos Vectores

Dados los vectores $\vec{u}$ ,$\vec{v}$  y siendo $\alpha$ y $\beta$ escalares, la **combinación lineal** de ambos vectores viene dado por $\vec{w}=\alpha \cdot \vec{u}+\beta \cdot \vec{v}$
<br>
### Vectores en el Espacio

#### Conceptos Básicos

**Requisitos de un Vector en el Espacio:**  $P(a_{1}, b_{1}, c_{1})$ y $Q(a_{2},b_{2},c_{2})$

**Vector dado dos Puntos:**  $\vec{PQ}=Q-P=(a_{2}-a_{1},b_{2}-b_{1},c_{2}-c_{1})=(a,b,c)=ai+bj+ck$

**Vector Opuesto en el Espacio:**  $-\vec{PQ}=(-a,-b,-c)=-ai-bj-ck$
<br>
#### Álgebra de Vectores en el Espacio

Sean los vectores -> $\vec{u}=(a_{1},b_{1},c_{1})$ y $\vec{v}=(a_{2},b_{2},c_{2})$

**Multiplicación por Escalar:**  $\alpha \cdot\vec{u}=(\alpha \cdot a_{1}, \alpha \cdot b_{1},\alpha \cdot c_{1})$

**Suma de Vectores:**  $\vec{u}+\vec{v}=(a_{1}+a_{2}, b_{1}+b_{2},c_{1}+c_{2})$

**Diferencia de Vectores:**  $\vec{u}-\vec{v}=(a_{1}-a_{2},b_{1}-b_{2},c_{1}-c_{2})$
<br>
#### Paralelidad de Vectores en el Espacio

Dos vectores son **paralelos** si existe un escalar $\vec{u}=\alpha \cdot\vec{v}$

#### Norma o Magnitud de un Vector y Vectores Unitarios en el Espacio

**Norma. Modulo o Magnitud:**  $\mid \vec{v}\mid=\sqrt{ a^2+b^2+c^2 }$

**Vector Unitario:**  Todo vector con $\mid \vec{v}\mid=1$

**Vector Unitario con misma dirección a otro vector:**  $\vec{u}=\frac{\vec{v}}{\mid \vec{v}\mid}$
<br>
#### Producto Punto y Producto Cruz

**Producto Punto:**  $\vec{u}\cdot \vec{v}=a_{1}a_{2}+b_{1}b_{2}+c_{1}c_{2}$

**Teorema:**  Dos vectores son ortogonales si el producto punto es igual a 0

**Producto Cruz:**  $\vec{u}\times \vec{v}=\begin{vmatrix}i&j&k\\a_{1}&b_{1}&c_{1}\\a_{2}&b_{2}&c_{2}\end{vmatrix}=[b_{1}\cdot c_{2}-(c_{1}\cdot b_{2})]i-[a_{1}\cdot c_{2}-(c_{1}\cdot a_{2})]j+[a_{1}\cdot b_{2}-(b_{1}\cdot a_{2})]k$

**Teorema:**  Dos vectores son paralelos si el producto cruz es igual a 0
<br>
#### Ángulo entre dos Vectores

Dados dos vectores no nulos, el ángulo entre ellos es $\theta=\cos^{-1}\left( \frac{\vec{u}\cdot \vec{v}}{\mid \vec{u}\mid \cdot \mid \vec{v}\mid} \right)$
<br>
#### Componente y Proyección entre dos Vectores

**Componente de un Vector u sobre un Vector v:**  $comp_{v}u=u\cdot\frac{v}{\mid v\mid}$

**Proyección de un Vector u sobre un Vector v:**  $proy_{v}u=v\cdot\frac{u\cdot v}{\mid v\mid^2}$
<br>
#### Ángulos y Cosenos Directores de un Vector

$\vec{v}=(a_{1},b_{1},c_{1})\to\begin{cases}\cos \alpha=\frac{a_{1}}{\mid v\mid}\\cos \beta=\frac{b_{1}}{\mid v\mid}\\cos \lambda=\frac{c_{1}}{\mid v\mid}\end{cases}\to \begin{cases}\alpha=\cos^{-1}\left( \frac{a_{1}}{\mid v\mid} \right)\\ \beta=\cos^{-1}\left( \frac{b_{1}}{\mid v\mid} \right)\\ \lambda=\cos^{-1}\left( \frac{c_{1}}{\mid v\mid} \right)\end{cases}$
<br>
##### Tags

#clase #class

