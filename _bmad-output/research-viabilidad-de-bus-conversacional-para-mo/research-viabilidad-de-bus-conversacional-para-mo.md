---
title: 'Market research: Viabilidad de bus conversacional para movilidad y delivery en Colombia y Latinoamérica'
type: 'market'
topic: 'Viabilidad de bus conversacional para movilidad y delivery en Colombia y Latinoamérica'
decision: 'Decidir si continuar con un componente B2B que conecte canales conversacionales con proveedores de movilidad y delivery mediante APIs autorizadas.'
source: 'native web research'
status: complete
preset: standard
validation: normal
created: '2026-11-14'
updated: '2026-11-14'
claims_verified: 0
claims_unverified: 5
claims_overturned: 1
---

# Market research: Viabilidad de bus conversacional para movilidad y delivery en Colombia y Latinoamérica

**Decision this research serves:** Decidir si continuar con un componente B2B que conecte canales conversacionales con proveedores de movilidad y delivery mediante APIs autorizadas.

_Sections are appended per the approved research plan; the executive summary is written last and placed here, first._

## Resumen ejecutivo

**Veredicto: viable con condiciones, pero no como un conector universal inmediato.** WhatsApp Business Platform y Telegram ofrecen interfaces oficiales suficientes para recibir y estructurar solicitudes. También hay proveedores con flujos API demostrables —Cabify, Uber Direct, Mensajeros Urbanos y Coordinadora—; por tanto, una primera versión autorizada es técnicamente construible. [1][2][3][4][5][6][30][31]

La tesis de integrar de inmediato WhatsApp con inDrive, DiDi, Rappi y Uber bajo una sola API **no está demostrada**. La evidencia pública muestra APIs y programas de partner heterogéneos: Uber Direct y Cabify documentan partes del flujo transaccional; Rappi publica integración merchant/POS, mientras que inDrive tiene su propio asistente de WhatsApp. No se halló una API pública comparable para inDrive, DiDi o Taxia, aunque ello no descarta acuerdos privados. [3][7][8][30][31]

El problema de grupos de WhatsApp no está vacío: varios productos ya venden “WhatsApp → despacho de flota propia” en Colombia. La diferenciación defendible tendría que ser la orquestación **autorizada** entre canales y múltiples proveedores, con un modelo de conectores, trazabilidad, consentimiento y acuerdos comerciales; no un chatbot genérico ni automatización de apps cerradas. [10][11][12][13]

La recomendación es continuar solo con un MVP de alcance estrecho: WhatsApp/Telegram más **uno o dos proveedores con API o partner program verificable** y un caso de uso acotado (por ejemplo, delivery empresarial o movilidad B2B). Antes de construir un bus multi-plataforma, conseguir por escrito disponibilidad, cobertura, sandbox, precios, SLA, autorizaciones y datos permitidos.

## Factibilidad técnica y de integración

### Canales de entrada

- **WhatsApp:** Meta ofrece la WhatsApp Business Platform/Cloud API para mensajes de negocio, webhooks y respuestas estructuradas; funciona como entrada oficial de chatbot al backend. Tiene reglas operativas, entre ellas plantillas y restricciones fuera de la ventana de atención. [1][14]
- **Telegram:** la Bot API, callbacks y Mini Apps permiten capturar solicitudes estructuradas y enviarlas a un backend propio. [2]
- **Apple:** Messages for Business es un canal comercial real, pero no se verificó una ruta pública y autocontenida para que un backend cualquiera se conecte en Colombia. FaceTime no encaja: la documentación encontrada cubre llamadas/asistencia en llamada, no bots ni transacciones. [15][16]

**Implicación:** WhatsApp y Telegram son los conectores iniciales realistas. Apple puede ser una investigación posterior; FaceTime debe excluirse del alcance de chatbot.

### Proveedores y APIs

| Proveedor / categoría | Evidencia encontrada | Implicación |
|---|---|---|
| Cabify | API B2B de ride-hailing con estimación, reserva/gestión de viajes y webhooks; también documentación logística. [3] | Candidato prioritario para validar cobertura y términos colombianos. |
| Uber Direct / Riders | Uber Direct documenta creación, gestión, monitoreo y webhooks; su guía de inicio documenta cotización y creación de entregas. Riders API documenta operaciones de viaje. Producción y autoservicio dependen de aprobación/región. [4][5][30][31] | Candidato, condicionado a confirmar Colombia y permiso B2B2C. |
| Mensajeros Urbanos / Coordinadora | Ambos publican APIs para creación y seguimiento de entregas/guías; Mensajeros Urbanos exige proceso comercial de integración. [6][17] | Alternativas locales más probables para el primer conector logístico. |
| Rappi | Integrations Manager/API PAv2 y POS para catálogo y operación de pedidos de Rappi. [7] | No debe presentarse como API pública para delivery externo hasta confirmación contractual. |
| inDrive | Producto empresarial colombiano con asistente propio de WhatsApp; no se verificó en esta pasada una cláusula específica de términos aplicable a middleware externo. [8][9] | Posible alianza; no integrar sin permiso escrito y documentación de partner. |
| DiDi / Taxia | Programas de comercio/empresa e integraciones asociadas, pero no documentación pública comprobada de creación/cotización/tracking para middleware. [18][19] | Requieren consulta directa de partner/API. |

## Mercado y competencia

El subsegmento “recibir por WhatsApp y despachar una flota propia” ya muestra oferta en Colombia: WhiteCloud, Lemonstart, Taxi Live/Festcar, Mekavo y Taxee declaran esa clase de capacidades. [10][11][12][13][20] Globia y Chazki cubren despacho, ruteo, logística e integraciones en la región. [21][22]

También existen plataformas de comercio conversacional —B2Chat, Blip, Botmaker, Yalo y Zenvia— que pueden competir por el canal de entrada o convertirse en partners de mensajería; la evidencia revisada no las muestra como agregadores multi-proveedor de movilidad. [23][24][25]

No se encontró evidencia de una solución regional consolidada que permita desde una sola API pública crear y gestionar libremente servicios de Rappi, Uber, DiDi, inDrive y otros. Esto es una **ausencia en la búsqueda**, no una prueba de inexistencia.

## Condiciones regulatorias y operativas en Colombia

El middleware no puede asumir el rol de operador. El Ministerio de Transporte distingue entre una plataforma tecnológica y la prestación del servicio: las empresas y vehículos habilitados conservan responsabilidad por el servicio; usar tecnología no habilita modalidades o vehículos no autorizados. [26][27]

La solución tratará datos de clientes, ubicaciones, conductores y solicitudes. La SIC exige mecanismos de autorización y acceso a política de tratamiento de datos en interfaces digitales; el diseño necesita consentimiento, minimización de datos, trazabilidad, roles responsable/encargado y revisión legal local. [28]

## Lo que muestra la combinación de evidencia

1. **El cuello de botella no es construir el bus.** Las APIs de chat y varias APIs logísticas demuestran factibilidad técnica. La restricción determinante es acceso contractual y operativo a cada proveedor.
2. **El primer nicho no debe ser “todos los taxis”.** Está competido si solo ofrece chatbot y despacho. Un piloto debe probar orquestación autorizada, reducción de trabajo manual o nueva demanda para un proveedor concreto.
3. **La estrategia de red solo funciona después del primer conector.** Cada proveedor conserva aprobación, seguridad, soporte y reglas de datos; la demanda agregada ayuda a vender, pero no sustituye el acuerdo.

## Recomendaciones

1. **No construir integraciones con inDrive, DiDi o Rappi mediante UI, scraping, cuentas de usuario ni bots sin autorización escrita.** La investigación no verificó una API pública transaccional para esos flujos; el acceso debe provenir de un acuerdo/documentación de partner.
2. **Hacer una diligencia comercial/técnica de cuatro candidatos:** Cabify, Uber Direct, Mensajeros Urbanos y Coordinadora. Solicitar cobertura, sandbox, endpoints, credenciales, webhooks, precios, SLA, responsabilidades y autorización para solicitudes de terceros. La recomendación tiene confianza media-alta: las capacidades públicas están documentadas, pero la disponibilidad comercial exacta no. [3][4][6][17]
3. **Prototipar solo el lado propio:** WhatsApp Cloud API/Telegram Bot API → modelo canónico de solicitud → simulador de proveedor. Esto valida experiencia y seguridad sin afirmar conexión a proveedores todavía. Confianza alta en factibilidad de canal; media en el valor comercial. [1][2]
4. **Contactar a Taxia o a un proveedor local para entrevista, no para prometer integración.** El objetivo es descubrir si existe API privada/partner y obtener criterios de éxito del despacho. [19]

## Preguntas abiertas

- ¿Qué ciudades colombianas y qué modalidades están disponibles actualmente para producción en Uber Direct y Cabify API?
- ¿Alguno de Rappi, inDrive, DiDi o Taxia ofrece una API privada/partner para requests externos y bajo qué cláusulas?
- ¿Qué proveedor local puede comprometer un piloto y qué métrica de valor acepta (solicitudes procesadas, tiempo de asignación, conversión, costo)?
- ¿Qué licencia, responsabilidad, seguros y tratamiento de datos aplican a cada flujo de taxi, delivery y mensajería?
- ¿Cuál era el proveedor de movilidad que el usuario asociaba con Jelpit? La empresa pública localizada se presenta como plataforma de pagos/recaudo. [29]

## Fuentes

Acceso a todas las fuentes: 2026-11-14. Cuando la fecha de publicación no era visible, se deja como no indicada en lugar de inferirla.

| Ref. | Hallazgo respaldado | Editor |
|---|---|---|
| [1] | WhatsApp Business Platform/Cloud API | [Meta](https://developers.facebook.com/documentation/business-messaging/whatsapp/overview) |
| [2] | Telegram Bot API | [Telegram](https://core.telegram.org/bots/api) |
| [3] | Cabify API ride-hailing | [Cabify Developers](https://developers.cabify.com/docs/ride-hailing) |
| [4] | Uber Direct overview | [Uber Developers](https://developer.uber.com/docs/deliveries/overview) |
| [5] | Uber Riders API | [Uber Developers](https://developer.uber.com/docs/riders/references/api) |
| [6] | Mensajeros Urbanos API | [Mensajeros Urbanos](https://integraciones.mensajerosurbanos.com/docs/intro) |
| [7] | Rappi Integrations Manager | [Rappi Colombia](https://merchants.rappi.com/es-co/para-que-sirve-el-integrations-manager-de-rappi) |
| [8] | inDrive Empresas Colombia | [inDrive](https://indrive.com/es-co/business) |
| [9] | Portal legal de inDrive; cláusula específica pendiente de verificar | [inDrive](https://indrive.com/es-co/legal) |
| [10] | WhiteCloud | [WhiteCloud](https://whitecloud.com.co/) |
| [11] | Lemonstart | [Lemonstart](https://lemonstart.com/) |
| [12] | Taxi Live | [Festcar](https://festcar.co/taxilive) |
| [13] | Mekavo | [Mekavo](https://mekavo.com/co/whatsapp) |
| [14] | Límites/cuenta WhatsApp Business | [Meta](https://developers.facebook.com/docs/graph-api/reference/whats-app-business-account) |
| [15] | Apple Messages for Business | [Apple](https://support.apple.com/es-la/102053) |
| [16] | FaceTime links | [Apple Developer](https://developer.apple.com/library/archive/featuredarticles/iPhoneURLScheme_Reference/FacetimeLinks/FacetimeLinks.html) |
| [17] | Coordinadora Developers | [Coordinadora](https://developers-dev.coordinadora.com/inicio) |
| [18] | DiDi Food para restaurantes | [DiDi Food](https://web.didiglobal.com/co/food/restaurantes/) |
| [19] | Taxia Life negocios | [Taxia Life](https://taxialife.com/negocios/) |
| [20] | Taxee | [Taxee](https://taxee.taxi/co/es/taxi-companies) |
| [21] | Globia | [Globia](https://www.globia.com.co/) |
| [22] | Chazki | [Chazki](https://www.chazki.com/preguntas-frecuentes) |
| [23] | B2Chat | [B2Chat](https://www.b2chat.io/en/) |
| [24] | Blip | [Blip](https://www.blip.ai/es/whatsapp/) |
| [25] | Botmaker | [Botmaker](https://botmaker.com/es/whatsapp-api) |
| [26] | Uso de plataformas tecnológicas de transporte | [Ministerio de Transporte](https://gestiondocumental.mintransporte.gov.co/nuez/2025/407/20254071089781_65495.pdf) |
| [27] | Posición sobre plataformas y responsabilidad | [Ministerio de Transporte](https://mintransporte.gov.co/publicaciones/3960/ministerio-fija-posicion-frente-a-utilizacion-de-plataformas-tecnologicas/) |
| [28] | Protección de datos / interfaces digitales | [SIC](https://sedeelectronica.sic.gov.co/sites/default/files/normativa/Circular%20externa%20002%20de%202026.pdf) |
| [29] | Jelpit | [Jelpit](https://jelpit.com/) |
| [30] | Uber Direct: inicio, cotización y creación | [Uber Developers](https://developer.uber.com/docs/deliveries/get-started) |
| [31] | Uber Direct webhooks | [Uber Developers](https://developer.uber.com/docs/deliveries/guides/webhooks) |

## Vigencia

Las capacidades API, términos, cobertura y programas de partner cambian rápidamente. Revalidar las fuentes [3]–[9], [14] y [18]–[19] antes de contactar clientes o prometer funcionalidades.

### Mapa de obsolescencia

Las seis afirmaciones de capacidad/política se deben revisar el **2027-02-01**. La afirmación regulatoria tomada como referencia quedó marcada como vencida por el cálculo (fecha fuente `2025-01`, ventana de 18 meses); debe sustituirse por asesoría jurídica o norma vigente antes de operar. La primera fecha de revisión pendiente es **2026-07-01**.
