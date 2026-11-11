# Proyecto de aula — Método de bisección

Aplicación web interactiva para aproximar raíces de funciones de una variable con el método de bisección. Incluye una gráfica, controles para recorrer las iteraciones y una tabla que se puede descargar en CSV.

## Cómo abrir la aplicación

Abre el enlace público de GitHub Pages del repositorio. También puedes descargar [`index.html`](index.html) y abrirlo en un navegador moderno como Chrome, Edge o Firefox. La aplicación funciona con JavaScript en el navegador y se puede usar sin instalar programas, sin servidor y sin credenciales. La conexión a internet solo se necesita para abrir el sitio publicado o cargar las fuentes de Google.

## Cómo usarla

1. Escribe la función en términos de `x` o selecciona un ejemplo. Usa `^` para las potencias, `*` para multiplicar y paréntesis en funciones como `cos(x)` y `sqrt(x)`.
2. Ingresa los extremos `a` y `b` del intervalo y una tolerancia positiva.
3. Pulsa **Calcular raíz**. Usa **‹**, **›** o **▶** para ver cómo se reduce el intervalo en cada paso.
4. Pulsa **Descargar tabla (CSV)** para guardar el registro de iteraciones.

### Ejemplo de prueba

Usa `x^3 - x - 2`, `a = 1`, `b = 2` y una tolerancia de `1e-6`. La raíz aproximada es **1,52138**.

## Método y limitaciones

La bisección calcula el punto medio `c = (a + b) / 2` y conserva la mitad del intervalo donde hay cambio de signo. La aplicación se detiene si encuentra un cero exacto o si la mitad del ancho del intervalo es menor que la tolerancia. También reconoce cuando un extremo ya es raíz.

El método requiere que la función sea continua en el intervalo y que los extremos tengan signos opuestos si ninguno es raíz. Un cambio de signo provocado por una discontinuidad puede producir un resultado engañoso. Si la función toca el eje sin cruzarlo, el intervalo puede no mostrar el cambio de signo requerido.

## Publicación en GitHub Pages

1. Sube `index.html` y `README.md` a la raíz de un repositorio público.
2. En **Settings → Pages**, selecciona **Deploy from a branch**.
3. Selecciona **main** y **/(root)** y guarda los cambios.
4. Cuando aparezca **Visit site**, abre la página y ejecuta el ejemplo de prueba.

Consulta la [guía oficial de GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).
