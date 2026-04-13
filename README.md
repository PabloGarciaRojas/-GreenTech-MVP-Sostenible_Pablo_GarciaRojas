# -GreenTech-MVP-Sostenible_Pablo_GarciaRojas

**Auditoría, Refactorización y Defensa de una Landing Page**

**Autor:** Pablo García Rojas

**Fecha:** 17 de Marzo 2026
 
## 1. Resumen Ejecutivo
Aquí presento el MVP refactorizado para la landing page de la campaña "Salvemos el Planeta". Al revisar el código original que me entregaron, vi que la web consumía muchísimos recursos y batería.
El código inicial tenía mucha "grasa digital" (bloatware) porque tenía frameworks enormes como Bootstrap o jQuery para hacer cosas súper básicas. Con esta refactorización ha sido demostrar que podemos tener una web visual y funcional, pero mucho más ligera, priorizando de verdad la eficiencia técnica y la sostenibilidad.

## 2. Auditoría Técnica y Acciones Realizadas
Para arreglar esto y aplicar un buen ecodiseño, he realizado cambios al código para poder conseguirlo.
He realizado varios cambios como:
* **Fuera frameworks pesados:** He quitado Bootstrap por completo y lo he sustituido por CSS Nativo (usando variables y Flexbox). Así evitamos que el móvil del usuario se sature leyendo miles de líneas de estilo que no se está usando.
* **Cero JavaScript:** Borré las librerías jQuery y Moment.js. El script que calculaba el año del pie de página lo he puesto a mano de forma estática en el HTML. Al final, el código más eficiente y sostenible es el que no necesita ejecutarse en el navegador. Lo que hice fue añadir un footer ya que con el script pedia la fecha, por lo que he añadido yo mismo la fecha.
* **Optimización de fuentes e iconos:** Solo le pido a Google Fonts los dos grosores de letra que realmente necesito (400 y 700). Además, quité la librería FontAwesome y puse el icono de la hoja directamente como un SVG en el HTML para ahorrar peticiones externas.
* **Imágenes eficientes:** Quité la imagen de fondo del CSS y la inserté en el HTML con una etiqueta img. Le bajé la resolución a 1200px y le añadí el loading lazy (para que no gaste datos si el usuario no hace scroll hacia abajo) y decoding="async"(para que su carga no congele el procesador).

## 3. Impacto en la Sostenibilidad, ASG y Economía Circular
Todos estos cambios técnicos no son solo para que la web cargue más rápido, sino que tienen un impacto físico real en el medio ambiente, siguiendo los principios de la Economía Circular:
1. **Menos consumo de red (Carbono Operacional):** Al quitar tanto código basura, la web pesa muchísimo menos. Esto significa que los servidores y las redes gastan menos energía en enviarle la página al usuario [1]. 
2. **Ahorro de batería (Green Software):** Una web que no obliga al procesador a pensar tonterías es una web que no calienta el móvil. Si la batería dura más, el usuario no tiene que cargar el teléfono tan a menudo [2]. 
3. **Freno a la obsolescencia programada (E-Waste):** Si los desarrolladores hacemos webs tan pesadas, obligamos a la gente a comprar móviles nuevos y más potentes continuamente. Al hacer una web ligera que funciona perfectamente y de forma fluida en móviles antiguos o de gama baja, alargamos la vida útil de ese hardware. Esto retrasa la obsolescencia programada y evita generar tanta basura electrónica [3].

## 4. Referencias
[1] W3C, "Web Sustainability Guidelines (WSG) 1.0," World Wide Web Consortium, 2023. [Online]. Available: https://www.w3.org/TR/wsgl/

[2] Green Software Foundation, "Green Software Practitioner Course," 2024. [Online]. Available: https://learn.greensoftware.foundation/

[3] R. Verdecchia, P. Lago, I. Malavolta, y G. Procaccianti, "Green IT and Green Software Engineering: A Systematic Mapping Study," arXiv preprint arXiv:2102.04945, 2021. [Online]. Available: https://arxiv.org/abs/2102.04945
