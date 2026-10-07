# CONTENIDO.md — Textos finales y comportamiento

Los textos van tal como están escritos. Si alguno no cabe en 360 px de ancho, se ajusta el diseño antes que el texto.

## Enlace de WhatsApp

Número de prueba: **+591 69328230**

**Mientras las inscripciones están abiertas**

- Mensaje: `Hola, quiero inscribirme al curso Experto en E-commerce del 16 de noviembre.`
- Enlace: `https://wa.me/59169328230?text=Hola%2C%20quiero%20inscribirme%20al%20curso%20Experto%20en%20E-commerce%20del%2016%20de%20noviembre.`

**Después del cierre**

- Mensaje: `Hola, quiero información sobre la próxima versión del curso Experto en E-commerce.`
- Enlace: `https://wa.me/59169328230?text=Hola%2C%20quiero%20informaci%C3%B3n%20sobre%20la%20pr%C3%B3xima%20versi%C3%B3n%20del%20curso%20Experto%20en%20E-commerce.`

Todos los botones de la página llevan al mismo enlace. Se abren en la misma pestaña.

## Línea de fecha

Cuenta los días que faltan para el **cierre de inscripciones: domingo 15 de noviembre de 2026** (supuesto), en hora de Bolivia (`America/La_Paz`, UTC−4). Se calcula con JavaScript al cargar la página.

| Momento | Texto de la línea | Texto del botón |
|---|---|---|
| Faltan 2 días o más | `Inscripciones hasta el domingo 15 de noviembre · faltan N días` | `Reserva tu cupo por WhatsApp` |
| Falta 1 día (sábado 14) | `Inscripciones hasta mañana, domingo 15 de noviembre` | `Reserva tu cupo por WhatsApp` |
| Domingo 15 | `Hoy cierran las inscripciones` | `Reserva tu cupo por WhatsApp` |
| Desde el lunes 16 | `Inscripciones cerradas · escríbenos para la próxima versión` | `Pregunta por la próxima versión` |

- Sin JavaScript, la línea muestra el texto fijo `Inscripciones hasta el domingo 15 de noviembre` y el botón funciona igual.
- Desde el lunes 16, el botón usa el segundo enlace.
- Referencia: el 7 de octubre de 2026 faltan 39 días.

## Medición

Cada botón de WhatsApp lleva `data-evento="clic_whatsapp"` y `data-ubicacion` con `primera-pantalla`, `barra-fija` o `cierre`. Un único manejador registra el toque (por ahora con `console.log`, dejando comentado dónde iría el evento de GA4). Sirve para explicar en la defensa qué se mediría y dónde se pierde la gente.

---

## 1. Primera pantalla

**Antetítulo**
Curso en vivo · UCB Tarija

**Titular**
En 2 semanas, diseña la operación completa de tu tienda online

**Frase de apoyo**
Para negocios que ya venden por redes o WhatsApp y quieren dejar de hacerlo todo a mano. Con Luis Canedo, cofundador de GOJA.

**Datos clave**
16 al 27 de noviembre · 6 sesiones en vivo por Zoom · 250 Bs · Certificado UCB

**Botón**
Reserva tu cupo por WhatsApp

**Línea de fecha**
(ver tabla de arriba)

## 2. Para quién es

**Título**
Si vendes así, este curso es para ti

- Tomas los pedidos por WhatsApp o Instagram y los anotas a mano.
- Cobras por QR y después revisas uno por uno quién pagó.
- Coordinas cada entrega por mensaje.
- Quieres vender más, pero ya no te alcanza el tiempo.

**Nota**
No necesitas título profesional para inscribirte.

**Dato de contexto**
Tu cliente ya paga en digital: en 2025 se hicieron 891 millones de pagos con QR en Bolivia.
Fuente: Asoban, informe de gestión 2025.

## 3. Tu docente

**Título**
Luis Canedo Arze

**Subtítulo**
Cofundador de GOJA y vicepresidente de Tecnología e IA

- Cofundó GOJA, empresa de e-commerce con operación en Bolivia y Estados Unidos.
- Más de 19 años en operaciones de e-commerce, procesamiento de pedidos y logística.
- Maestría en Gestión de Tecnologías de la Información (University of Salford, Reino Unido) e Ingeniero en Telecomunicaciones (UCB).

**Texto alternativo del retrato**
Luis Canedo Arze, docente del curso

**Pie de la foto del equipo**
El equipo de GOJA, la empresa de e-commerce que Luis cofundó.

**Texto alternativo de la foto del equipo**
El equipo de GOJA posa en un jardín detrás de letras grandes que forman la palabra GOJA

## 4. Qué te llevas

**Título**
Terminas con el plan de tu propia operación

**Introducción**
El proyecto final se hace sobre tu negocio. Entregas:

1. La plataforma elegida para tu tienda, con su justificación.
2. Tu flujo de compra completo, del primer clic a la entrega.
3. Una propuesta de logística y medios de pago.
4. El mapa de procesos de tu operación.

## 5. Temario

**Título**
Lo que vas a trabajar

1. **Modelos de e-commerce y marketplaces.** B2C, B2B o D2C: cuál le conviene a tu negocio.
2. **Selección de plataforma.** Shopify, WooCommerce o Wix, según costos, escala e integraciones.
3. **Catálogo, precios y medios de pago en Bolivia.** Para que comprar sea simple y seguro.
4. **Logística, fulfillment y atención al cliente.** De la preparación del pedido a la entrega.
5. **Automatización no-code y CRM básico.** Zapier y Make para dejar de repetir tareas.
6. **IA operativa.** Chatbots, recomendadores y automatización inteligente.

## 6. Datos prácticos

**Título**
Fechas, horario e inversión

| | |
|---|---|
| Fechas | Lunes 16, miércoles 18, viernes 20, lunes 23, miércoles 25 y viernes 27 de noviembre de 2026 |
| Horario | 19:00 a 21:30 |
| Modalidad | Virtual, en vivo por Zoom |
| Inversión | 250 Bs |
| Certificado | De aprobación, emitido por la UCB, con carga de 140 horas académicas |

**Nota bajo la tabla**
Las 140 horas suman las 6 sesiones en vivo, el trabajo en tu proyecto y la evaluación. Se aprueba con una prueba de conocimiento y el proyecto aplicado.

**Línea de confianza**
Universidad Católica Boliviana "San Pablo" · Sede Tarija · Desde 1966

## 7. Cierre

**Título**
Empieza el lunes 16 de noviembre

**Texto**
Escríbenos por WhatsApp y te contamos cómo inscribirte.

**Botón**
Reserva tu cupo por WhatsApp

**Línea de fecha**
(la misma de la primera pantalla)

## 8. Pie

Universidad Católica Boliviana "San Pablo" · Sede Tarija
Departamento de Ciencias Empresariales · Carrera de Marketing y Medios Digitales

Trabajo académico de la materia Marketing Móvil (MKD-314). No es la página oficial del curso.

---

## Metadatos de la página

- `<title>`: Experto en E-commerce · Curso en vivo · UCB Tarija
- Descripción: Curso en vivo de la UCB Tarija para negocios que ya venden por redes o WhatsApp. Del 16 al 27 de noviembre, con Luis Canedo, cofundador de GOJA. 250 Bs.
- `lang="es"`
