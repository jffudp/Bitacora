# Bitacora
Proceso del semestre 

1. Gestos — reconocimiento y memes

**Idea:** crear una interacción en la que los movimientos de las manos y del rostro cambian la imagen o animación mostrada en pantalla. El proyecto tomó como referencia `meowmeowcatcam` y utiliza MediaPipe para detectar puntos de la cara y las manos.

**Proceso:** se organizó una interfaz con cámara y un panel de imágenes. A partir de los puntos detectados se definieron gestos: tres dedos, aprobación, señalar, oración, boca abierta y puño cerca de la cara. Cada gesto se vinculó a una imagen o GIF de la carpeta `memes`. Para evitar cambios rápidos e involuntarios, el sistema confirma el gesto durante varios fotogramas antes de actualizar la imagen.

**Resultado:** una experiencia web que relaciona la expresión corporal con memes. Se ejecuta mediante un servidor local y requiere permiso de cámara. La carpeta también contiene una versión de escritorio en Python y modelos locales.

**Para completar la bitácora:** registrar qué gestos costó reconocer, en qué condiciones se probó la cámara y agregar capturas de la interacción.

## 2. Dos realidades — dos lecturas de una cámara

**Idea:** explorar cómo una misma cámara puede producir dos representaciones distintas, sin mostrar directamente su imagen. La propuesta relaciona cuerpo, percepción y representación digital.

**Proceso:** se plantearon dos sistemas independientes. En el primero, MediaPipe identifica hasta dos manos y sus puntos se conectan en una telaraña geométrica de colores neón; cuando aparecen dos manos se añade un vínculo entre ellas. En el segundo, se comparan fotogramas consecutivos para detectar cambios de luminancia y generar partículas que caen como lluvia digital. La interfaz incorpora controles para activar o pausar cada sistema y una estética de terminal con bordes fracturados.

**Resultado:** dos visualizaciones simultáneas: una interpreta la estructura de la mano y la otra responde al cambio de la imagen. Se desarrolló con JavaScript, Canvas y MediaPipe, y necesita servidor local y permiso de cámara.

**Aprendizaje que propone:** el sensor no entrega una única representación; las reglas elegidas determinan qué aspecto del movimiento se vuelve visible. Conviene registrar pruebas de iluminación y sensibilidad para documentar sus límites.

## 3. Oír la luz / Fuga Vice City

**Idea:** traducir el movimiento de una autopista nocturna en una composición sonora. La intención es construir una interpretación audiovisual de las luces y el tráfico, no reproducir el sonido original del video.

**Proceso:** se seleccionaron tres videos de tráfico y un banco de ocho sonidos de carretera. La imagen se divide en una cuadrícula: el programa compara fotogramas y mide el cambio dentro de cada bloque. Cuando supera un umbral, activa una muestra sonora; la intensidad puede modificar el volumen y la posición horizontal puede definir el panorama. Se añadieron controles de sensibilidad, repetición, envolvente, filtro y reverberación, junto con indicadores visuales y un registro de eventos. También se incorporó la opción de cargar video o música propia, de modo que la energía de la música afecte la imagen.

**Resultado:** una consola audiovisual de estética nocturna en la que el video funciona como disparador de capas sonoras. El README del proyecto acredita los videos y sonidos y propone capturas para documentar la entrega.

**Observación:** el sistema detecta diferencias entre imágenes, no reconoce autos; los reflejos o el movimiento de cámara también pueden activar sonidos. Quedan como mejoras propuestas la separación por color y el uso de grabaciones propias.

## 4. Neon Salvage — tacto y dispositivos conectados

**Idea:** convertir el teléfono en un mando físico para un juego audiovisual que se presenta en el computador. Los dispositivos se comunican mediante MQTT.

**Proceso:** se desarrollaron una pantalla de juego y una interfaz de mando móvil, conectadas mediante una sala y un código QR. Se asociaron acciones del juego a entradas del teléfono: toque para desplazarse, toque sostenido o sacudida para saltar, varios dedos o voz para activar un escudo, giro para ajustar dirección y movimiento de cámara para activar un EMP. El juego se estructuró en cinco sectores y un jefe final, con gráficos dibujados en Canvas y sonido generado mediante Web Audio. Se prepararon opciones de conexión local y publicación web.

**Pruebas:** existe una pauta para revisar conexión, presión, diámetro de contacto, cantidad de dedos, giro, latencia, bloqueo de pantalla, micrófono y cámara en teléfonos reales. La tabla de resultados está vacía; por tanto, no se puede afirmar qué dispositivos se probaron ni cuáles fueron sus resultados.

**Resultado:** un juego de plataformas controlable desde un teléfono, con alternativas de teclado o ratón. La carpeta `tacto-main` aparece vacía en la revisión; la implementación documentada se encuentra en `ejercicio 7`.

## 5. Poetas — sistema editorial

**Idea y proceso reconstruido:** desarrollar una propuesta editorial para una colección de poetas, articulando tipografía, composición y formatos impresos. El portafolio reúne un afiche A3, una publicación y piezas desplegables como partes de un mismo sistema.

**Resultado:** una familia de piezas editoriales presentada mediante fotografías de detalles y un PDF del afiche. Los archivos revisados no permiten establecer las etapas concretas de investigación, bocetaje o producción; se pueden añadir fotografías, decisiones de materiales y fechas propias para completarlas.

## 6. Hard bop — sistema gráfico

**Idea y proceso reconstruido:** traducir el ritmo, la improvisación y la energía del jazz hard bop a una identidad gráfica aplicada en diferentes soportes. La propuesta se presenta como un afiche y una serie de posavasos relacionados visualmente.

**Resultado:** un sistema compuesto por el afiche, los posavasos y sus imágenes de presentación. Para completar el proceso, se pueden incorporar referentes musicales y visuales, bocetos, decisiones de color y tipografía, y registros de impresión.

## 7. Portafolio — diseño, procesos y proyectos

**Idea:** reunir los trabajos en una experiencia digital que explique quién es el autor, presente su perfil y permita recorrer cada proyecto.

**Proceso:** se seleccionaron y organizaron los proyectos en una página de inicio, una sección personal, un archivo y páginas individuales. Se construyó un lenguaje visual compartido con el monograma JD, tipografías Space Grotesk y DM Mono, una familia de morados y un acento naranja. Se incorporaron componentes interactivos, entre ellos tarjetas arrastrables, cursor dibujado y botón magnético. La navegación y la grilla se adaptaron a pantallas móviles; los proyectos digitales se acompañan de registros en video y los impresos de imágenes y PDF.

**Resultado:** un sitio estático desarrollado con HTML, CSS y JavaScript, con una carpeta `dist` para publicación. El README del portafolio registra los créditos de componentes y fuentes, y describe el uso de IA como apoyo técnico.

## Cierre personal

Todos los proyectos están subidos y publicados. El portafolio reúne los trabajos y permite recorrer sus resultados, registros y enlaces en un mismo lugar.
