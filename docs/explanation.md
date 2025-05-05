# Explicación del método numérico

La cuadratura Gaussiana es un método para calcular integrales definidas mediante una suma ponderada de valores de la función en puntos específicos (llamados puntos de colocación).

Para una función \( f(x) \), la integral en el intervalo \([-1, 1]\) se aproxima como:

\[
\int_{-1}^1 f(x)\,dx \approx \sum_{i=1}^N w_i f(x_i)
\]

donde:
- \(x_i\) son las raíces del polinomio de Legendre de grado \(N\),
- \(w_i\) son los pesos correspondientes.

Si la integral está definida en un intervalo arbitrario \([a, b]\), se realiza un cambio de variable:

\[
x = \frac{b - a}{2} x' + \frac{a + b}{2}
\]

Este método es especialmente eficiente porque logra alta precisión con pocos puntos de evaluación si la función es suave.

En nuestro caso, se usa cuadratura Gaussiana para evaluar la integral \(\int_0^\pi \sin(x^2) dx\), una función que requiere integración numérica precisa.

Pasos para usar la cuadratura gaussiana.

1-Elegimos un número n de puntos 
2-Calculamos los pesos con los polinomios de Legendre:

Los pesos se eligen tal que:
      - $\displaystyle w_k = \left[\frac{2}{1-x^2}\left(\frac{dP_N}{dx}\right)^{-2}\right]_{x={x_k}}$, con $x_k$ que cumple $P_N(x_k)=0$
     
3-Ahora evaluamos la función en los nodos

4-Por último multiplicamos cada ( f(x_i) ) por su peso correspondiente ( w_i ) y sumamos los resultados.
