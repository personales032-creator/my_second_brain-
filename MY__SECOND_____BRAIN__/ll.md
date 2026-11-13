
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
| **RF-014** | Catálogo            | Listar / Consultar Servicios<br>       | Visualización de la oferta de servicios disponibles.                     | Alta          | Todos los roles         |
| **RF-015** | Catálogo            | Editar Servicio de Barbería            | Modificación de precios, nombres o tiempos de los servicios.             | Media         | Administrador           |
| **RF-016** | Citas               | Agendamiento de Cita                   | Reserva de espacio temporal asignando servicio y barbero.                | Alta          | Cliente, Administrador  |
| **RF-017** | Citas               | Consultar Disponibilidad de Agenda     | Visualización en tiempo real de espacios libres por barbero.             | Alta          | Todos los roles         |
| **RF-018** | Citas               | Reagendar / Editar Cita                | Modificación de fecha, hora o barbero de una cita existente.             | Media         | Cliente, Administrador  |
| **RF-019** | Citas               | cancelar cita                          | Liberación anticipada de un turno reservado.                             | Media         | Cliente, Administrador  |
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
