Aquí tienes una guía actualizada para instalar y configurar el entorno de **RoboCup Soccer Simulation** en sistemas operativos modernos como **Ubuntu 22.04** o **Debian 11**. Esta guía cubre la instalación del servidor, monitor, y herramientas necesarias para ejecutar simulaciones de partidos de fútbol.

### Instalación y Configuración del Entorno

#### Requisitos Previos
Es necesario tener instaladas ciertas dependencias para poder compilar y ejecutar los componentes de RoboCup Soccer Simulation. Abre una terminal y ejecuta el siguiente comando:

```bash
sudo apt-get install g++ build-essential libboost-all-dev qt5-default libaudio-dev libgtk-3-dev libxt-dev bison flex
```

### Instalación del Servidor y Monitor

1. **Descarga de archivos:**
   Visita el repositorio oficial de RoboCup Soccer Simulation y descarga las versiones actuales de los archivos `rcssserver` y `rcssmonitor`. Suelen tener un nombre similar a `rcssserver-x.x.x.tar.gz` y `rcssmonitor-x.x.x.tar.gz`, donde `x.x.x` representa la versión del archivo.

2. **Extracción del Servidor:**
   Una vez descargado, extrae el archivo del servidor ejecutando:

   ```bash
   tar -zxpf rcssserver-x.x.x.tar.gz
   ```

3. **Configuración y Compilación del Servidor:**
   Ahora, accede al directorio del servidor y compila el código:

   ```bash
   cd rcssserver-x.x.x
   ./configure && make
   sudo make install
   ```

4. **Instalación del Monitor:**
   Para instalar `rcssmonitor`, sigue los mismos pasos que para el servidor, pero con el archivo correspondiente:

   ```bash
   tar -zxpf rcssmonitor-x.x.x.tar.gz
   cd rcssmonitor-x.x.x
   ./configure && make
   sudo make install
   ```

### Instalación de Herramientas Adicionales

**Nota:** Las herramientas mencionadas a continuación son esenciales para crear agentes y equipos de fútbol en la simulación.

1. **Descarga de `librcsc` y `agent2d`:**
   Visita el repositorio de herramientas de RoboCup en SourceForge y descarga los archivos correspondientes:

   - `librcsc`
   - `agent2d`

2. **Extracción de Archivos:**
   Accede al directorio donde descargaste los archivos y extráelos:

   ```bash
   tar -zxpf librcsc-x.x.x.tar.gz
   tar -zxpf agent2d-x.x.x.tar.gz
   ```

### Instalación de `librcsc`

1. **Configuración del Sistema:**
   Es importante que tu sistema esté configurado en inglés para evitar errores de entrada/salida debido al uso de separadores decimales. Si tu sistema está en otro idioma, ejecuta:

   ```bash
   export LC_NUMERIC="C"
   ```

2. **Configuración y Compilación:**
   Accede al directorio de `librcsc` y compila el código:

   ```bash
   cd librcsc-x.x.x/
   ./configure
   make
   sudo make install
   ```

### Instalación de `agent2d`

1. **Configuración y Compilación:**
   Accede al directorio de `agent2d` y compila el código:

   ```bash
   cd agent2d-x.x.x/
   ./configure
   make
   sudo make install
   ```

### Instalación Opcional del Monitor `soccerwindow2`

Este monitor proporciona información más detallada sobre los partidos y jugadores, y se utiliza en la Copa Mundial de RoboCup.

1. **Descarga e Instalación:**
   Descarga el archivo `soccerwindow2-x.x.x.tar.gz` desde el repositorio de RoboCup y sigue los siguientes pasos:

   ```bash
   tar -zxpf soccerwindow2-x.x.x.tar.gz
   cd soccerwindow2-x.x.x
   ./configure
   make
   sudo make install
   ```

### Solución de Problemas Comunes

- **Error con la opción ‘-pthread-lQtGui’:**
  Si encuentras un error similar, abre el archivo `configure` y busca la línea relacionada con `QT4_LDADD`. Agrega un espacio entre `$PKG_CONFIG` y las variables para que la línea se vea así:

  ```bash
  QT4_LDADD="$($PKG_CONFIG --static --libs-only-other $QT4_REQUIRED_MODULES) $($PKG_CONFIG --static --libs-only-l $QT4_REQUIRED_MODULES)"
  ```

### Conclusión

Una vez completados todos los pasos, puedes ejecutar un partido de prueba para asegurarte de que todo está funcionando correctamente.

Aquí tienes la sección actualizada sobre cómo ejecutar un partido de RoboCup Soccer Simulation:

---

### Ejecutar un Partido

Para seguir este tutorial, asegúrate de haber completado la instalación y configuración de los componentes del servidor y monitor descritos anteriormente.

#### 1. Iniciar el Servidor

Abre una terminal y ejecuta el servidor:

```bash
rcssserver &
```

Este comando inicia el servidor en segundo plano.

#### 2. Iniciar el Monitor

Necesitas un monitor para visualizar el partido. Puedes elegir entre `rcssmonitor` y `soccerwindow2`. Abre una nueva terminal y ejecuta uno de los siguientes comandos según el monitor que hayas instalado:

```bash
rcssmonitor &
```

o

```bash
soccerwindow2 &
```

Ambos comandos inician el monitor en segundo plano.

#### 3. Llevar Equipos al Campo

Para añadir equipos al campo de juego, sigue estos pasos:

1. **Accede al directorio de `agent2d`:**

   ```bash
   cd path/to/agent2d/src/
   ```

   Reemplaza `path/to/agent2d` con la ruta real al directorio `agent2d`.

2. **Ejecuta el script para iniciar un equipo:**

   ```bash
   ./start.sh -t team_name
   ```

   Reemplaza `team_name` con el nombre del equipo deseado.

   **Nota:** Si encuentras problemas de permisos con el script, puedes resolverlo ejecutando:

   ```bash
   sudo chmod +x start.sh
   ```

   Si los problemas persisten, puedes modificar los permisos del directorio con:

   ```bash
   sudo chmod 777 *
   ```

3. **Abrir otra terminal y repetir el proceso para el segundo equipo:**

   Ejecuta el mismo comando en una nueva terminal, reemplazando `team_name` con el nombre del segundo equipo.

#### 4. Realizar el Inicio del Partido

Una vez que ambos equipos estén en el campo, puedes iniciar el partido utilizando la siguiente combinación de teclas en el monitor:

- **Ctrl+K**: Realiza el inicio del partido (kick-off).

---
