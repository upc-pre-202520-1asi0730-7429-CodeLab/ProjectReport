# Capítulo III: Requirements Specification

## 3.1. To-Be Scenario Mapping

El mapeo de escenarios "To-Be" nos permite visualizar cómo será el proceso o flujo de trabajo deseado en el futuro después de implementar las mejoras propuestas. Nos ayuda a identificar los cambios necesarios en los procesos actuales y a diseñar soluciones para optimizarlos. Al crear escenarios "To-Be", podemos visualizar claramente cómo se verá el proceso una vez que se implementen las mejoras, lo que nos permite comunicar mejor la visión del proyecto y alinear a todas las partes interesadas en torno a los objetivos comunes. Esto facilita la planificación y la implementación efectiva de los cambios para lograr los resultados deseados.

#### Segmento Objetivo: Administrador/a

</strong><img src="images/tobeP.jpg">


#### Segmento Objetivo: Húesped

</strong><img src="images/tobeH.jpg">

## 3.2. User Stories

### EPICS

| Epic ID | Título                     | Descripción                                                                                                                                                     |
|---------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EP01    | Gestión de Reservas         | Como administrador de un hostal quiero gestionar todo el ciclo de reservas (búsqueda, creación, cambios y cancelaciones) para que se reduzcan errores y se optimice la ocupación de habitaciones. |
| EP02    | Operación de Huéspedes      | Como administrador quiero controlar check-in, check-out y el historial de cada huésped para que pueda ofrecer un servicio rápido y personalizado.              |
| EP03    | Servicios y Experiencia     | Como huésped quiero solicitar y pagar servicios adicionales en tiempo real para que mi estadía sea más cómoda y completa.                                      |
| EP04    | Administración financiera   | Como administrador quiero registrar pagos, generar facturas y obtener reportes para que pueda llevar un control financiero confiable del negocio.              |
| EP05    | Plataforma y Acceso Seguro  | Como usuario (administrador) quiero autenticarme y acceder desde cualquier dispositivo para que mis datos estén protegidos y pueda operar en todo momento.     |
| EP06    | Marketing y Capacitación    | Como visitante o potencial cliente quiero conocer la propuesta de valor, planes y testimonios en una landing page para que pueda decidir registrarme o solicitar más información. |
| EP07    | API Pública e Integraciones | Como desarrollador externo quiero consumir una API RESTful de reservas, pagos y usuarios para que pueda integrar Hostel Manager con otros sistemas o aplicaciones. |



### User stories

| ID   | Título                        | Descripción                                                                                       | Criterios de Aceptación                                                                                                                                                                                                 | Epic  |
|------|-------------------------------|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| US01 | Buscar disponibilidad         | Como huésped quiero consultar habitaciones libres por fecha para poder planificar mi viaje.       | **Escenario 1: Búsqueda exitosa**<br>Dado que el huésped ingresa fechas válidas, cuando solicita disponibilidad, entonces el sistema muestra habitaciones y tarifas.<br>**Escenario 2: Fechas inválidas**<br>Dado que el huésped ingresa un rango invertido, cuando solicita disponibilidad, entonces el sistema informa “Fechas no válidas”. | EP01  |
| US02 | Crear reserva                 | Como administrador quiero registrar una reserva con datos de huésped y habitación para que se asegure la disponibilidad. | **Escenario 1: Reserva confirmada**<br>Dado que ingresa datos válidos, cuando confirma, entonces el sistema guarda la reserva y confirma.<br>**Escenario 2: Reserva fallida**<br>Dado que la habitación está ocupada, cuando intenta reservar, entonces el sistema muestra “No disponible”. | EP01  |
| US03 | Modificar reserva             | Como administrador quiero actualizar las fechas o datos de una reserva para que la información esté siempre correcta. | **Escenario 1: Actualización exitosa**<br>Dado que la reserva está activa, cuando modifica fechas, entonces el sistema valida y guarda cambios.<br>**Escenario 2: Actualización fallida**<br>Dado que las nuevas fechas se superponen, cuando guarda, entonces el sistema muestra “Conflicto de fechas”. | EP01  |
| US04 | Cancelar reserva              | Como administrador quiero cancelar reservas confirmadas para que pueda liberar la habitación.      | **Escenario 1: Cancelar reserva**<br>Dado que selecciona una reserva activa, cuando confirma, entonces el sistema marca la reserva como cancelada.<br>**Escenario 2: Reserva ya cancelada**<br>Dado que la reserva ya está cancelada, cuando intenta cancelarla, entonces el sistema indica “Reserva ya cancelada”. | EP01  |
| US05 | Reserva en línea              | Como huésped quiero crear y pagar una reserva desde mi dispositivo para que tenga confirmación inmediata. | **Escenario 1: Confirmación**<br>Dado que ingresa datos válidos y método de pago, cuando confirma, entonces el sistema registra la reserva y envía confirmación.<br>**Escenario 2: Pago rechazado**<br>Dado que el pago falla, cuando intenta reservar, entonces el sistema notifica “Transacción no completada”. | EP01  |
| US06 | Confirmación por correo       | Como huésped quiero recibir un email con los detalles de la reserva para que pueda comprobarla en cualquier momento. | **Escenario 1: Éxito**<br>Dado que la reserva es creada, cuando el sistema procesa, entonces envía correo de confirmación.<br>**Escenario 2: Correo inválido**<br>Dado que el correo del huésped es incorrecto, cuando se intenta enviar, entonces el sistema registra el error y alerta al administrador. | EP01  |
| US07 | Registrar huésped             | Como administrador quiero registrar la información de un nuevo huésped para que pueda mantener un historial de clientes. | **Escenario 1: Registro completo**<br>Dado que ingresa todos los datos requeridos, cuando guarda, entonces el sistema confirma “Huésped registrado”.<br>**Escenario 2: Datos incompletos**<br>Dado que falta información obligatoria, cuando se guarda, entonces el sistema muestra “Datos incompletos”. | EP02  |
| US08 | Actualizar datos de huésped   | Como administrador quiero editar información personal de un huésped para que los registros estén actualizados. | **Escenario 1: Cambios guardados**<br>Dado que el huésped existe, cuando modifica datos, entonces el sistema guarda los cambios.<br>**Escenario 2: No encontrado**<br>Dado que el ID no existe, cuando intenta modificar, entonces el sistema muestra “Huésped no encontrado”. | EP02  |
| US09 | Check-in digital              | Como administrador quiero registrar el check-in de un huésped para que el estado de la habitación se actualice en tiempo real. | **Escenario 1: Cambio de estado**<br>Dado que hay reserva confirmada, cuando registra check-in, entonces el sistema cambia estado a “Ocupado”.<br>**Escenario 2: Sin reserva**<br>Dado que no hay reserva, cuando intenta check-in, entonces el sistema muestra “Reserva no encontrada”. | EP02  |
| US10 | Check-out digital             | Como administrador quiero registrar la salida de un huésped para que la habitación quede disponible. | **Escenario 1: Check-in liberación**<br>Dado que la habitación está ocupada, cuando confirma check-out, entonces el sistema libera la habitación.<br>**Escenario 2: Sin check-in**<br>Dado que no se ha hecho check-in, cuando intenta check-out, entonces el sistema muestra “Check-in no registrado”. | EP02  |
| US11 | Consultar historial de huésped| Como administrador quiero revisar el historial de visitas de cada huésped para que pueda ofrecer un servicio personalizado. | **Escenario 1: Registro**<br>Dado que selecciona un huésped válido, cuando solicita historial, entonces el sistema muestra reservas previas.<br>**Escenario 2: Sin registro**<br>Dado que el huésped no tiene historial, cuando solicita, entonces el sistema muestra “Sin registros disponibles”. | EP02  |
| US12 | Registrar preferencias        | Como administrador quiero guardar preferencias especiales de cada huésped para que pueda personalizar futuras estadías. | **Escenario 1: Preferencias**<br>Dado que ingresa preferencias, cuando guarda, entonces el sistema las asocia al perfil.<br>**Escenario 2: Huésped inexistente**<br>Dado que el ID no existe, cuando guarda, entonces el sistema indica “Huésped no encontrado”. | EP02  |
| US13 | Crear servicio adicional      | Como administrador quiero definir servicios extras con precios para que pueda ofrecer más opciones de venta. | **Escenario 1: Registro servicio**<br>Dado que ingresa nombre y precio, cuando confirma, entonces el sistema lo registra.<br>**Escenario 2: Datos incompletos**<br>Dado que falta el precio, cuando se guarda, entonces el sistema muestra “Información incompleta”. | EP03  |
| US14 | Editar servicio adicional     | Como administrador quiero modificar o eliminar un servicio extra para que la oferta se mantenga actualizada. | **Escenario 1: Edición completada**<br>Dado que el servicio existe, cuando se actualiza o elimina, entonces el sistema guarda cambios.<br>**Escenario 2: No encontrado**<br>Dado que el ID no existe, cuando intenta modificar, entonces el sistema muestra “Servicio no encontrado”. | EP03  |
| US15 | Solicitar servicio en estadía | Como huésped quiero pedir un servicio extra en tiempo real para que mi experiencia sea más cómoda. | **Escenario 1: Servicio activo**<br>Dado que hay servicios activos, cuando selecciona uno, entonces el sistema registra la solicitud y notifica.<br>**Escenario 2: Servicio inactivo**<br>Dado que el servicio está deshabilitado, cuando intenta solicitar, entonces el sistema muestra “Servicio no disponible”. | EP03  |
| US16 | Pagar servicio adicional      | Como huésped quiero pagar los servicios consumidos para que pueda cerrar mi cuenta de manera rápida y segura. | **Escenario 1: Pago exitoso**<br>Dado que selecciona método de pago válido, cuando confirma, entonces el sistema procesa pago y emite comprobante.<br>**Escenario 2: Pago fallido**<br>Dado que el método es inválido, cuando confirma, entonces el sistema informa “Pago rechazado”. | EP03  |
| US17 | Registrar pago de reserva     | Como administrador quiero validar y registrar pagos recibidos para que el control financiero sea exacto. | **Escenario 1: Éxito**<br>Dado que ingresa datos correctos, cuando confirma, entonces el sistema registra el pago.<br>**Escenario 2: Datos incompletos**<br>Dado que falta monto, cuando confirma, entonces el sistema muestra “Información insuficiente”. | EP04  |
| US18 | Emisión de factura electrónica| Como administrador quiero generar comprobantes automáticos de pago para que cumpla con requisitos legales. | **Escenario 1: Éxito**<br>Dado que se registra un pago, cuando se procesa, entonces el sistema envía factura al correo.<br>**Escenario 2: Correo inválido**<br>Dado que el correo es incorrecto, cuando intenta enviar, entonces el sistema registra error y alerta al administrador. | EP04  |
| US19 | Reporte financiero por fechas | Como administrador quiero obtener reportes de ingresos y ocupación para que pueda analizar el desempeño del negocio. | **Escenario 1: Éxito**<br>Dado que selecciona rango válido, cuando solicita, entonces el sistema genera reporte con totales.<br>**Escenario 2: Rango inválido**<br>Dado que la fecha inicial es mayor a la final, cuando solicita, entonces el sistema muestra “Rango de fechas inválido”. | EP04  |
| US20 | Conciliación de pagos         | Como administrador quiero conciliar pagos con reservas para que se detecten discrepancias.         | **Escenario 1: Éxito**<br>Dado que existen transacciones, cuando solicita conciliación, entonces el sistema identifica coincidencias.<br>**Escenario 2: Sin transacciones**<br>Dado que no hay pagos, cuando solicita, entonces el sistema muestra “No hay datos para conciliar”. | EP04  |
| US21 | Autenticación segura          | Como usuario quiero iniciar sesión con credenciales protegidas para que mis datos permanezcan seguros. | **Escenario 1: Éxito**<br>Dado que las credenciales son válidas, cuando se envían, entonces el sistema concede acceso.<br>**Escenario 2: Credenciales inválidas**<br>Dado que la contraseña es incorrecta, cuando se envían, entonces el sistema responde “Usuario o contraseña incorrectos”. | EP05  |
| US22 | Recuperar contraseña          | Como usuario quiero restablecer mi contraseña olvidada para que pueda volver a acceder.            | **Escenario 1: Éxito**<br>Dado que ingresa correo registrado, cuando solicita recuperación, entonces el sistema envía enlace temporal.<br>**Escenario 2: Correo no registrado**<br>Dado que el correo no existe, cuando solicita, entonces el sistema muestra “Correo no encontrado”. | EP05  |
| US23 | Gestión de roles              | Como administrador quiero asignar roles con distintos permisos para que cada usuario tenga el acceso adecuado. | **Escenario 1: Éxito**<br>Dado que selecciona un usuario y rol, cuando guarda, entonces el sistema aplica permisos.<br>**Escenario 2: Rol inválido**<br>Dado que el rol no existe, cuando intenta asignarlo, entonces el sistema muestra “Rol no válido”. | EP05  |
| US24 | Acceso multicanal             | Como usuario quiero acceder desde web o móvil para que tenga flexibilidad de uso.                 | **Escenario 1: Éxito**<br>Dado que posee credenciales válidas, cuando inicia sesión desde cualquier dispositivo, entonces el sistema ofrece las mismas funciones.<br>**Escenario 2: Dispositivo no soportado**<br>Dado que el navegador no es compatible, cuando inicia sesión, entonces el sistema muestra “Dispositivo no soportado”. | EP05  |
| US25 | Información en landing page   | Como visitante quiero ver la propuesta de valor y testimonios para que pueda decidir si registrarme. | **Escenario 1: Éxito**<br>Dado que accede a la landing, cuando la página carga, entonces se muestran secciones informativas.<br>**Escenario 2: Error de carga**<br>Dado que el servidor está inactivo, cuando intenta acceder, entonces el sistema muestra mensaje de mantenimiento. | EP06  |
| US26 | Registro rápido desde landing | Como administrador interesado quiero crear una cuenta desde la landing para que pueda empezar a usar la plataforma de inmediato. | **Escenario 1: Éxito**<br>Dado que ingresa datos válidos, cuando envía el formulario, entonces el sistema crea la cuenta y envía confirmación.<br>**Escenario 2: Datos inválidos**<br>Dado que el correo no es válido, cuando envía, entonces el sistema muestra “Formato de correo inválido”. | EP06  |
| US27 | Formulario de contacto        | Como visitante quiero enviar una consulta o solicitud de demostración para que el equipo comercial me responda. | **Escenario 1: Éxito**<br>Dado que completa nombre, correo y mensaje, cuando envía, entonces el sistema confirma el envío y notifica al equipo.<br>**Escenario 2: Campos vacíos**<br>Dado que falta un campo obligatorio, cuando envía, entonces el sistema muestra “Complete todos los campos”. | EP06  |
| US28 | Visualizar planes y precios   | Como visitante quiero revisar planes de suscripción y costos para que pueda elegir el más adecuado. | **Escenario 1: Éxito**<br>Dado que accede a la sección de precios, cuando carga, entonces el sistema muestra planes actualizados.<br>**Escenario 2: Error de actualización**<br>Dado que ocurre fallo de datos, cuando carga, entonces el sistema muestra “Información no disponible temporalmente”. | EP06  |
| US29 | Endpoint de reservas          | Como desarrollador externo quiero crear reservas mediante un endpoint RESTful para que pueda integrar mi aplicación con el sistema. | **Escenario 1: Éxito**<br>Dado que el request contiene datos correctos, cuando se envía, entonces el sistema responde 201 con JSON de la reserva.<br>**Escenario 2: Datos incompletos**<br>Dado que falta un campo obligatorio, cuando se envía, entonces el sistema responde 400 con mensaje de error. | EP07  |
| US30 | Endpoint de pagos             | Como desarrollador externo quiero registrar pagos mediante un endpoint RESTful para que pueda sincronizar mis sistemas de cobro. | **Escenario 1: Éxito**<br>Dado que el request es válido, cuando se procesa, entonces el sistema responde 201 con confirmación de pago.<br>**Escenario 2: Rechazo de pasarela**<br>Dado que la pasarela rechaza el pago, cuando se procesa, entonces el sistema responde 402 con mensaje de rechazo. | EP07  |



## 3.3. Impact Mapping

En esta sección, aplicamos la técnica de Impact Mapping, una herramienta visual que ayuda a los equipos a definir y alinear las acciones con los objetivos estratégicos del proyecto.

</strong><img src="images/impaM.jpg">

## 3.4. Product Backlog

| #Orden | User Story ID | Título                     | Descripción (resumen)                                                             | Story Points |
|--------|---------------|----------------------------|-----------------------------------------------------------------------------------|--------------|
| 1      | US01          | Buscar disponibilidad      | Como huésped quiero consultar habitaciones libres para planificar mi viaje.       | 5            |
| 2      | US02          | Crear reserva              | Como administrador quiero registrar una reserva para asegurar disponibilidad.      | 8            |
| 3      | US05          | Reserva en línea           | Como huésped quiero reservar y pagar en línea para obtener confirmación inmediata. | 8            |
| 4      | US03          | Modificar reserva          | Como administrador quiero actualizar fechas o datos de una reserva.                | 5            |
| 5      | US04          | Cancelar reserva           | Como administrador quiero cancelar reservas confirmadas.                           | 3            |
| 6      | US06          | Confirmación por correo    | Como huésped quiero recibir un email con los detalles de la reserva.              | 3            |
| 7      | US09          | Check-in digital           | Como administrador quiero registrar el check-in para actualizar ocupación en tiempo real. | 5      |
| 8      | US10          | Check-out digital          | Como administrador quiero registrar la salida de un huésped.                       | 3            |
| 9      | US07          | Registrar huésped          | Como administrador quiero registrar la información de un nuevo huésped.            | 3            |
| 10     | US08          | Actualizar datos de huésped| Como administrador quiero editar información personal de un huésped.              | 3            |
| 11     | US11          | Consultar historial        | Como administrador quiero revisar el historial de visitas.                         | 3            |
| 12     | US12          | Registrar preferencias     | Como administrador quiero guardar preferencias del huésped.                        | 3            |
| 13     | US13          | Crear servicio adicional   | Como administrador quiero definir servicios extras.                                | 5            |
| 14     | US15          | Solicitar servicio en estadía | Como huésped quiero pedir un servicio extra en tiempo real.                     | 5            |
| 15     | US16          | Pagar servicio adicional   | Como huésped quiero pagar los servicios consumidos.                                | 5            |
| 16     | US14          | Editar servicio adicional  | Como administrador quiero modificar o eliminar un servicio extra.                  | 3            |
| 17     | US17          | Registrar pago de reserva  | Como administrador quiero validar y registrar pagos recibidos.                     | 5            |
| 18     | US18          | Emisión de factura         | Como administrador quiero generar comprobantes automáticos de pago.                | 5            |
| 19     | US19          | Reporte financiero         | Como administrador quiero obtener reportes de ingresos y ocupación.                | 5            |
| 20     | US20          | Conciliación de pagos      | Como administrador quiero conciliar pagos con reservas.                            | 3            |
| 21     | US25          | Información en landing page| Como visitante quiero ver la propuesta de valor y testimonios.                     | 3            |
| 22     | US26          | Registro rápido en landing | Como administrador interesado quiero crear una cuenta desde la landing.            | 5            |
| 23     | US27          | Formulario de contacto     | Como visitante quiero enviar una consulta o solicitud de demostración.             | 3            |
| 24     | US28          | Visualizar planes y precios| Como visitante quiero revisar planes de suscripción y costos.                      | 3            |
| 25     | US21          | Autenticación segura       | Como usuario quiero iniciar sesión con credenciales protegidas.                    | 5            |
| 26     | US22          | Recuperar contraseña       | Como usuario quiero restablecer mi contraseña olvidada.                            | 3            |
| 27     | US23          | Gestión de roles           | Como administrador quiero asignar roles con distintos permisos.                    | 5            |
| 28     | US24          | Acceso multicanal          | Como usuario quiero acceder desde web o móvil.                                     | 3            |
| 29     | US29          | Endpoint de reservas       | Como desarrollador externo quiero crear reservas mediante un endpoint RESTful.     | 8            |
| 30     | US30          | Endpoint de pagos          | Como desarrollador externo quiero registrar pagos mediante un endpoint RESTful.    | 8            |




