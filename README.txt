Sistema de Gestión de Libros

Sistema de escritorio para administrar lectores, libros y préstamos.

Características

-   Lectores: alta, baja, edición, búsqueda.
-   Libros: registro, inventario, categorías, disponibilidad.
-   Préstamos: crear/devolver, fechas, estado, historial.

Stack

-   Java (JDK 17+)
-   Swing (interfaz)
-   MySQL 8.x

Requisitos

-   JDK 17 o superior
-   MySQL 8.x
-   Variables de conexión a BD

Instalación

    # 1) Clonar
    git clone https://github.com/<usuario>/<repo>.git
    cd <repo>

    # 2) Crear BD
    # Importa el script en /sql/schema.sql (tablas: lectores, libros, prestamos, etc.)

Configuración

Crea un archivo .env o config.properties (según usen) con:

    DB_URL=jdbc:mysql://localhost:3306/biblioteca?useSSL=false&serverTimezone=UTC
    DB_USER=tu_usuario
    DB_PASS=tu_password

Ejecución

-   Con IDE (IntelliJ/Eclipse/NetBeans): abrir el proyecto y ejecutar
    Main.
-   Concompilación simple:

    javac -cp lib/mysql-connector-j.jar -d out src/**/*.java
    java  -cp "out;lib/mysql-connector-j.jar" Main

Estructura del proyecto (resumen)

    src/
      main/
        java/
          app/Main.java
          domain/        # entidades: Lector, Libro, Prestamo
          dao/           # DAO + JDBC
          service/       # lógica de negocio
          ui/            # pantallas Swing
    sql/
      schema.sql
      seed.sql
    lib/
      mysql-connector-j.jar

Uso

1.  Inicia sesión / conecta a la BD.
2.  Gestiona Lectores y Libros.
3.  Crea Préstamos y registra devoluciones.
4.  Consulta historial y disponibilidad.

Roadmap

-   Reportes (PDF/Excel)
-   Búsqueda avanzada
-   Validaciones y manejo de errores mejorado

Contribución

-   Issues y PRs bienvenidos.
-   Estándar de código: Java conventions.
-   Commits claros y descriptivos.

Autores

-   Juan Celedonio
-   Gilbert Perdomo
-   Erasmo Ortega

Licencia

.
