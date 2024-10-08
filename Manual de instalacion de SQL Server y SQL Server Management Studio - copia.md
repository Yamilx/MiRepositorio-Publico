   # Instalación de SQL Server y SQL Server Management Studio

**Nombre:** [Yamil Leonel Mamani Guzman](https://www.facebook.com/yamil.guzman.58726)  
**Universidad:** [Universidad Privada Domingo Savio](https://www.upds.edu.bo/sede/santa-cruz/)  
**Carrera:** Ingeniería de Sistemas  

## 📌 Introducción

SQL Server es un sistema de gestión de bases de datos relacional desarrollado por Microsoft. Junto con SQL Server Management Studio (SSMS), proporciona una solución completa para la administración, desarrollo y despliegue de bases de datos. Esta guía proporciona una serie de pasos que debes seguir antes, durante y después de la instalación de SQL Server, con un enfoque especial en la configuración del collation y otros aspectos esenciales para garantizar el óptimo funcionamiento del sistema.

## 🎯 Objetivo

El objetivo de este manual es proporcionar una referencia completa sobre cómo instalar SQL Server y SSMS, explicando en detalle las consideraciones antes, durante y después de la instalación, así como la configuración de collation y otros aspectos fundamentales para un entorno de trabajo eficiente.

---

## 📚 Antes de Instalar SQL Server

Es crucial preparar el sistema antes de iniciar la instalación de **SQL Server** para evitar errores comunes y garantizar un entorno de trabajo estable.

### 1. **Espacio disponible en la unidad C:**
   - Asegúrate de que la unidad **C:** tenga suficiente espacio disponible para:
     - **Copias de seguridad:** SQL Server almacena copias de seguridad de las bases de datos en la unidad C por defecto. 
     - **Restauración de bases de datos:** El proceso de restauración también consume una cantidad considerable de espacio en la unidad C.
   - Es recomendable que mantengas al menos un 20-30% de espacio libre en la unidad C para asegurar la estabilidad y el correcto funcionamiento del servidor.

### 2. **Puerto por defecto (1433):**
   - SQL Server utiliza el puerto **1433** para aceptar conexiones remotas.
   - **Pre-instalación:** Verifica que este puerto no esté siendo utilizado por otros servicios.
   - **Post-instalación:** Asegúrate de habilitar el puerto **1433** en el firewall para permitir las conexiones externas. Esto se puede hacer a través del "Firewall de Windows con Seguridad Avanzada".

### 3. **Preparar la instancia:**
   - Durante la instalación de SQL Server, puedes optar por:
     - **Instancia predeterminada:** Utiliza el nombre **MSSQLSERVER** (ejemplo: para producción u oficial).
     - **Nueva instancia:** Para desarrollo o entornos personalizados, puedes crear una nueva instancia con un nombre específico, como **desarrollo2024**.
   - **Nota sobre la conexión:** Para conectarte a la instancia predeterminada puedes usar `"."`, `"localhost"` o el **nombre del host**. Para instancias personalizadas, el formato será `nombre_servidor\instancia`.

### 4. **Verificación del Collation:**
   - **Collation (intercalación)** es un conjunto de reglas que determina cómo se ordenan y comparan los caracteres.
   - Es importante seleccionar el collation correcto para tu región e idioma durante la instalación. Algunos ejemplos incluyen:
     - **Latin1_General_CI_AS** (inglés)
     - **Modern_Spanish_CI_AS** (español)
   - Si trabajas con una base de datos multilingüe, asegúrate de seleccionar un collation que soporte los caracteres y las reglas de ordenamiento de los idiomas que necesitas.

### 5. **Configurar el modo de autenticación (Mixto):**
   - SQL Server ofrece dos modos de autenticación:
     - **Solo autenticación de Windows:** Recomendado para entornos controlados donde no se necesita autenticación de SQL Server.
     - **Modo Mixto:** Habilita tanto la autenticación de Windows como la de SQL Server, permitiendo la cuenta **sa** (superusuario). Este modo es útil para la administración remota.
   - **Conección remota:** Si planeas conectar al servidor de forma remota, el modo mixto es esencial para facilitar las conexiones con credenciales SQL Server (usuario y contraseña).

---

## 📚 Al Instalar

Una vez hayas preparado tu sistema, puedes proceder con la instalación de SQL Server siguiendo estos pasos:

### 1. **Descargar el Instalador:**
   - Dirígete a [Microsoft SQL Server Downloads](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) y descarga la última versión del instalador de SQL Server.

### 2. **Ejecutar el Instalador:**
   - Inicia el instalador y selecciona la opción "Nueva instalación o agregar características a una instalación existente".

### 3. **Aceptar los Términos de Licencia:**
   - Acepta los términos de la licencia para continuar con el proceso de instalación.

### 4. **Seleccionar Características a Instalar:**
   - Elige las características que deseas instalar:
     - **Motor de base de datos**: Indispensable para la creación y gestión de bases de datos.
     - **Herramientas de administración**: Opcional, pero útil para administrar y monitorizar el servidor.
   - También puedes seleccionar otros componentes como "Servicios de Análisis" o "Servicios de Reportes" si son necesarios para tu entorno.

### 5. **Configurar la Instancia:**
   - **Instancia predeterminada:** Si seleccionas esta opción, el nombre de la instancia será **MSSQLSERVER**.
   - **Nueva instancia:** Define un nombre específico para la nueva instancia (por ejemplo, **desarrollo2024**).
   - Para conectar a una instancia predeterminada, utiliza `"."`, `"localhost"` o el **nombre del host**. Para instancias personalizadas, utiliza el formato `nombre_servidor\instancia`.

### 6. **Configurar el Collation:**
   - Durante la instalación, selecciona el collation que sea adecuado para tu entorno (por ejemplo, **Latin1_General_CI_AS** para inglés o **Modern_Spanish_CI_AS** para español).
   - Si no seleccionas el collation correcto, podrías experimentar problemas en la comparación y manipulación de texto.

### 7. **Modo de Autenticación:**
   - Elige el **modo mixto** para permitir tanto la autenticación de Windows como la de SQL Server.
   - **Habilitar la cuenta `sa`:** Asegúrate de habilitar la cuenta **sa** y definir una contraseña segura.
   - Esta cuenta será utilizada para la administración y las conexiones remotas.

### 8. **Completar la Instalación:**
   - Revisa todas las configuraciones y haz clic en "Instalar". 
   - Una vez finalizada la instalación, es posible que necesites reiniciar el servidor.

---

## 📚 Después de Instalar

Después de haber instalado SQL Server, es importante realizar algunas configuraciones adicionales para asegurar que el servidor funcione correctamente.

### 1. **Habilitar el puerto 1433 en el firewall:**
   - SQL Server utiliza el puerto **1433** por defecto para conexiones remotas. Asegúrate de que esté habilitado en el firewall.
   - Para habilitarlo, ve a la "Configuración de Firewall de Windows con Seguridad Avanzada", crea una nueva regla de entrada que permita las conexiones entrantes en el puerto **1433**.

### 2. **Verificar que los servicios estén en ejecución:**
   - Asegúrate de que los servicios de SQL Server y SQL Server Browser estén ejecutándose.
   - Puedes verificar esto en el "Administrador de Servicios de Windows" o desde la herramienta de configuración de SQL Server.

### 3. **Verificar el collation:**
   - Después de la instalación, puedes verificar el collation predeterminado de tu base de datos ejecutando la siguiente consulta en SSMS:
   ```sql
   SELECT SERVERPROPERTY('Collation');
   ```

   - Si el collation no es el correcto, podrías considerar modificarlo para evitar problemas en el futuro. Sin embargo, cambiar el collation después de la instalación puede ser complejo, así que es mejor configurarlo correctamente durante la instalación.

### 4. **Configurar la autenticación remota:**
   - Si planeas conectarte a SQL Server desde otra máquina, asegúrate de que las conexiones remotas estén habilitadas.
   
   - Puedes habilitar las conexiones remotas desde SSMS:
      -Conéctate al servidor, haz clic derecho sobre el nombre del servidor, selecciona **Propiedades.**
      -En la pestaña **Conexiones**, marca la casilla **Permitir** conexiones remotas a este servidor.

## **Instalar SQL Server Management Studio (SSMS):**

1. **Descargar el Instalador de SSMS:**
   - Visita el sitio web oficial de Microsoft para descargar SSMS. Puedes encontrarlo en [SQL Server Management Studio (SSMS) Downloads](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms).

2. **Ejecutar el Instalador:**
   - Abre el archivo descargado para iniciar el asistente de instalación.

3. **Instalar SSMS:**
   - Sigue las instrucciones del asistente de instalación. Puedes optar por la configuración predeterminada o personalizar la instalación según tus necesidades.

4. **Completar la Instalación:**
   - Una vez que SSMS esté instalado, reinicia el sistema si es necesario.

## Conclusiones

La correcta instalación de SQL Server y SSMS es fundamental para el manejo eficiente de bases de datos. Además, una adecuada configuración del collation asegura que los datos se comparen, ordenen y manejen de manera correcta, evitando problemas de integridad y rendimiento en la base de datos.

## Bibliografía

- [Microsoft. "SQL Server Downloads.](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
- [Microsoft. "SQL Server Management Studio (SSMS) Downloads.](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms)
- [Microsoft. "Collation in SQL Server.](https://learn.microsoft.com/en-us/sql/relational-databases/collations/collation-and-unicode-support?view=sql-server-ver16)
