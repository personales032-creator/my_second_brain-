Para que un software quede profesional de principio a fin —especialmente si te lo van a calificar en el SENA o la EAN, o si buscas estándar de industria—, la documentación se divide en fases cronológicas.

Usaremos como **ejemplo un Supermercado** (módulo de inventario, caja/ventas, clientes y cajeros) para que veas exactamente qué documento va en cada momento.

### Fase 1: Inicio y Planificación (El "Por qué" y "Cuándo")

Aquí defines de qué trata el proyecto y cómo te vas a organizar temporalmente.

- **Acta de Constitución del Proyecto (Project Charter):** Nombre del proyecto (ej: _SuperMarket POS_), objetivo general, justificación y alcance.
    
- **Cronograma o Matriz de Sprints:** La tabla que armamos antes con fechas, entregables y responsables (Sprint 0, Sprint 1, etc.).
    

### Fase 2: Análisis y Requisitos (El "Qué" del sistema)

Aquí pones por escrito lo que el software tiene prohibido fallar y lo que debe hacer.

- **Requisitos Funcionales (RF):** La lista limpia de acciones (ej: _RF-001: Registrar venta de productos por código de barras_).
    
- **Requisitos No Funcionales (RNF):** Restricciones técnicas o de rendimiento (ej: _RNF-01: El sistema debe procesar el pago en menos de 2 segundos; RNF-02: Las contraseñas deben estar encriptadas con BCrypt_).
    
- **Casos de Uso (CU):** La lista o diagramas que muestran quién interactúa con qué (ej: _El Cajero genera una factura_).
    

### Fase 3: Diseño de Base de Datos y Arquitectura (El Backend)

Aquí diseñas la estructura técnica antes de escribir una sola línea de código en DBeaver o Postgres.

- **Diagrama Entidad-Relación (DER):** El mapa de tus tablas en la base de datos.
    
    - _Ejemplo Supermercado:_ Tablas `Cliente`, `Producto`, `Categoria`, `Venta`, `Detalle_Venta` y `Cajero`.
        
- **Diccionario de Datos:** Una tabla que describe cada columna de tu base de datos (nombre del campo, tipo de dato `VARCHAR`, `INT`, `UUID`, si es llave primaria `PK` o foránea `FK`).
    
- **Diagrama de Arquitectura:** Un esquema simple de cómo se comunican las capas:
    
    - _Frontend (React/Móvil)_ →\rightarrow→ _API REST (Spring Boot / Python)_ →\rightarrow→ _Base de Datos (PostgreSQL)_.
        

### Fase 4: Diseño Visual e Interfaces (El Frontend)

- **Wireframes o Mockups de Baja/Alta Fidelidad:** Bocetos o diseños en Figma de cómo se verá la pantalla de la caja registradora, el catálogo de productos y el inicio de sesión del cajero.
    
- **Flujo de Usuario (User Journey):** Cómo navega el cajero desde que entra a la app hasta que imprime el recibo.
    

### Fase 5: Desarrollo y Documentación de APIs (Integración)

Cuando estás programando el backend y el frontend, necesitas documentar cómo se hablan.

- **Documentación de Endpoints (API Docs):** Una lista de tus rutas HTTP (usando herramientas como Swagger o Postman):
    
    - `POST /api/v1/productos` (Crear producto en inventario)
        
    - `GET /api/v1/ventas/{id}` (Consultar factura de venta)
        
- **Guía de Configuración (README.md):** Instrucciones técnicas para levantar el proyecto en otro computador (ej: _"1. Clonar repositorio, 2. Ejecutar docker-compose up, 3. Configurar variables de entorno en archivo .env"_).
    

### Fase 6: Pruebas y Cierre (Calidad y Manuales)

- **Casos de Prueba (Test Cases):** Tabla para comprobar que lo que hiciste funciona (ej: _Prueba #1: Intentar vender un producto con stock en 0 →\rightarrow→ Resultado esperado: Bloquear la venta y mostrar alerta_).
    
- **Manual de Usuario:** Una guía visual paso a paso con capturas de pantalla dirigida al usuario final (el cajero o el administrador del supermercado) sobre cómo usar el software.
    
- **Manual Técnico:** Documentación para futuros desarrolladores sobre la estructura del código backend y frontend.