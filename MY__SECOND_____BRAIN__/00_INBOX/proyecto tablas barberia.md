
# REQUISITOS FUNCIONALES TABLA IMPROVISADA 

### Tabla 1: Especificación de Requisitos Funcionales (RF)

**Estructura optimizada: agrupada por módulos de negocio para facilitar la trazabilidad y el diseño de la base de datosS**

| **Código** | **Módulo**          | **Nombre del Requisito Funcional**     | **Descripción Breve**                                                    | **Prioridad** | **Rol Autorizado**      |
| ---------- | ------------------- | -------------------------------------- | ------------------------------------------------------------------------ | ------------- | ----------------------- |
| **RF-001** | Usuarios / Auth     | Iniciar Sesión                         | Autenticación de usuarios mediante credenciales en el sistema.           | Alta          | Todos los roles         |
| **RF-002** | Usuarios / Auth     | Cerrar Sesión                          | Finalización segura de la sesión activa del usuario.                     | Alta          | Todos los roles         |
| **RF-003** | Usuarios / Auth     | Recuperar Contraseña                   | Restablecimiento de credenciales vía token o correo electrónico.         | Media         | Todos los roles         |
| **RF-004** | Usuarios / Clientes | Autorregistro de Cliente               | Registro público para nuevos clientes en la plataforma.                  | Alta          | Cliente (público)       |
| **RF-005** | Usuarios / Auth     | Registrar Usuario Interno              | Creación de cuentas para personal administrativo o barberos.             | Alta          | Administrador           |
| **RF-006** | Usuarios / Auth     | Consultar / Listar Usuarios            | Visualización y filtrado de la base de datos de usuarios.                | Media         | Administrador           |
| **RF-007** | Usuarios / Auth     | Editar Perfil de Usuario               | Actualización de datos personales y de contacto propios.                 | Media         | Usuario autenticado     |
| **RF-008** | Usuarios / Auth     | Desactivar Usuario                     | Suspensión lógica de cuentas sin eliminar el historial.                  | Baja          | Administrador           |
| **RF-009** | Clientes            | Registrar Historial del Cliente        | Registro de notas, preferencias o alergias del cliente.                  | Media         | Admin, barbero          |
| **RF-010** | Clientes            | Consultar Historial de Cliente         | Consulta de visitas anteriores y preferencias del cliente.               | Media         | Admin, cliente, barbero |
| **RF-011** | Barberos y Horarios | Registrar Barbero                      | Alta de un nuevo barbero en el sistema operativo.                        | Alta          | Administrador           |
| **RF-012** | Barberos y Horarios | Configurar Horario y Disponibilidad    | Definición de turnos, días laborales y descansos.                        | Alta          | Administrador, barbero  |
| **RF-013** | Catálogo            | Registrar Servicio de Barbería         | Creación de nuevos servicios (corte, barba, etc.) con precio y duración. | Alta          | Administrador           |
| **RF-014** | Catálogo            | Listar / Consultar Servicios           | Visualización de la oferta de servicios disponibles.                     | Alta          | Todos los roles         |
| **RF-015** | Catálogo            | Editar Servicio de Barbería            | Modificación de precios, nombres o tiempos de los servicios.             | Media         | Administrador           |
| **RF-016** | Citas               | Agendamiento de Cita                   | Reserva de espacio temporal asignando servicio y barbero.                | Alta          | Cliente, Administrador  |
| **RF-017** | Citas               | Consultar Disponibilidad de Agenda     | Visualización en tiempo real de espacios libres por barbero.             | Alta          | Todos los roles         |
| **RF-018** | Citas               | Reagendar / Editar Cita                | Modificación de fecha, hora o barbero de una cita existente.             | Media         | Cliente, Administrador  |
| **RF-019** | Citas               | Cancelar Cita                          | Liberación anticipada de un turno reservado.                             | Media         | Cliente, Administrador  |
| **RF-020** | Citas               | Confirmar Asistencia / Finalizar Cita  | Control de estado del turno (asistido, en proceso, completado).          | Alta          | Barbero, Administrador  |
| **RF-021** | Citas               | Listar Citas por Barbero y Día         | Agenda diaria operativa individualizada por profesional.                 | Alta          | Barbero, Administrador  |
| **RF-022** | Inventario          | Registrar Producto de Venta            | Alta de artículos para comercialización (ceras, champús, etc.).          | Alta          | Administrador           |
| **RF-023** | Inventario          | Registrar Insumo Operativo             | Alta de insumos de uso interno en la barbería.                           | Alta          | Administrador           |
| **RF-024** | Inventario          | Control de Stock y Semáforo Mínimo     | Alertas automáticas por stock bajo de productos o insumos.               | Alta          | Administrador           |
| **RF-025** | Inventario          | Registrar Entrada / Compra             | Ingreso de stock por reabastecimiento de proveedores.                    | Alta          | Administrador           |
| **RF-026** | Ventas y Reportes   | Registrar Venta de Producto / Servicio | Facturación y cobro de servicios prestados o productos vendidos.         | Alta          | Admin, barbero          |
| **RF-027** | Ventas y Reportes   | Consultar / Listar Ventas              | Historial de transacciones y transacciones ejecutadas.                   | Alta          | Administrador           |
| **RF-028** | Ventas y Reportes   | Anular Venta                           | Reversión de una factura por error operativo o devolución.               | Baja          | Administrador           |
| **RF-029** | Inventario / Ventas | Descontar Insumo Automático            | Reducción automática de stock tras ejecutar un servicio o venta.         | Alta          | Sistema (Automático)    |
| **RF-030** | Ventas y Reportes   | Generar Reporte Gráfico de Ventas      | Estadísticas visuales de rendimiento financiero y comercial.             | Media         | Administrador           |
| **RF-031** | Ventas y Reportes   | Generar Comprobante de Venta           | Emisión de tiquete o factura física/digital para el cliente.             | Alta          | Admin, barbero          |
| **RF-032** | Ventas y Reportes   | Generar Reporte Neto / Balance         | Cálculo de ingresos, egresos y balance general del negocio.              | Alta          | Administrador           |


---
# Estrategia de requisitos 

### Tabla 2: Matriz de Estrategia de Requisitos y Planificación (Product Backlog por Sprints)

_Estructura optimizada: Vincula la gestión temporal (Sprints), los Casos de Uso (CU), los canales de acceso (Web/Móvil) y los roles operativos._

| Fase / Sprint | Código CU | Caso de Uso / Requisito Asociado       | Módulo              | Admin | Barbero / Vendedor | Cliente | Web | Móvil | Fechas Estimadas        | Responsable          |
| ------------- | --------- | -------------------------------------- | ------------------- | ----- | ------------------ | ------- | --- | ----- | ----------------------- | -------------------- |
| **Sprint 0**  | CU-001    | Iniciar Sesión                         | Usuarios / Auth     | ✔     | ✔                  | ✔       | ✔   | ✔     | 14/09/2026 - 22/09/2026 | Equipo de Desarrollo |
| **Sprint 0**  | CU-002    | Cerrar Sesión                          | Usuarios / Auth     | ✔     | ✔                  | ✔       | ✔   | ✔     | 14/09/2026 - 22/09/2026 | Equipo de Desarrollo |
| **Sprint 0**  | CU-003    | Recuperar Contraseña                   | Usuarios / Auth     | ✔     | ✔                  | ✔       | ✔   | ✔     | 14/09/2026 - 22/09/2026 | Equipo de Desarrollo |
| **Sprint 0**  | CU-004    | Autorregistro de Cliente               | Clientes            | ⎕     | ⎕                  | ✔       | ✔   | ✔     | 14/09/2026 - 22/09/2026 | Equipo de Desarrollo |
| **Sprint 1**  | CU-005    | Registrar Usuario Interno              | Usuarios / Auth     | ✔     | ⎕                  | ⎕       | ✔   | ✔     | 22/09/2026 - 30/09/2026 | Equipo de Desarrollo |
| **Sprint 1**  | CU-006    | Listar / Consultar Usuarios            | Usuarios / Auth     | ✔     | ⎕                  | ⎕       | ✔   | ✔     | 22/09/2026 - 30/09/2026 | Equipo de Desarrollo |
| **Sprint 1**  | CU-011    | Registrar Barbero                      | Barberos            | ✔     | ⎕                  | ⎕       | ✔   | ⎕     | 22/09/2026 - 30/09/2026 | Equipo de Desarrollo |
| **Sprint 1**  | CU-013    | Registrar Servicio de Barbería         | Catálogo            | ✔     | ⎕                  | ⎕       | ✔   | ⎕     | 22/09/2026 - 30/09/2026 | Equipo de Desarrollo |
| **Sprint 2**  | CU-016    | Agendar Cita                           | Citas               | ✔     | ⎕                  | ✔       | ✔   | ✔     | 01/10/2026 - 15/10/2026 | Equipo de Desarrollo |
| **Sprint 2**  | CU-017    | Consultar Disponibilidad de Agenda     | Citas               | ✔     | ✔                  | ✔       | ✔   | ✔     | 01/10/2026 - 15/10/2026 | Equipo de Desarrollo |
| **Sprint 2**  | CU-020    | Confirmar Asistencia / Finalizar Cita  | Citas               | ✔     | ✔                  | ⎕       | ✔   | ✔     | 01/10/2026 - 15/10/2026 | Equipo de Desarrollo |
| **Sprint 3**  | CU-022    | Registrar Producto de Venta            | Inventario          | ✔     | ⎕                  | ⎕       | ✔   | ⎕     | 16/10/2026 - 30/10/2026 | Equipo de Desarrollo |
| **Sprint 3**  | CU-026    | Registrar Venta de Producto / Servicio | Ventas              | ✔     | ✔                  | ⎕       | ✔   | ⎕     | 16/10/2026 - 30/10/2026 | Equipo de Desarrollo |
| **Sprint 3**  | CU-029    | Descontar Insumo por Servicio          | Inventario / Ventas | ⎕     | ⎕                  | ⎕       | ✔   | ⎕     | 16/10/2026 - 30/10/2026 | Equipo de Desarrollo |
| **Sprint 4**  | CU-030    | Generar Reporte Gráfico de Ventas      | Ventas / Reportes   | ✔     | ⎕                  | ⎕       | ✔   | ⎕     | 01/11/2026 - 15/11/2026 | Equipo de Desarrollo |
| **Sprint 4**  | CU-032    | Generar Reporte Neto / Balance         | Ventas / Reportes   | ✔     | ⎕                  | ⎕       | ✔   | ⎕     | 01/11/2026 - 15/11/2026 | Equipo de Desarrollo |


---
# NEW TABLE 


| **Código** | **Modulo**                 | **Nombre Del Requisito Funcional**     | **Descripción Breve**                                                                                                                                                  | **Prioridad** | **Rol Autorizado**      |
| ---------- | -------------------------- | -------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- | ----------------------- |
| RF-001     | Usuarios/autenticación     | Iniciar Sesión                         | Autentica al usuario con email y contraseña, validando credenciales contra el hash bcrypt y redirigiendo según su rol.                                                 | Alta          | Todos los roles         |
| RF-002     | Usuarios/autenticación     | Cerrar Sesión                          | Destruye la sesión activa o token del usuario y bloquea el acceso a rutas privadas mediante el botón atrás del navegador.                                              | Alta          | Todos los roles         |
| RF-003     | Usuarios/autenticación<br> | Recuperar contraseña                   | Permite restablecer la clave enviando un enlace o código temporal de verificación al correo registrado.                                                                | Media         | Todos los roles<br>     |
| RF-004     | Usuarios/autenticación     | Autorregistro de Cliente               | Permite a un cliente nuevo crear su cuenta con nombre  , email único, teléfono y contraseña, asignándole rol **CLIENTE** por defecto.                                  | Alta          | Cliente (publico)       |
| RF-005     | Usuarios/autenticación     | Registrar Usuario Interno              | Permite al Administrador crear cuentas con rol **BARBERO o ADMINISTRADOR**  y definir sus datos básicos.                                                               | Alta          | Administrador           |
| RF-006     | Usuarios/autenticación     | Consultar / Listar Usuarios            | Muestra al Administrador el listado de usuarios con filtros de búsqueda por nombre, rol y estado (`ACTIVO`/`INACTIVO`)                                                 | Media         | Administrador           |
| RF-007     | Usuarios/autenticación     | Editar Perfil de Usuario               | Permite a cualquier usuario autenticado actualizar su teléfono, nombre o contraseña sin alterar su rol asignado.                                                       | Media         | Usuario autenticado     |
| RF-008     | Usuarios/autenticación     | Desactivar Usuario                     | Cambia el estado de un usuario a**INACTIVO** (borrado lógico) para impedir su acceso sin perder  el historial de sus citas o ventas .                                  | Baja          | Administrador           |
| RF-009     | Clientes                   | Registrar Notas Técnicas del Cliente   | Permite al barbero o administrador guardar observaciones del servicio (ej. tipo de corte o alergias) asociadas a la cita                                               | Media         | Admin, barbero          |
| RF-010     | Clientes                   | Consultar Historial de Cliente         | Lista cronológicamente los servicios realizados, barberos que lo atendieron, fechas y notas técnicas de un cliente.                                                    | Alta          | Admin, cliente, barbero |
| RF-011     | Barberos y Horarios        | Registrar Barbero                      | Asocia un usuario con rol **BARBERO**  a su perfil laboral registrando su especialidad y fecha de ingreso a la barbería.                                               | Alta          | Administrador           |
| RF-012     | Barberos y Horarios        | Configurar Horario y Disponibilidad    | Permite definir los días de la semana y bloques de horas laborables del barbero para no cruzar citas con sus estudios.                                                 | Alta          | Administrador y Barbero |
| RF-013     | Catálogo                   | Registrar Servicio de Barbería         | Crea un servicio con nombre, precio base, duración en minutos y su receta de insumos asociados para el descuento automático.                                           | Alta          | Administrador           |
| RF-014     | Catálogo                   | <br>Listar / Consultar Servicios<br>   | Muestra el catálogo de servicios activos con sus precios y tiempos estimados de duración para todos los roles.                                                         | Alta          | Todos los roles         |
| RF-015     | Catálogo                   | Editar Servicio de Barbería            | Permite al Administrador actualizar el precio, duración, receta de insumos o cambiar el estado (**ACTIVO/INACTIVO**) de un servicio.                                   | Media         | Administrador           |
| RF-016     | Citas                      | Agendar cita                           | Registra una cita validando que el barbero tenga turno activo (RF-012) y que el rango entre hora de inicio y fin no choque con otra cita.                              | Alta          | Cliente , administrador |
| RF-017     | Citas                      | Consultar Disponibilidad de Agenda<br> | Calcula y muestra los bloques de horario libres de un barbero en una fecha específica cruzando su turno contra las citas activas.                                      | Alta          | Todos los roles         |
| RF-018     | Citas                      | Reagendar / Editar Cita                | Modifica la fecha, hora o barbero de una cita pendiente o confirmada, ejecutando de nuevo la validación de disponibilidad.                                             | Media         | Cliente , administrador |
| RF-019     | Citas                      | cancelar cita                          | Cambia el estado de una cita a **CANCELADA**, liberando inmediatamente ese bloque de tiempo en la agenda del barbero.                                                  | Media         | Cliente , administrador |
| RF-020     | Citas                      | Confirmar Asistencia / Finalizar Cita  | <br>Cambia el estado de la cita a **FINALIZADA** tras atender al cliente y dispara el descuento automático de insumos (RF-029).<br>                                    | Alta          | Barbero, administrador  |
| RF-021     | Citas                      | Listar Citas por Barbero y Día         | Filtra y ordena cronológicamente la agenda del día para que el barbero o administrador controle los turnos de atención.                                                | Alta          | Barbero y administrador |
| RF-022     | Inventario                 | Registrar Producto de Venta            | Crea artículos comerciales con precio de costo, precio de venta y umbral de stock mínimo.                                                                              | Alta          | Administrador           |
| RF-023     | Inventario                 | Registrar Insumo Operativo             | Registra materiales de trabajo interno definiendo su unidad de medida (unidad, gramo o mililitro).                                                                     | Alta          | Administrador           |
| RF-024     | Inventario                 | Control de Stock y Semáforo Mínimo     | Alerta visualmente en **ROJO** cuando el stock actual de un ítem iguala o baja de su stock mínimo.                                                                     | Alta          | Administrador           |
| RF-025     | Inventario                 | Registrar Entrada / Compra             | Incrementa el stock de un producto o insumo registrando la cantidad comprada y su costo unitario.                                                                      | Alta          | Administrador           |
| RF-026     | Ventas y Reportes          | Registrar Venta de Producto / Servicio | Procesa el cobro de una cita o producto, registrando el método de pago y el responsable.                                                                               | Alta          | Administrador , Barbero |
| RF-027     | Ventas y Reportes<br>      | Consultar / Listar Ventas              | Muestra el historial de ventas filtrando por rango de fechas, barbero, método de pago y estado.                                                                        | Alta          | Administrador           |
| RF-028     | Ventas y Reportes<br>      | Anular Venta                           | Cambia el estado de una venta a **ANULADA**, revierte el stock descontado y guarda el evento en auditoría.                                                             | Baja          | Administrador           |
| RF-029     | Ventas y Reportes<br>      | Descontar Insumo Automático            | Resta automáticamente del inventario las cantidades de insumos de la receta al finalizar una cita (RF-020)  o registrar un servicio por venta directa        (RF-033). | Alta          | Sistema                 |
| RF-030     | Ventas y Reportes<br>      | Generar Reporte Gráfico de Ventas      | Visualiza en gráficas el volumen de ingresos por periodo, servicios más vendidos y rendimiento                                                                         | Media         | Administrador           |
| RF-031     | Ventas y Reportes<br>      | Generar Comprobante de Venta<br><br>   | Genera un recibo digital en PDF o vista rápida con el detalle de cobro sin requerir impresora.                                                                         | Alta          | Administrador , Barbero |
| RF-032     | Ventas y Reportes<br>      | Generar Reporte Neto / Balance         | Calcula la ganancia neta cruzando el total de ventas completadas contra el costo de compras e insumos                                                                  | Alta          | Administrador           |
| RF-033     | Ventas y reportes          | Registro de venta directa              | Registra un servicio o venta de mostrador al instante sin exigir una cita agendada previamente                                                                         | Alta          | Administrador , barbero |

---
# ESTRATEGIA DE REQUISITOS 

| Fase / Sprint  | Código CU | Caso de Uso / Requisito Asociado  | Módulo              | Admin | Barbero / Vendedor | Cliente | Web | Móvil | Fechas Estimadas        | Responsable          |
| -------------- | --------- | --------------------------------- | ------------------- | ----- | ------------------ | ------- | --- | ----- | ----------------------- | -------------------- |
| **Sprint 0**   | CU-001    | Iniciar Sesión                    | Usuarios / Auth     | 1     | 1                  | 1       | 1   | 1     | 14/09/2026 - 22/09/2026 | Equipo de desarrollo |
| **Sprint 0**   | CU-002    | Cerrar Sesión                     | Usuarios / Auth     | 1     | 1                  | 1       | 1   | 1     | 14/09/2026 - 22/09/2026 | Equipo de Desarrollo |
| **Sprint 0**   | CU-003    | Recuperar Contraseña              | Usuarios / Auth     | 1     | 1                  | 1       | 1   | 1     | 14/09/2026 - 22/09/2026 | Equipo de Desarrollo |
| **Sprint 0**   | CU-004    | Autorregistro de Cliente          | Clientes            | 0     | 0                  | 1       | 1   | 1     | 14/09/2026 - 22/09/2026 | Equipo de Desarrollo |
| **Sprint 1**   | CU-005    | Registrar Usuario Interno         | Usuarios / Auth     | 1     | 0                  | 0       | 1   | 1     | 22/09/2026 - 30/09/2026 | Equipo de Desarrollo |
| **Sprint 1**   | CU-006    | Listar / Consultar Usuarios       | Usuarios / Auth     | 1     | 0                  | 0       | 1   | 1     | 22/09/2026 - 30/09/2026 | Equipo de Desarrollo |
| **Sprint 1**   | CU-007    | Editar Perfil de Usuario          | Usuarios / Auth     |       | ⎕                  | ⎕       | ✔   | ⎕     | 22/09/2026 - 30/09/2026 | Equipo de Desarrollo |
| **Sprint 1**   | CU-008    |                                   |                     | ✔     | ⎕                  | ⎕       | ✔   | ⎕     | 22/09/2026 - 30/09/2026 | Equipo de Desarrollo |
| **sprint 1**   | CU-011    |                                   |                     | ✔     | ⎕                  | ✔       | ✔   | ✔     | 01/10/2026 - 15/10/2026 | Equipo de Desarrollo |
| **sprint 1**   | CU-012    |                                   |                     | ✔     | ✔                  | ✔       | ✔   | ✔     | 01/10/2026 - 15/10/2026 | Equipo de Desarrollo |
| **sprint 1\|** | CU-013    |                                   |                     | ✔     | ✔                  | ⎕       | ✔   | ✔     | 01/10/2026 - 15/10/2026 | Equipo de Desarrollo |
| **sprint 1**   | CU-014    |                                   |                     | ✔     | ⎕                  | ⎕       | ✔   | ⎕     | 16/10/2026 - 30/10/2026 | Equipo de Desarrollo |
| **sprint 1**   | CU-015    |                                   |                     | ✔     | ✔                  | ⎕       | ✔   | ⎕     | 16/10/2026 - 30/10/2026 | Equipo de Desarrollo |
| ****           |           | Descontar Insumo por Servicio     | Inventario / Ventas | ⎕     | ⎕                  | ⎕       | ✔   | ⎕     | 16/10/2026 - 30/10/2026 | Equipo de Desarrollo |
| ****           |           | Generar Reporte Gráfico de Ventas | Ventas / Reportes   | ✔     | ⎕                  | ⎕       | ✔   | ⎕     | 01/11/2026 - 15/11/2026 | Equipo de Desarrollo |
| ****           |           | Generar Reporte Neto / Balance    | Ventas / Reportes   | ✔     | ⎕                  | ⎕       | ✔   | ⎕     | 01/11/2026 - 15/11/2026 | Equipo de Desarrollo |
| ****           |           |                                   |                     |       |                    |         |     |       |                         |                      |

