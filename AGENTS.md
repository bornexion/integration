# Contexto del proyecto: Bus de integraciones para plataformas de servicios

Este proyecto explora una posible iniciativa latinoamericana: una capa de integración (un "bus") que permita a aplicaciones de comunicación y a negocios solicitar, cotizar, coordinar y dar seguimiento a servicios de plataformas de movilidad, domicilios y logística.

## Idea central

Una persona o negocio podría escribir en un canal conversacional como WhatsApp o Telegram una petición en lenguaje natural, por ejemplo: "envía este pedido", "pide un viaje para este paciente" o "necesito un mensajero". El sistema transforma esa petición en un flujo estructurado y, cuando exista autorización, se conecta con proveedores de servicio para cotizar, crear, actualizar, cancelar y rastrear la solicitud.

La propuesta no es crear otra aplicación de transporte o delivery, sino ofrecer infraestructura y experiencia conversacional para que comercios, clínicas, hoteles, restaurantes y otras empresas coordinen múltiples proveedores desde una interfaz común.

## Contexto de mercado y diferenciación

- La categoría tecnológica general ya existe: iPaaS, middleware, ESB y automatización de flujos (por ejemplo, Zapier, Make, n8n y MuleSoft).
- También existe Mobility as a Service (MaaS), que integra planificación e información de distintos medios de transporte.
- La oportunidad a evaluar es una capa especializada para Latinoamérica, con lenguaje conversacional y un modelo operativo/comercial adaptado a movilidad, entregas y logística.
- No se ha identificado una plataforma regional consolidada que, de forma oficial, permita con una sola API crear y gestionar servicios entre Rappi, inDrive, DiDi, Uber y equivalentes.
- Las plataformas de comunicación sí cuentan con mecanismos oficiales de integración: WhatsApp Business Platform y Telegram Bot API.
- El mayor reto no es construir el bus técnico: es obtener APIs, permisos y acuerdos comerciales de los proveedores de movilidad y delivery. No se deben automatizar apps cerradas mediante simulación de interfaz, scraping o uso de cuentas de usuarios.
- Rappi es una empresa nacida en Colombia. inDrive opera fuertemente en Latinoamérica, pero no es una empresa latinoamericana.

## Enfoque inicial recomendado

1. Validar un nicho B2B concreto: clínicas, hoteles, restaurantes, comercios o empresas con mensajería recurrente.
2. Empezar con proveedores locales o APIs autorizadas y con enlaces profundos cuando no haya una API transaccional disponible.
3. Unificar el modelo de datos: solicitud, origen, destino, cotización, asignación, estado, cancelación, pago, comprobante e incidencias.
4. Diseñar conectores independientes por proveedor y una API canónica para los clientes del bus.
5. Obtener acuerdos comerciales antes de prometer reserva, cobro o rastreo dentro de plataformas externas.

## Instrucción obligatoria para agentes

Antes de analizar, diseñar, implementar o modificar este proyecto, leer y aplicar siempre estos dos archivos:

1. `.agents/skills/bmad-project-context/SKILL.md`
2. `.agents/skills/bmad-project-context/references/template.md`

Estas referencias forman parte del contexto obligatorio del proyecto y deben permanecer incluidas en este archivo.
