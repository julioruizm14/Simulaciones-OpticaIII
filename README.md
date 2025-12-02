# Simulaciones de Óptica III

Este repositorio contiene una colección de prácticas y simulaciones numéricas desarrolladas en Python para la asignatura de **Óptica III**. El proyecto abarca desde los fundamentos del procesamiento de señales hasta la simulación avanzada de propagación de ondas y haces complejos.

**Autor:** Julio David Ruiz Mendoza

## Contenido del Repositorio

El código está organizado en tres notebooks principales, cada uno enfocado en un bloque temático de la óptica física y computacional:

### 1. [Práctica 1: Convolución de Señales](P1OIII.ipynb)
Introducción al tratamiento matemático de señales y sistemas lineales invariantes en el tiempo (LSI).
* **Convolución Discreta:** Implementación y cálculo de la suma de convolución $y[n] = x[n] * h[n]$, comparando métodos propios con la función nativa `numpy.convolve`.
* **Convolución Continua:** Análisis de funciones analíticas y resolución numérica de la integral de convolución $y(t) = \int x(\tau)h(t-\tau) d\tau$.

### 2. [Práctica 2: Transformadas de Fourier y Muestreo](P2OIII.ipynb)
Generación de funciones ópticas bidimensionales y análisis en el dominio de la frecuencia.
* **Función de Airy:** Modelado de la función de dispersión de punto (PSF) de una lente circular, representando la intensidad como $I(r) = |2J_1(r)/r|^2$.
* **Transformada de Fourier (DFT):** Cálculo y visualización del espectro de funciones de apertura clásicas como el círculo ($circ$) y el rectángulo ($rect$).
* **Estudio de Aliasing:** Análisis de los efectos del teorema de muestreo en la calidad de la transformada numérica y cómo evitar artefactos en las imágenes.

### 3. [Práctica 3: Propagación de Ondas y Haces Especiales](P3OIII.ipynb)
Simulación numérica de la difracción y propagación de la luz en el espacio libre.
* **Aproximación de Fresnel:** Implementación de la propagación mediante tres métodos numéricos distintos para analizar sus ventajas y limitaciones:
    1.  **Espectro Angular:** Uso de la función de transferencia $H(f_x, f_y)$.
    2.  **Convolución Numérica:** Respuesta impulsional espacial.
    3.  **Método de una sola FFT:** Transformada con escalado de coordenadas para distancias largas.
* **Propagación Exacta:** Comparación de la aproximación paraxial con la solución exacta mediante la integral de **Rayleigh-Sommerfeld**.
* **Haces Complejos:**
    * Simulación de **Axicones** y generación de haces de Bessel (ver `Axicon.PNG`).
    * Generación y propagación de **Vórtices Ópticos** con carga topológica (ver `Vortice.PNG`).

El repositorio incluye archivos de imagen (`Axicon.PNG`,`barbara.png`, `Vortice.PNG`, `webb.png`) que se utilizan dentro de los notebooks como parte de los enunciados teóricos

## Tecnologías y Requisitos
Las simulaciones están escritas en **Python 3** y están diseñadas para ejecutarse en un entorno de Jupyter Notebook o Google Colab.

**Librerías principales:**
* `numpy`: Para operaciones matriciales, mallados y cálculo numérico.
* `matplotlib`: Para la visualización de campos complejos, perfiles de intensidad y mapas de color.
* `scipy`: Para funciones especiales (Bessel) y algoritmos eficientes de FFT (`scipy.fft`).

## Instrucciones de Uso
1. Clona este repositorio:
   ```bash
   git clone [https://github.com/tu-usuario/simulaciones-optica-iii.git](https://github.com/tu-usuario/simulaciones-optica-iii.git)
   ```
   
2. Asegúrate de tener las librerías necesarias instaladas:
   ```bash
   pip install numpy matplotlib scipy
   ```
3. Abre los archivos .ipynb con Jupyter Notebook o Google Colab para interactuar con las simulaciones.

