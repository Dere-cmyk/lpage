# DESIGN.md — Dirección visual

Decisiones ya tomadas. Lo que no esté aquí queda a criterio de quien construye, dentro de estas reglas.

## Intención

Una página de universidad que le habla a alguien que trabaja: sobria, directa, con una sola nota de color. Tiene que verse hecha a mano y no salida de una plantilla. Si una decisión es "lo que haría cualquier generador", se cambia.

## Color

Tres colores y nada más.

| Token | Valor | Origen | Uso |
|---|---|---|---|
| `--gris` | `#4C4C4C` | Pantone Cool Gray 11, manual de marca UCB | Fondo de la primera pantalla y del cierre. Texto sobre blanco. Texto sobre amarillo. |
| `--blanco` | `#FFFFFF` | — | Fondo de las secciones de lectura. Texto y logo sobre gris. |
| `--amarillo` | `#FFCD00` | Aproximación al Pantone 116 (pendiente el hex oficial) | Solo el botón de WhatsApp y, como máximo, dos datos clave sobre gris. |
| `--gris-claro` | `#F2F2F2` | Es el fondo exacto del retrato de Luis Canedo | Fondo de la sección del docente, para que la foto se funda sin recortarla. |

### Contraste medido

| Combinación | Ratio | Veredicto |
|---|---|---|
| Blanco sobre gris | 8,6:1 | Sí |
| Gris sobre blanco | 8,6:1 | Sí |
| Gris sobre gris claro | 7,7:1 | Sí |
| Amarillo sobre gris | 5,7:1 | Sí |
| Gris sobre amarillo | 5,7:1 | Sí (texto del botón) |
| Amarillo sobre blanco | 1,5:1 | **Nunca**, ni texto ni líneas finas |
| Blanco sobre amarillo | 1,5:1 | **Nunca** |

### Reglas

- El amarillo es escaso a propósito: si aparece en más de un elemento por pantalla, deja de señalar el botón.
- Sobre blanco, el amarillo solo puede existir como relleno del botón, y el botón debe llevar además un borde o sombra en gris para no depender de un contraste de 1,5:1 contra el fondo.
- Grises derivados para texto secundario o bordes: se permiten, pero ningún texto sobre blanco puede ser más claro que `#767676` (4,5:1).
- Sin degradados, sin un cuarto color, sin azul.
- El gris como fondo grande puede verse plano. Se compensa con tipografía de buen tamaño, mucho aire y la foto; no con texturas ni brillos.

## Logo

- **Principal:** el logotipo de nombre completo, "Universidad Católica Boliviana · Tarija". Va arriba a la izquierda, sobre gris.
- **Secundario:** el escudo, junto a la mención del certificado o en el pie.
- Los archivos son **blancos con fondo transparente**: solo van sobre `--gris`. Sobre blanco o gris claro son invisibles.
- Respetar el área libre alrededor; no recolorear, deformar ni poner sobre la foto.

## Tipografía

Dos familias como máximo, de licencia libre.

- **Titulares:** serif humanista con carácter, emparentada con la serif del logotipo (el manual de marca de 2020 indica Scala, que es comercial). Peso regular, interlineado apretado, sin mayúsculas sostenidas.
- **Texto e interfaz:** sans humanista, legible a 16–18 px en celular. Cifras tabulares en fechas y precio.
- Evitar las tipografías que delatan plantilla. Elegir probando el titular real a 360 px de ancho, no por costumbre.
- Tamaños de partida en móvil: titular 34–40 px, subtítulos 24–28 px, texto 17–18 px, notas 14–15 px. Nada por debajo de 14 px.

## Estructura (móvil primero)

Una columna. Secciones que alternan fondo para marcar el ritmo.

| # | Sección | Fondo |
|---|---|---|
| 1 | Primera pantalla | Gris |
| 2 | Para quién es | Blanco |
| 3 | Luis Canedo | Gris claro |
| 4 | Qué te llevas | Blanco |
| 5 | Temario | Blanco |
| 6 | Datos prácticos y certificado | Gris claro |
| 7 | Cierre con botón | Gris |
| 8 | Pie | Gris |

### Primera pantalla

En este orden, y todo visible sin desplazarse en un celular de 360 × 740 px:

1. Logotipo UCB Tarija. Sin menú.
2. Antetítulo corto.
3. Titular.
4. Frase de apoyo, que nombra a Luis Canedo.
5. Bloque de oferta: datos clave, botón de ancho completo y línea de fecha, agrupados como una unidad.
6. El borde superior de la foto de Luis Canedo asomando al final, para invitar a bajar.

### Botón de WhatsApp

- Relleno amarillo, texto gris, ícono de WhatsApp a la izquierda del texto.
- Ancho completo en móvil, alto mínimo 56 px, esquinas poco redondeadas.
- Es el único elemento amarillo sólido de la página.
- **Barra fija inferior:** al salir de la primera pantalla aparece una barra con el mismo botón, al alcance del pulgar. Se oculta cuando el botón del cierre entra en pantalla, para no mostrar dos a la vez.
- Estados: reposo, presionado y foco visible.

### Línea de fecha

Una sola línea de texto, sin cajas, sin segundos, nunca más grande que el botón. La lógica está en `CONTENIDO.md`.

## Imágenes

| Archivo | Uso | Notas |
|---|---|---|
| `assets/luis-canedo.jpg` | Retrato principal en la sección 3; asoma al final de la primera pantalla | 800 × 533 px, fondo `#F2F2F2`. Tamaño medio, nunca a sangre completa. No quitar el fondo. |
| `assets/equipo-goja.jpg` | Franja ancha en la sección 3, con pie de foto | 1280 × 720 px. Funciona como prueba de que GOJA existe, no para reconocer caras. |
| `assets/logo-ucb-tarija-blanco.png` | Encabezado | Solo sobre gris. |
| `assets/escudo-ucb-blanco.png` | Pie o certificado | Solo sobre gris. |

- La selfie con el equipo no se usa.
- Sin fotos de banco de imágenes ni ilustraciones genéricas. Si falta una imagen, se resuelve con tipografía.
- Exportar en WebP con respaldo JPG, declarar `width` y `height`, y cargar de forma diferida todo lo que esté fuera de la primera pantalla.

## Movimiento

Casi ninguno. Como mucho, la entrada de la barra fija y el estado presionado del botón. Respetar `prefers-reduced-motion`.

## Referencias: qué se toma de cada una

- **ClimbCon:** la foto del ponente con su nombre en la primera pantalla.
- **Marble:** titular que nombra el problema, una sola frase de apoyo y botón de ancho completo.
- **Shopify:** un bloque que agrupa la oferta y la acción.
- **ICON:** fecha en el color de acento, pegada al botón.
- **Amica:** confianza por trayectoria de la institución.

## Lo que no se hace

- Degradados de colores, sombras de neón o efecto vidrio.
- Eslóganes vacíos en mayúsculas.
- Contador de cuatro cajas con segundos corriendo.
- Menú de navegación, enlaces a redes o segundo llamado a la acción.
- Tarjetas dentro de tarjetas; íconos decorativos en cada viñeta.
- Formulario o campo de correo.
- Testimonios, cifras de inscritos o "últimos cupos" inventados.
- Carruseles.
- Centrar todo el texto: los párrafos van alineados a la izquierda.
