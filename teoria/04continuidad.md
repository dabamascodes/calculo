---
title: "Tema 3 - Límites y continuidad"
author: "Juan Gabriel Gomila, Arnau Mir y Llorenç Valverde"
date: ''
output: 
  ioslides_presentation: 
    css: Mery_style.css
    fig_caption: yes
    keep_md: yes
    logo: Images/calculus.gif
    widescreen: yes
---



# Introducción

## Funciones reales de variable real

Supondremos que son conocidos el concepto de **función**, en tanto que una **aplicación** entre conjuntos de números. En particular, nos concentraremos en **funciones reales de variable real**, es decir en funciones $f:\mathbb{R} \rightarrow \mathbb{R}$.

Tambien suponemos conocidos los cenceptos de **rango** y **dominio** de una función, así como los términos **variable independiente** y **dependiente**. 

Aunque seran tratadas con detalle más adelante, es conveniente tener presentes las principales características de funciones elementales como las polinómicas $f(x)= P_n(x) = a_nx^n+a_{n-1}x^{n-1}+ \cdots + a_1x+a_0$, la exponencial $f(x)=e^x$,  las trigonométricas $f(x)=\sin(x)$, $f(x)=\cos(x)$, $f(x) =\tan(x)$, entre otras. 

## Funciones reales de variable real

Uno de los principales objetivos del càlculo es el estudio las funciones. De hecho, como ya se ha mencionado, el **cálculo diferencial** trata del estudio de la **medida del cambio**, precisamente a través de relaciones que vienen expresadas como funciones, principalmente como **funciones reales de variable real**

La primera cuestión que se aborda tiene que ver con los **números reales**, en particular cómo **evaluar las funciones reales de variable real** cuando la **variable independiente** es un número **irraciona**l. Nuevamente el concepto de **límite** viene a ayudar en la solución de esta cuestión.

## Límite de una función en un punto

<l class="definition"> **Definición. Límite de una función en un punto.** </l>

Sea $f:A \subset \mathbb{R}$ una función definida sobre el conjunto $A \subset \mathbb{R}$ y sea $x_0$ un punto de acumulación de $A$. $L \in \mathbb{R}$ es el **límite de $f(x)$ cuando $x$ tiende a $x_0$** si para toda sucesión $\{x_n\}_{n \in \mathbb{N}}$ de puntos de $A$ tal que $\lim_{n \rightarrow \infty}x_n = x_0$ es $\lim_{n \rightarrow \infty}f(x_n)=L$.

Escribiremos, $\lim_{x \rightarrow x_0}f(x)=L$, para indicar el límite de $f(x)$ cuando $x$ tiende a $x_0$. 


##  Límite de una función en un punto
<l class="observ"> **Observaciones.** </l>

**1.** Igual que hemos hecho con las sucesiones y los números irracionales, con esta definción convertimos el problema de evaluar una función en un punto irracional en el de calcular el límite de una sucesión. 

**2.** El hecho requerir que $x_0$ sea un punto de acumulación de $A$, nos garantiza que existan sucesiones $\{x_n\}$ de puntos de $A$ tales que $\lim_{n\rightarrow \infty} x_n = x_0$ y, por lo tanto, la definición tiene sentido.

**3.** Si $x_0$ es un punto **aislado** de $A$, es decir si hay un entorno de $x_0$ en el cual no hay puntos de $A$ diferentes de $x_0$, entonces no tiene sentido hablar del límite de $f$ en ese punto.

## Límite de una función en un punto: Ejemplos.

<div class="example"> **Ejemplos**

**Ejemplo 1.** Sea $f: \mathbb{R}\rightarrow \mathbb{R}$ definida por $f(x)=x$ y sea $c \in \mathbb{R}$, entonces
$$
\lim_{x \rightarrow c} x = c
$$
puesto que para cualquier sucesión $x_n  \rightarrow c$ es obvio que $f(x_n) = x_n \rightarrow c$.

**Ejemplo 2.** Análogamente si ahora es $f(x) = \dfrac{1}{x}$ y $c \neq 0$, entonces 

$$
\lim_{x \rightarrow c} \dfrac{1}{x} = \dfrac{1}{c},
$$
puesto que si $x_n \rightarrow c$, entonces $\dfrac{1}{x} \rightarrow \dfrac{1}{c}$

</div>

## Límite de una función en un punto: Ejemplos

<div class="example"> **Ejemplos**

**Ejemplo 3.** Si $f(x) = P_n(x) = a_n x^n + a_{n-1}x^{n-1}+ \cdots + a_1 x + a_0$, entonces para todo $c \in \mathbb{R}$ es
$$
\lim_{x \rightarrow c}P_n(x) = P_n(c) = a_n c^n + a_{n-1}c^{n-1}+ \cdots + a_1 c + a_0,
$$
como se deduce fácilmente de las propiedades aritméticas de los límites de sucesiones.

**Ejemplo 4.** Igualmente, si $P_n(x)$ y $Q_m(x)$ són polinomios tales que $P_n(x_0) \ne 0$ y $Q_m(x_0) \ne 0$, entonces 
$$
\lim_{x \rightarrow x_0} \dfrac{P_n(x)}{Q_m(x)} = \dfrac{P_n(x_0)}{Q_m(x_0)}.
$$
**Ejemplo 5.** Si $f(x) = e^x$, entonces $\lim_{x \rightarrow x_0} e^x = e^{x_0}$ puesto que, como hemos demostrado, si $x_n \rightarrow x_0$, entonces $e^{x_n} \rightarrow e^{x_0}$.
</div>


## Límite de una función en un punto: Ejemplos

<div class="example"> **Ejemplos**

**Ejemplo 6.** Más interesante és el caso $\lim_{x \rightarrow 1} \dfrac{x^5-2x^3+1}{x-1}$, puesto que, en principio, para $x=1$ la función no está definida al anularse el denominador, es decir que el dominio de la función es $\mathbb{R}\setminus\{1\}$ y, por lo tanto, $1$ es un punto de acumulación del dominio.

Ahora bien, dado que el numerador también se anula en este punto, podemos simplificar la fracción por $x-1$, con lo que nos queda que $\dfrac{x^5-2x^3+1}{x-1} = x^4+x^3-x^2-x$, y por lo tanto, $\lim _{x \rightarrow 1} \dfrac{x^5-2x^3+1}{x-1} = \lim _{x \rightarrow 1} x^4+x^3-x^2-x = 0$. 
</div>

## Caracterización del límite: propiedad $\epsilon-\delta$.

<l class="prop"> **Proposición** </l>

Sea $f:A \subset \mathbb{R} \rightarrow \mathbb{R}$ una función definida sobre el conjunto $A \subset \mathbb{R}$ y sea $x_0$ un punto de acumulación de $A$. entonces son equivalentes las tres afirmaciones siguientes:

  a) $\lim_{x \rightarrow x_0}f(x)=L$
  
  b) Para todo $\epsilon >0$ existe un $\delta >0$ tal que siempre que $0<|x-x_0|< \delta$, entonces es $|f(x)-L|<\epsilon$. (**Propiedad $\epsilon-\delta$**).

  c) Para todo entorno abierto de $L$, $V_{\epsilon}(L)$, existe un entorno abierto de $x_0$, $V_{\delta} (x_0)$ tal que para todo $x \in V^*_{\delta} (x_0)$ es $f(x) \in V_{\epsilon}(L)$, donde $V^*_{\delta}= V_{\delta} \setminus \{x_0\}$, es decir el entorno reducido de $x_0$ y radio $\delta$


## Caracterización del límite: propiedad $\epsilon-\delta$

<div class="dem"> **Demostración**

 Veamos en primer lugar que 2) $\implies$ 1). Sea $x_n$ una sucesión de puntos distintos de $x_0$, tal que $x_n \rightarrow x_0$.

Supongamos que para todo $\epsilon >0$ existe $\delta >0$ tal que si $|x - x_0|< \delta$, entonces $|f(x)-L|<\epsilon$. 

Dado que $\delta >0$, existe $n_0$ tal que para todo $n > n_0$ es $|x_n - x_0|<\delta$, por lo tanto será $|f(x_n) - L| < \epsilon$, para todo $n > n_0$, por lo que, efectivamente, $f(x_n) \rightarrow L$.

</div>

## Las dos definiciones son equivalentes

<div class="dem">

Demostramos la otra implicación por contraposición, es decir usando la equivalencia $b \implies a \equiv \lnot a \implies \lnot b$. 

Suponemos, pues, que $\lim_{x \rightarrow x_0} f(x) \neq L$, es decir que hay un $\epsilon > 0$ tal que para todo $\delta >0$ existe $x_{\delta}$ tal que $|x_{\delta} - x_0|<\delta$ y $|f(x_{\delta}) - L| \geq \epsilon$. 

Se trata de ver que hay una sucesión, $\{x_n\}$ que tiene límite  $x_0$ y que $f(x_n) \not\rightarrow_{x \rightarrow x_0} L$. 

Consideremos ahora la sucesión de números positivos $\frac{1}{n}$, y los correspondientes $x_n$ tales que $|x_n-x_0|< \frac{1}{n}$, es $|f(x_n) -L | \geq \epsilon$, es decir $f(x_n) \not\rightarrow L$, en tanto que $x_n \rightarrow x_0$, que es lo que se quería demostrar.

Finalmente, en lo que se refiere al tercer apartado, es suficiente tener en cuenta que que $|x-x_0| < \delta$ si, y sólo si,  $x \in V_{\delta}(x_0)$.

</div>

## Ejemplo de la propiedad $\epsilon-\delta$

<div class="example"> **Ejemplo**


Si $f(x)=\dfrac{1}{x}$, dado un punto $c>0$, tenemos para $x>0$, 
$$
\left|\dfrac{1}{x} -\dfrac{1}{c}\right|= \left|\dfrac{1}{cx}(c-x)\right| = \dfrac{1}{cx}|c-x|
$$
Ahora, si $x$ es tal que $|x-c| <\dfrac{1}{2}c$, de tal manera que $\dfrac{1}{2}<x<\dfrac{3}{2}$, por lo que $0 < \dfrac{1}{cx} <  \dfrac{2}{c^2} \quad \text{ para } |x-c|< \dfrac{1}{2}c$.
Por lo tanto, para estos valores de $x$ tenemos que
$$
\left|\dfrac{1}{x} -\dfrac{1}{c}\right| \leq \dfrac{2}{c^2} |x-c|
$$


Ahora, dado un $\epsilon >0$ bastaá tomar $\delta = \min \left\{\dfrac{1}{2}c, \dfrac{1}{2}c^2 \epsilon \right\}$ para tener asegurado que si $|x -c|<\delta$, entonces $\left|\dfrac{1}{x} -\dfrac{1}{c}\right| < \epsilon$.

</div>


##  Ejemplo de la propiedad $\epsilon-\delta$

<div class="example"> **Ejemplo**

Veamos que $\lim_{x \rightarrow 2} \dfrac{x^3-4}{x^2+1}= \dfrac{4}{5}$
$$
\left|\dfrac{x^3-4}{x^2+1} -  \dfrac{4}{5}\right|= \left|\dfrac{5x^3-20-4x^2-4}{5(x^2+1)}\right| = \dfrac{|5x^2+6x+12|}{5(x^2+1)}|x-2|
$$
Ahora, si $|x-2|<1$, o equivalentemente, si $0<x<3$, tendremos que $\dfrac{|5x^2+6x+12|}{5(x^2+1)} \leq \dfrac{15}{2}$, puesto que el numerador es menor o igual que $15$ y el numerador mayor o igual que $2$. 

Si para un $\epsilon >0$ tomamos $\delta = \min \left\{1, \dfrac{2}{15} \epsilon \right\}$, tendremos que si $|x-2| < \delta$, entonces 
$$
\left|\dfrac{x^3-4}{x^2+1} -  \dfrac{4}{5}\right| < \epsilon
$$
que era lo que queríamos demostrar.

## Sobre la propiedad $\epsilon-\delta$

<l class="observ"> **Observaciones** </l>

**1.** La propiedad $\epsilon -\delta$, significa que dada una precisión cualquiera, $\epsilon$, para el resultado, $L$, podemos determinar la precisión, $\delta$, con la que hay que tomar la aproximación, $x$ de $c$, para tener asegurada la precisión requerida para $L$.

**2.** Los ejemplos anteriores muestran que $\delta$ puede depender de $\epsilon$, por lo que sería más apropiado escribir $\delta(\epsilon)$, lo que no se acostumbra a hacer para evitar complicar la notación en exceso, lo cual no és óbice para olvidar esta dependencia.

**3.** Los ejemplos anteriores también pueden producir la impresión, equivocada, que es más conveniente usar la primera definición de límite que la propiedad $\epsilon-\delta$, pero veremos que, en ocasiones, resulta más conveniente esta última que la primera.

## La propiedad $\epsilon-\delta$

<div class="center">
<img src="Images/epdel0.png" width="600px" />
</div>

## Propiedades del límite de una función

<l class="definition"> **Definición** </l>

Sea $f:A \subset \mathbb{R} \rightarrow \mathbb{R}$ y $c$ un punto de acumulación de $A$. $f$ **está cotada en un entorno de $c$** $V_{\delta}(c)$ si existe una constante $M \in \mathbb{R}$ tal que $|f(x)| \leq M$ para todo $x \in A \cap V_{\delta}(c)$.

<l class="prop"> **Proposición**

Sea $f:A \subset \mathbb{R} \rightarrow \mathbb{R}$ y $c$ un punto de acumulación de $A$. Si $\lim _{x \rightarrow c} f(x) =L$, entonces f está acotada en un entorno de $c$.

<div class="dem"> **Demostración**

Dado $\epsilon=1>0$, existe $\delta$ tal que $|f(x)|-|L| \leq |f(x)-L|<1$, para todo $x \in A \cap V_{\delta}(c)$. Por consiguiente si $M= |L|+1$, es $|f(x)| < |L|+1 = M$.

</div>

## Propiedades del límite de una función

<l class="definition"> **Definición** </l>

Sean $f,g:A \subset \mathbb{R} \rightarrow \mathbb{R}$ dos funciones reales de variable real. Entonces

1) $f+g: A \subset \mathbb{R} \rightarrow \mathbb{R}$ es la función definida por $(f+g)(x) = f(x)+g(x)$

2)  $f \cdot g: A \subset \mathbb{R} \rightarrow \mathbb{R}$ es la función definida por $(f\cdot g)(x) = f(x) \cdot g(x)$

3) Si $g(x)\neq 0$ en un $A$, entonces $\dfrac{1}{g}:A \subset \mathbb{R} \rightarrow \mathbb{R}$ es la función definida por $\dfrac{1}{g}(x)= \dfrac{1}{g(x)}$

4) Si $\lambda \in \mathbb{R}$, entonces $\lambda \cdot f: A \subset \mathbb{R} \rightarrow \mathbb{R}$ es la función definida por $(\lambda \cdot f)(x)= \lambda \cdot f(x)$.


## Propiedades del límite de una función


<l class="prop"> **Proposición** </l>

Sean $f,g:A \subset \mathbb{R} \rightarrow \mathbb{R}$ dos funciones reales de variable real y $c$ un punto de acumulñación de $A$, tales que $\lim_{x \rightarrow c} f(x) = L_1$ y $\lim_{x \rightarrow c} g(x)= L_2$. Entonces

P1. $\lim_{x \rightarrow c}(f+g)(x) = L_1+L_2$

P2. $\lim_{x \rightarrow c}(f \cdot g)(x) = L_1 \cdot L_2$

P3 $\lim_{x \rightarrow c} (\lambda \cdot f)(x) = \lambda \cdot L_1$

P4. Si $L_2 \neq 0$, entonces $\lim_{x \rightarrow c} \dfrac{f(x)}{g(x)} = \dfrac{L_1}{L_2}$

## Propiedades del límite de una función

<div class="dem"> **Demostración**

P1, P2 y P3 son una consecuencia inmediata de la definción de límite de una función. En el caso de P1, por ejemplo, tenemos que si $x_n \rightarrow c$ entonces $f(x_n) \rightarrow L_1$ y $g(x_n) \rightarrow L_2$, por lo tanto, 

$$
\lim_{x \rightarrow c}(f+g)(x)= \lim_{n  \rightarrow \infty} (f+g)(x_n)= \lim_{n  \rightarrow \infty} \left( f(x_n)+g(x_n) \right)
$$

$$=  \lim_{n  \rightarrow \infty} f(x_n) + \lim_{n  \rightarrow \infty} g(x_n) = L_1+L_2 = \lim_{x \rightarrow c} f(x) + \lim_{x \rightarrow c} g(x) 
$$


Por lo que se refiere a P4, tenemos que si $L_2 \neq 0$, entonces hemos demostrado, en el tema de límite de sucesiones, que para toda sucesión $x_n$ de puntos de $A$ tal que $g(x_n) \rightarrow L_2$, existe $n_0$ tal $g(x_n) \neq 0$ para todo $n \geq n_0$ y, además, $\lim_{n \rightarrow \infty}\dfrac{1}{g(x_n)} = \dfrac{1}{L_2}$ y, por lo tanto,
$$
\lim_{x \rightarrow c} \dfrac{f(x)}{g(x)} = \dfrac{L_1}{L_2}.
$$


## Propiedades del límite de una función

<l class="prop"> **Proposición** </l>

Si para todo $x \in A$ es $a \leq f(x) \leq b$, entonces $a \leq \lim_{x \rightarrow c} f(x) \leq b$

<l class="prop"> **Proposición** </l>

Sean $f,g,h :A\subset \mathbb{R} \rightarrow \mathbb{R}$, tales que $h(x) \leq f(x) \leq g(x)$, para todo $x \in A$, y

que $\lim_{x \rightarrow c} g(x) =  \lim_{x \rightarrow c} h(x) = L$, entonces  
$$
\lim_{x \rightarrow c} f(x) = L.
$$

<div class="exercise"> **Ejercicio**

Las demostraciones de estas dos proposiciones son del todo análogas a las correspondientes en el caso de límites de sucesiones y se dejan como ejercicio.
</div>


## Propiedades del límite de una función

<l class="prop"> **Proposición**

Sean $f:A \subset \mathbb{R} \rightarrow \mathbb{R}$ y $c$ un punto de acumulación de $A$. Si $\lim _{x \rightarrow c} f(x) = L>0$, entonces existe $\delta > 0$ tal que $f(x)>0$ para todo $x \in V^*_{\delta}(c) \cap A$.

Análogamente, si Si $\lim _{x \rightarrow c} f(x) = L <0$, entonces existe $\delta > 0$ tal que $f(x)<0$ para todo $x \in V^*_{\delta}(c) \cap A$.

<div class="dem"> **Demostración**

Supongamos, en primer lugar que $L>0$. Sea $\epsilon = \dfrac{L}{2} > 0$, entonces, por ser $L= \lim _{x \rightarrow c} f(x)$, existe $\delta >0$ tal que $|f(x)-L|<\dfrac{L}{2}= \epsilon$, por lo tanto, tenemos que $-\dfrac{L}{2} < f(x) - L < \dfrac{L}{2}$ y por lo tanto, es $0 <\dfrac{L}{2} < f(x)$. 

La demostración para el caso $L<0$ es completamente similar y se deja como ejercicio.

## Límites laterales


La función $f:\mathbb{R} \setminus \{0\} \rightarrow \mathbb{R}$, $f(x) = \dfrac{x}{|x|}$, no està definida en el punto ${0}$, de hecho, se trata de la función
$$ 
f(x) =
\begin{cases}
\;\;   1, & \mbox { si } x>0 \\
-1, & \mbox { si } x<0
\end{cases}
$$
conocida como la función *signo* de $x$. 

$0$ es un punto de acumulación del dominio de $f$, pero no existe el $\lim_{x \rightarrow 0} f(x)$

## Límites laterales

No existe el $\lim_{x \rightarrow 0}f(x)$. 

En efecto, consideremos la sucesión de término general $x_n = \dfrac{(-1)^n}{n}$, entonces es $f(x_{2k})= 1$ en tanto que $f(x_{2k+1})=-1$, para todo $k \in \mathbb{N}$, es decir que la sucesión de término general $f(x_n)$ tiene dos subsucesiones con límite diferente y, por lo tanto, $f(x_n)$ no tiene límite. 

En definitiva no existe el $\lim_{x \rightarrow 0}f(x)$.


## Límites laterales: gráfica de la función signo

<div class="center">
  <img src="Images/sgn1.png" width="600px" />
</div>

## Límites laterales

<l class="definition"> **Definición de límite lateral** </l>

@) Sea $f: A \subset \mathbb{R} \rightarrow \mathbb{R}$ una función real de variable real y sea $c$ un punto de acumulación de $A$. $L \in \mathbb{R}$ es el **límite lateral por la derecha** de $f$ en $c$, si para toda sucesión $x_n$ tal que $x_n \rightarrow c$ con $x_n \geq c$, es $f(x_n)\rightarrow L$. Escribiremos 
$$
L = \lim_{x \rightarrow c^+}f(x).
$$


@) Análogamente, $L \in \mathbb{R}$ es el **límite lateral por la izquierda** de $f$ en $c$, si para toda sucesión $x_n$ tal que $x_n \rightarrow c$ con $x_n \leq c$, es $f(x_n)\rightarrow L$. Escribiremos 
$$
L = \lim_{x \rightarrow c^-}f(x).
$$



## Límites laterales 

<div class="example"> **Ejemplos**

@) En el caso de la función *signo*, $f(x) = \dfrac{x}{|x|}$, hemos visto que  $\lim_{x \rightarrow 0^+}f(x) = 1$ y  $\lim_{x \rightarrow 0^-}f(x) = -1$.

@) Sea $g:\mathbb{R} \rightarrow \mathbb{R}$, la función definida por
$$
g(x)=
\begin{cases}
x+1, & \mbox{ si } x \leq 0 \\
x^2, & \mbox{ si } x > 0 
\end{cases}
$$
Entonces $\lim_{x \rightarrow 0^+} g(x) = 1$ y $\lim_{x \rightarrow 0^-} g(x) = 0$.

@) Sea $h:\mathbb{R} \rightarrow \mathbb{R}$, la función definida por
$$
h(x)=
\begin{cases}
x+1, & \mbox{ si } x \leq 0 \\
x^2+1, & \mbox{ si } x > 0 
\end{cases}
$$
Entonces $\lim_{x \rightarrow 0^+} h(x) = 1$ y $\lim_{x \rightarrow 0^-} h(x) = 1$. y, como veremos a continuación, existe el $\lim_{x \rightarrow 0} h(x)$ y es igual a $1$.

## Gráfica de la función g 

<div class="center">
  <img src="Images/gx.png" width="600px" />
</div>

## Gráfica de la función h 

<div class="center">
  <img src="Images/hx.png" width="600px" />
</div>

## Límites laterales

<div class="exercise"> **Ejercicios**

En lo que sigue,  $f: A \subset \mathbb{R} \rightarrow \mathbb{R}$ es una función real de variable real y $c$ es un punto de acumulación de $A$.

@) Demuestra que $L = \lim_{x \rightarrow c^+}f(x)$ si, y sólo si, para todo $\epsilon >0$, existe $\delta >0$ tal que, siempre que $0<x-c<\delta$, entonces es $|f(x)-L| < \epsilon$. 

@) Demuestra que   $L = \lim_{x \rightarrow c^-}f(x)$ si, y sólo si,si para todo $\epsilon >0$, existe $\delta >0$ tal que, siempre que $0<c-x<\delta$, entonces es $|f(x)-L| < \epsilon$.

@) Demuestra que  $L = \lim_{x \rightarrow c^+}f(x)$ si, y sólo si, para todo $\epsilon >0$, existe $\delta >0$ tal que si $x \in V^*_{\delta} (x) \cap (c, +\infty)$, entonces $f(x) \in V_{\epsilon}(L)$

@) Demuestra que  $L = \lim_{x \rightarrow c^-}f(x)$ si, y sólo si, para todo $\epsilon >0$, existe $\delta >0$ tal que si $x \in V^*_{\delta} (x) \cap (-\infty, c)$, entonces  entonces $f(x) \in V_{\epsilon}(L)$.

</div>


## Límites laterales

<l class="prop"> **Proposición**

Sea $f: A \subset \mathbb{R} \rightarrow \mathbb{R}$ y sea $c$ un punto de acumulación de $A$. Entonces existe el $\lim_{x \rightarrow c}f(x)$ si, y sólo si, los dos límites laterales $\lim_{x \rightarrow c^+}f(x)$ y $\lim_{x \rightarrow c^-}f(x)$
existen y son iguales.

## Límites laterales

<div class="dem"> **Demostración**

Si $\lim_{x \rightarrow c}f(x) = L$, entonces para toda sucesión $x_n$ tal que $x_n \rightarrow c$ es $f(x_n) \rightarrow L$. Ahora, si $x_n \rightarrow c$ y $x_n > c$ será igualemente $f(x_n) \rightarrow L$. Análogamente si $x_n <c$.

Supongamos ahora que los dos límites laterales existen y son iguales a $L$. Sea $x_n$ tal que $x_n \rightarrow c$, entonces tres casos són posibles:1) todos los $x_n$ a partir de un lugar son tales que $x_n \geq c$, 2) todos los $x_n$ a partir de un lugar son tales que $x_n \leq c$, y 3) existen infinitos $x_{n_k}$ tales que $x_{n_k} \geq c$ e infinitos $x_{n_j}$ tales que $x_{n_j} \leq c$, claramente $\{x_n\}= \{ x_{n_k}\} \cup \{x_{n_j}\}$.

En todos los casos es $f(x_n) \rightarrow L$, en el primero por ser $\lim_{x \rightarrow c^+}f(x)$ y en el segundo por ser  $\lim_{x \rightarrow c^-}f(x)$. El el tercer caso tendríammos dos subsucesiones $f(x_{n_k})$ y $f(x_{n_j})$ con el mismo límite L y, por lo tanto es $f(x_n) \rightarrow L$, dado que $\{x_n\}= \{ x_{n_k}\} \cup \{x_{n_j}\}$. En definitiva es  $\lim_{x \rightarrow c}f(x) = L$.


## Limites infinitos

<l class="definition"> **Definición**

Sean $f: A \subset \mathbb{R} \rightarrow \mathbb{R}$ y $c$ un punto de acumulación de $A$,

@) Diremos que $\lim_{x \rightarrow c}f(x) = +\infty$, si para cada $K >0$ existe un $\delta > 0$ tal que si $x \in V^*_{\delta}(c)$ entonces es $f(x)>K$.

@) Diremos que $\lim_{x \rightarrow c}f(x) = - \infty$, si para cada $K >0$ existe un $\delta > 0$ tal que si $x \in V^*_{\delta}(c)$ entonces es $f(x)< -K$

<div class="exercise"> **Ejercicio** 

Las definiciones anteriores también se pueden formular en términos de sucesiones así, por ejemplo, se pide comprobar que la primera definición es equivalente a

$\lim_{x \rightarrow c}f(x) = +\infty$ si, y sólo si, para toda sucesión $x_n$ tal que $x_n \rightarrow c$ es $f(x_n) \rightarrow \infty$. 

</div>

## Limites infinitos: Ejemplos.

<div class="example"> **Ejemplo**

$\lim_{x \rightarrow 0} \dfrac{1}{x^2} = \infty$, puesto que si $x_n \rightarrow 0$ entonces para todo $K>0$ existe $n_0$ tal que para todo $n > n_0$ es $|x_n| <K$ y, por lo tanto $|f(x_n)|=\dfrac{1}{x_n^2}>K^2$.


<div class="center">

 <img src="Images/inversax2.png" width="500px" />
</div>

## Límites en el infinito

El ejemplo anterior también sirve para justificar la siguiente definición:

<l class="definition"> **Definición** </l>

Sean $f: \mathbb{R} \rightarrow \mathbb{R}$ y $L \in \mathbb{R}$, $L = lim_{x \rightarrow \infty}f(x)$ si para toda sucesión $x_n$ tal que $\lim_{n \rightarrow \infty}x_n= \infty$ entonces $\lim_{n \rightarrow \infty} f(x_n)= L$.

Análogamente, $L = lim_{x \rightarrow -\infty}f(x)$ si para toda sucesión $x_n$ tal que $\lim_{n \rightarrow \infty}x_n= -\infty$ entonces $\lim_{n \rightarrow \infty} f(x_n)= L$.

<div class="exercise"> **Ejercicios**

@) Demuestra que $L = lim_{x \rightarrow \infty}f(x)$ si, sólo sí, para todo $\epsilon >0$ existe $K>0$ tal que si $x>K$ entonces $|f(x)-L|<\epsilon$.

@) Demuestra que $L = lim_{x \rightarrow -\infty}f(x)$ si, sólo sí, para todo $\epsilon >0$ existe $K>0$ tal que si $x<-K$ entonces $|f(x)-L|<\epsilon$.

## Limites en el infinito

<div class="example"> **Ejemplos**

@) $\lim_{x \rightarrow \infty} \dfrac{1}{x^2} = 0$, puesto que dado un $\epsilon >0$ para $K=\dfrac{1}{\sqrt{\epsilon}}$ es $f(x)= \dfrac{1}{x^2} < K$ siempre que $x >K$

@) Anàlogamente $\lim_{x \rightarrow -\infty} \dfrac{1}{x^2} = 0$, puesto que dado un $\epsilon >0$ para $K=\dfrac{1}{\sqrt{\epsilon}}$ es $f(x)= \dfrac{1}{x^2} < K$ siempre que $x <-K$

@) La función $h(x) = \dfrac{1}{x}$, proporciona un interesante ejemplo de también tienen sentido los límites laterales para los límites infinitos, puesto que como es fácil comprobar $\lim_{x \rightarrow 0^+} h(x) = +\infty$ en tanto que $\lim_{x \rightarrow 0^-} h(x) = -\infty$. 

@) También es fácil comprobar que $\lim_{x \rightarrow -\infty} \dfrac{1}{x} =0 = \lim_{x \rightarrow \infty}  \dfrac{1}{x}$


## Límites en el infinito: Gráfica de la función $\dfrac{1}{x}$

<div class="center">

 <img src="Images/inversx.png" width="600px" />
</div>

# Cálculo de límites


## Infinitésimos

<l class="definition"> **Definición** </l>

Sea $c$ un punto de acumulación del dominio de una función $f: A \subset \mathbb{R} \rightarrow \mathbb{R}$. $f$ es un **infinitésimo** en $c$ si $\lim_{x \rightarrow c}f(x) =0$.

<div class="example"> **Ejemplos**

1. $f(x)=x$ en el punto $0$,
2. $g(x)= \sin x$, en $x=0$ y, en general, en todos los puntos de la forma $(2k+1)\pi$, con $k \in \mathbb{N}$,
3. $h(x) = e^x -1$ en $x=0$,
4. $k(x)= \cos x$ en $x=\dfrac{\pi}{2}$ y, en general en todos los $x=\dfrac{(2k+1)}{2}\pi$, con $k \in \mathbb{N}$,
5. $l(x)= \dfrac{1}{x^2}$ en $x=\pm \infty$,
6. $p(x) = e^{\frac{1}{x}}$ en $x=\pm\infty$

<div>

## Infinitésimos equivalentes

<l class="definition"> **Definición** </l>

Sean $f$ y $g$ dos infinitésimos en $c$, entonces $f$ y $g$ son **equivalentes** si 
$$
\lim_{x \rightarrow c} \dfrac{f(x)}{g(x)}=1
$$

<div class="example"> **Ejemplos**

1. $f(x)= 3x -5x^2$ y $g(x)=3x$ en $x=0$, puesto que el $\lim_{x \rightarrow 0} \frac{3x-5x^2}{3x} =1$.
2. $h(x)= e^x -1$ y $p(x)=x$, en $x=0$, puesto que el $\lim_{x \rightarrow 0} \dfrac{e^x-1}{x}=1$.
3. $\log (1+x)$ y $x$ son equivalentes en $x=0$, puesto que $\lim_{x \rightarrow 0} \dfrac{\log(1+x)}{x} = \lim_{x \rightarrow 0} \log(1+x)^\frac{1}{x} = \log \lim (1+x)^\frac{1}{x} = \log e =1$.





## Infinitésimos equivalentes

<div class="example"> **Ejemplo**

Las funciones $\sin x$ y $x$ son infinitésimos equivalentes en $x=0$

<div class="center">

 <img src="Images/sinxx1.png" width="600px" />
</div>

## Cálculo del $\lim_{x \rightarrow 0}\dfrac{sin x}{x}$

<div class="center">

<img src="Images/sinxx.png" width="300px" />
</div>

El área del triangulo $ABE$ es $\frac{1}{2} \sin \alpha$

El área del sector circular $ABE$ es $\frac{1}{2} \alpha$

El área del triángulo $ADE$ es $\frac{1}{2} \tan \alpha$


## Cálculo del $\lim_{x \rightarrow 0}\dfrac{sin x}{x}$

Claramente, la relación entre estas tres áreas es la siguiente
$$
\frac{1}{2} \sin \alpha < \frac{1}{2} \alpha < \frac{1}{2} \tan \alpha
$$
Dividiendo por $\frac{1}{2} \sin \alpha$ y tomando recíprocos, queda
$$
\cos \alpha < \dfrac{\sin \alpha}{\alpha} < 1
$$
Por lo tanto,
$$
1 = \lim_{x \rightarrow 0^+} \cos x \leq \lim_{x \rightarrow 0^+}\dfrac{\sin x}{x} \leq 1
$$

## Cálculo del $\lim_{x \rightarrow 0}\dfrac{sin x}{x}$

Análogamente tenemos
$$
1 = \lim_{x \rightarrow 0^-} \cos x \leq \lim_{x \rightarrow 0^-}\dfrac{\sin x}{x} \leq 1
$$
En definitiva, como los dos límites laterales existen y son iguales, resulta que
$$
\lim_{x \rightarrow 0}\dfrac{\sin x}{x} =1
$$
Por lo tanto, $\sin x$ y $x$ son infinitésimos equivalentes en $0$.

## Infinitésimos equivalentes.

<l class="prop"> **Proposición** </l>

Sean $f,g,h: A \subset \mathbb{R} \rightarrow \mathbb{R}$ y sea $c$ un punto de acumulación de $a$. Supongamos, además que $f(x)$ y $g(x)$ son infinitésimos equivalentes en $x =c$. Entonces

1. Existe el $\lim_{x \rightarrow c} f(x)h(x) = L$ si, y sólo si, existe el $\lim g(x)h(x)=L$. 


2. Existe el $\lim_{x \rightarrow c} \dfrac{f(x)}{h(x)} = L$ si, y sólo si, existe el $\lim \dfrac{g(x)}{h(x)}=L$.

<div class="observ"> **Observación**

La proposición anterior establece que, en el cálculo de un límite, se pude substituir un infinitésimo por otro equivalente, siempre que el infinitésimo multiplique o divida a la otra función involucrada. No se puede substituir si forma parte de una suma o de una diferencia.

</div>

## Infinitésimos equivalentes

<div class="dem"> **Demostración**

1. Multiplicando y dividiendo por $g(x)$, tendremos que 
$$
L = \lim_{x \rightarrow c} f(x).h(x) = \lim_{x \rightarrow c} \dfrac{f(x)}{g(x)}\dfrac{g(x)}{h(x)}= \lim_{x \rightarrow c}\dfrac{f(x)}{g(x)} \lim_{x \rightarrow c} \dfrac{g(x)}{h(x)} = \lim_{x \rightarrow c} \dfrac{g(x)}{h(x)}
$$

2. La demostración és análoga a la anterior.

</div>

<div class="example"> **Ejemplo**

Cálculo del límite $\lim_{x \rightarrow 0} \dfrac{\sin 2x}{3x -5x^3}$

Primero, usamos la equivalencia entre $3x -5x^3$ y $3x$ y, acontinuación, la que hay entre $\sin 2x$ y $2x$:
$$
\lim_{x \rightarrow 0} \dfrac{\sin 2x}{3x -5x^3}= \lim \dfrac{\sin 2x}{3x} = \dfrac{2}{3}\lim\dfrac{\sin 2x }{2x}= \dfrac{2}{3}
$$
</div>