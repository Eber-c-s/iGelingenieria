# Revisión de IGEL Ingeniería y Construcción

Fecha: 2 de noviembre de 2026.

Se revisó el proyecto del ZIP adjunto. Estas correcciones están en los archivos entregados; no se publicó ningún cambio en el sitio alojado.

## Correcciones realizadas

- **Formulario:** se convirtió en un formulario real con campos obligatorios, validación de nombre, teléfono y correo opcional. Antes podía abrir WhatsApp sin completar nombre o teléfono. Se añadieron autocompletado, teclado telefónico y límites de longitud.
- **Texto del formulario:** se eliminó la promesa de enviar una copia por correo, porque no existe código que haga ese envío. WhatsApp abre el mensaje preparado; la persona debe pulsar enviar dentro de WhatsApp.
- **Galerías:** el zoom vuelve a su estado inicial al cambiar de proyecto. Se mantuvieron el avance, retroceso y selección de miniaturas.
- **Accesibilidad de la galería:** cierre con Escape, foco inicial en el botón de cerrar, recorrido con Tab dentro del diálogo, restitución del foco y bloqueo del desplazamiento del fondo. El zoom también responde a Enter y espacio.
- **Miniaturas en pantallas táctiles:** se eliminó un desplazamiento manual duplicado para permitir el desplazamiento nativo horizontal y vertical.
- **Menú móvil:** se añadieron nombre accesible, estado abierto/cerrado e identificación del menú controlado.
- **Navegación:** se definió la variable del área segura para que la cabecera adhesiva tenga una posición superior válida. Se añadió margen al navegar a secciones para evitar que sus títulos queden bajo la cabecera.
- **Pantallas pequeñas:** ajustes de título, estadísticas, tarjetas de contacto y botones del visor; tamaño de campos de 16 px para evitar el zoom automático de Safari en iPhone.
- **Movimiento reducido:** las animaciones respetan esa preferencia del dispositivo. El contenido no depende de una animación para ser visible.
- **Teléfono y correo:** se respetan los enlaces nativos y se añadió el signo + al teléfono internacional.
- **Carga:** las cuatro imágenes JPEG incrustadas repetidamente se guardaron en `images/assets/`. El HTML pasó de 1.437.519 bytes a aproximadamente 257.000 bytes. Las fotos siguen incluidas en el proyecto.
- **HTML inicial:** se actualizó la copia estática de la página para que coincida con la aplicación y conserve contenido legible antes de ejecutar JavaScript.
- **Imagen al compartir:** se sustituyó la ruta `/logo.jpg`, cuyo archivo no estaba incluido, por `/images/hero.webp`, que sí existe en el proyecto. Sigue pendiente confirmar el dominio.

## Comprobaciones realizadas

- Sintaxis de los dos scripts ejecutables: correcta.
- Estructura y cierre de etiquetas HTML; identificadores únicos: correctos.
- Referencias de imágenes locales: 276 archivos comprobados, sin archivos faltantes.
- Contenedores de las 272 imágenes WebP: tamaño y cabecera válidos.
- 12 tarjetas de proyectos, 11 galerías y 271 fotografías referenciadas en ellas.
- Enlaces internos: todos apuntan a secciones existentes.
- Pruebas de las funciones de la aplicación: menú móvil, apertura y cierre de cada proyecto, avance y retroceso circular, reinicio de zoom y composición del mensaje de WhatsApp.
- Validación de teléfono y codificación del mensaje con tildes, símbolos y saltos de línea.

Las pruebas de funciones se hicieron en un entorno de JavaScript con estado simulado. No equivalen a una prueba visual o a la validación nativa de formularios en un navegador. El navegador disponible no pudo acceder a los archivos locales, por lo que no se confirma visualmente la ausencia de desbordamientos ni el funcionamiento táctil en un teléfono real. No se enviaron mensajes de WhatsApp ni correos. Tampoco se comprobó la disponibilidad real del número, email, Instagram, fuentes externas o mapa.

## Datos que debes confirmar antes de publicar

1. **Dominio:** las etiquetas `og:url` y `og:image` usan `https://igel.cl`. Si tu dominio final es otro, actualiza ambas. La imagen para compartir debe tener una URL pública que funcione después de subir los archivos. Revisa por separado que `contacto@igel.cl` sea el correo correcto; no tiene por qué coincidir con el dominio web.
2. **Foto de Valle de Aconcagua:** esa tarjeta utiliza `images/proyectos/bodega-san-ignacio/09.webp`. No hay una carpeta propia de Valle de Aconcagua. Confirma que esa foto corresponda; no se cambió por otra sin evidencia.
3. **Testimonios y afirmaciones comerciales:** confirma los nombres y autorizaciones de los tres testimonios; también las cifras «50+ obras», «100% entregas a tiempo», «5 años de garantía», «certificado SEC» y la respuesta garantizada en menos de dos horas. No se validaron contra documentos de la empresa.
4. **Fechas, descripciones y ubicación:** revisa los plazos y detalles técnicos de los proyectos. En particular, el texto de Canal del Chucao menciona «Los Muermos, Puerto Varas»; confirma la ubicación que deba figurar.
5. **Duplicado de foto:** `hospital-quintero/09.webp` y `10.webp` tienen los mismos bytes. Se conservaron para no alterar el registro sin confirmación.

## Cómo usar esta entrega

Descomprime el ZIP y sube `index.html` junto con la carpeta `images` al mismo nivel en tu repositorio. Conserva los nombres y subcarpetas. El archivo `REVISION.md` es informativo y no es necesario para mostrar la página.

Después de publicar, verifica en un iPhone y un computador: menú, enlaces de secciones, apertura/cierre de galería, desplazamiento de miniaturas, zoom, campos inválidos y apertura del mensaje en WhatsApp. Confirma también la vista al compartir el enlace.

## Ajuste solicitado: segmentos de servicio

Se conservaron «Respuesta <2h», «Los Andes, V Región» y «Facturación electrónica». Debajo se añadió «Segmentos de servicio» con Industrial, Agrícola, Domiciliario, Minería, Energía y Servicios al Estado / Mercado Público, cada uno acompañado de un punto verde. La lista se distribuye en varias líneas según el ancho disponible.

## Ajuste solicitado: nuestros clientes

Se añadió una tercera sección, después de Nosotros y antes de Proyectos, con cinco logos de fuentes oficiales y distribución en columnas según el ancho disponible. Incluye Minera Los Pelambres, Agrícola Río Blanco (RIOblanco), Agrosano, Parque Arauco y Mercado Público con la leyenda «Servicios al Estado». Las fuentes están en LOGOS_CLIENTES.md. Se comprobó la presencia de las cinco imágenes locales, la estructura del HTML y el orden de las secciones. La comprobación visual en un navegador continúa pendiente.

## Ajuste solicitado: orientación de fotografías

Se inspeccionaron visualmente las 271 fotografías de las 11 galerías, la imagen principal y los recursos fotográficos de las otras secciones. Se detectaron cuatro fotografías giradas 90 grados en Escuela Pablo Neruda: 01, 02, 04 y 08.

Se corrigió su presentación mediante archivos SVG locales que conservan los píxeles de la fotografía, sin recorte ni reconstrucción. La rotación es de 90 grados hacia la izquierda. Se actualizaron la portada de la tarjeta, las miniaturas y las imágenes de la galería; también las referencias a esa foto en otras secciones. Los WebP originales se conservan.

Se renderizaron las cuatro versiones corregidas, se verificó visualmente su orientación y se compararon sus píxeles con la rotación exacta de los originales: coincidencia completa. También se verificaron las 271 rutas de galería. No se detectaron otros giros inequívocos; las tomas inclinadas o dirigidas hacia el suelo o techo se conservaron como fueron tomadas.

Para publicar, se deben subir el nuevo index.html y la carpeta images completa, incluidos los cuatro archivos terminados en -orientada.svg.
