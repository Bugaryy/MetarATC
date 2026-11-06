# Meteo ATC 3D

Simulador web 3D de meteorología para estudiantes y controladores de tránsito aéreo. Permite construir el cielo capa por capa, escribir un METAR y ver cómo se ve en la escena, practicar con escenarios aleatorios y comparar todo con un mapa de Panamá.

> Herramienta educativa y de simulación. No usar para planificación de vuelos ni como fuente meteorológica oficial.

Autor: **Delta Charlie** · [github.com/Bugaryy](https://github.com/Bugaryy)

## Qué incluye

La interfaz tiene una escena 3D a la izquierda y, a la derecha, un panel de mandos con una barra de iconos para cambiar de sección.

| Sección | Para qué sirve |
| --- | --- |
| **Nubes** | Hasta 3 capas como en un METAR. Eliges tipo (Ci, Cc, Cs, Ac, As, Sc, St, Ns, Cu, TCU, Cb), cobertura en octas y base. Muestra dónde queda cada capa respecto al nivel de 0 °C. |
| **Tiempo** | Situaciones listas, fenómenos (lluvia, tormenta, niebla, neblina…) con su intensidad, y controles de temperatura, punto de rocío, QNH, visibilidad y hora. |
| **Viento** | Dirección, velocidad y ráfagas sobre el aeropuerto de referencia, con el viento de frente y cruzado por pista. |
| **METAR** | Escribes o pegas un METAR y la escena se actualiza mientras tecleas. Avisa de errores y de grupos ignorados. |
| **Datos** | METAR generado, techo, visibilidad, categoría de vuelo (VFR, MVFR, IFR, LIFR), altitud de densidad y de presión, nivel de congelación y una lectura del tiempo para el ATC. |
| **Guía** | Referencia rápida de tipos de nube, categorías y claves del METAR. |
| **Práctica** | Escenarios aleatorios: lees el METAR, miras el cielo y respondes. |
| **Mapa** | Vista aérea de Panamá con nubes, radar, viento, rayos y estaciones METAR coloreadas por categoría, vinculada al METAR del simulador. |

### Vistas de cámara

- **Órbita**: vista general para girar y acercar.
- **Torre**: lo que ve el controlador desde la torre, con la visibilidad real en metros.
- **Pistas**: aproximación y pistas del aeródromo.
- **Panamá**: mapa del país.

### Detalles de la simulación

- Sol, sombras de nubes y colores de amanecer y atardecer según la hora del simulador (hora UTC; la hora local de Panamá es UTC−5).
- Niebla densa con visibilidad baja, igual de día y de noche.
- Si el METAR no indica el tipo de nube y el tiempo es tranquilo, el simulador sortea entre Cu, Sc, Ci, Cc y Cs según la altura, y a veces añade nubes altas que el METAR no reporta (base sobre 5 000 ft). **Enviar** vuelve a sortear, y puedes cambiar el tipo a mano.
- Unidades de visibilidad y altitud: aviación, km, ft o millas.
- Tema oscuro (grafito y ámbar) y tema claro, que se recuerda entre visitas.
- Funciona en escritorio, tableta y móvil.

## Cómo usarlo

1. Abre `index.html` (o el enlace publicado) en un navegador moderno con WebGL.
2. Elige una sección en la barra de iconos y ajusta los controles; la escena responde al instante.
3. Para empezar desde un METAR, ve a **METAR**, pégalo y mira el cielo.
4. Cambia de cámara con las pestañas de arriba. Arrastra para girar, usa la rueda o el pellizco para acercar y Mayús + arrastrar para desplazar.

Se necesita conexión a internet para cargar Three.js y las tipografías.

## Publicar en GitHub Pages

1. Sube el archivo HTML al repositorio con el nombre `index.html`, junto con `README.md` y `LICENSE`.
2. En **Settings → Pages**, elige la rama y la carpeta raíz.
3. La página queda disponible en `https://bugaryy.github.io/<repositorio>/`.

## Tecnología

- Un solo archivo HTML, sin pasos de compilación.
- [Three.js](https://threejs.org/) r128 para la escena 3D.
- IBM Plex Sans y IBM Plex Mono para la interfaz.

## Licencia

Todos los derechos reservados © 2026 Delta Charlie. Consulta [LICENSE](LICENSE). Para pedir permiso de uso o una licencia comercial, escribe al autor en [github.com/Bugaryy](https://github.com/Bugaryy).
