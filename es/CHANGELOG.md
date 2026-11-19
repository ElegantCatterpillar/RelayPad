# Registro de cambios

[English](../CHANGELOG.md) · **Español (México)**

> Traducción de referencia. Si algo difiere, prevalece la versión en inglés, que es la que se
> publica en cada versión de GitHub.

Cada versión de RelayPad que llega al repositorio público de
[versiones de RelayPad](https://github.com/ElegantCatterpillar/RelayPad/releases). El formato
sigue [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/) y las versiones siguen
[Versionado Semántico](https://semver.org/lang/es/) (mientras RelayPad esté en 0.x, una versión
menor puede cambiar el comportamiento).

La sección de cada versión también es el texto de su versión en GitHub, así que está escrita
para jugadores, no para desarrolladores.

## [0.3.0] - 2026-11-19

La versión del editor y del NFC: perfiles con el nombre que tú les pones, NFC y amiibo en el
Control Pro de Switch 2, el Joy-Con 2 derecho y el Control Pro de Switch, y una batería que
marca lo mismo en todos los lugares donde la ves.

### Agregado

#### NFC en los controles de Switch 2

- **El Control Pro de Switch 2 lee y escribe NFC,** por Bluetooth y con cable USB, en la misma
  pantalla de NFC.
- **El Joy-Con 2 derecho también,** solo o unido a uno izquierdo: acerca la etiqueta sobre su
  stick derecho. El Joy-Con 2 izquierdo no tiene lector NFC, y la pantalla de NFC lo indica.
- **Respalda tus propios amiibo** y graba esa copia en una etiqueta NTAG215 en blanco, sellada
  como una original, con tu propio archivo de claves. Ver [Respalda tus amiibo](amiibo-backup.md).

#### NFC (Control Pro de Switch, Switch 1)

- **Pantalla de NFC,** que se abre con un botón de la pantalla principal. El botón se habilita
  cuando el control conectado tiene lector NFC; si no, te dice por qué.
- **Lee amiibo y etiquetas:** acerca uno al control para ver qué es y, si es un amiibo, el
  nombre del personaje.
- **Uno tras otro:** el lector sigue activo después de cada lectura, y un historial lista todo
  lo que leíste, con exportación a CSV.
- **Escribe en etiquetas NTAG en blanco:** un texto corto, o el ID de
  un amiibo que leíste antes. RelayPad muestra ese texto o personaje cuando vuelve a leer la
  etiqueta. La etiqueta no es un amiibo: una Switch o un juego no la reconocen.
- **Tus etiquetas están seguras:** RelayPad se niega a escribir sobre un amiibo, una etiqueta
  bloqueada o una etiqueta que no puede escribir de forma segura, y nunca bloquea una etiqueta.
- **Funciona por Bluetooth.** Con el cable conectado, el control también necesita su conexión
  Bluetooth con esta PC; la pantalla te dice qué conectar.

#### Editor del control

- **Perfiles con nombre por tipo de control,** con un menú de perfiles rediseñado y un selector
  de control en el encabezado. Los perfiles guardados por la 0.2.0 se abren en una vista de
  solo lectura.
- **Sticks:** zonas muertas interactivas sobre una vista en vivo del stick, vista previa de la
  curva de respuesta e inversión de X y Y para cada stick por separado.
- **Botones:** un diseño compacto junto a una imagen del control físico.
- Pestañas de **Turbo** y **Macros**, cada una con una guía corta para crear uno.
- **Salida:** un diseño más claro con textos de ayuda, y **vista previa de vibración**: prueba
  ajustes de vibración sin guardar en el control que elijas antes de guardarlos.
- Descripciones emergentes en cada pestaña del editor.

#### Pantalla principal y estado

- **Cuatro jugadores, antes ocho:** un control por jugador, como en una consola. Un quinto
  control se queda conectado y espera a que se libere un jugador.
- Unión de Joy-Con 2 con un gesto.
- Botón **Desconectar** para un control conectado.
- **Interruptor de búsqueda Bluetooth:** evita que RelayPad busque controles Bluetooth mientras
  no lo necesitas.
- Botón de **Registro de actividad** en la pantalla principal; presionarlo otra vez cierra la
  ventana.
- **Pasos de emparejamiento por control en la pantalla de espera,** con tarjetas de Joy-Con 2
  y una guía que lista los pasos por USB y por Bluetooth de cada modelo.
- Botones de inicio y de regresar en la barra superior reemplazan el botón de regresar de cada
  vista.

#### Instalación y configuración

- **La configuración inicial ofrece HidHide** junto a ViGEmBus y explica para qué sirve cada
  uno. ViGEmBus es necesario; HidHide es recomendado, para que los juegos solo vean el mando
  virtual y nunca lean una pulsación dos veces. Ambos se instalan desde sus versiones oficiales,
  con la suma de verificación comprobada.
- **Al desinstalar RelayPad se vuelve a mostrar cualquier control que dejó oculto** y RelayPad
  sale de los programas permitidos de HidHide. HidHide sigue instalado, y las actualizaciones
  mantienen la configuración como está.
- **El desinstalador dice qué quita:** la app, sus accesos directos y su inicio con Windows; los
  controladores se quedan. Su casilla "Eliminar los datos de aplicación" también borra ajustes,
  registros, perfiles y copias y claves de amiibo guardados en las carpetas de RelayPad.
- El instalador y el desinstalador están en español cuando Windows lo está.

#### Otros

- Los LEDs de jugador del Control Pro de Switch se corrigen cuando no coinciden con su jugador.
- Todas las advertencias que muestra la app están traducidas (inglés y español).
- Las entradas del registro de actividad conservan el nombre de su control después de que se
  desconecta.
- Los reportes de diagnóstico opcionales también registran los tiempos de conexión Bluetooth.
- **Licencia:** RelayPad es gratis para uso personal. La licencia y los avisos de terceros
  vienen con el instalador y se enlazan desde Acerca de.
- **Reportar en GitHub:** después de un cierre inesperado, el siguiente inicio ofrece
  reportarlo; el registro de errores también tiene el botón, para todo el registro o para una
  línea. Abre un issue ya escrito con el informe de diagnóstico, con los números de serie y las
  direcciones Bluetooth ocultos.
- **Controles en el menú de la bandeja:** haz clic en un control para abrir RelayPad en él, o en
  su engrane para abrir su configuración.
- **Apoyar a RelayPad** en Acerca de abre la página de apoyo. El apoyo es opcional y no
  desbloquea nada.

### Cambiado

- **Batería:** el porcentaje se calcula una sola vez para cada control, así que la bandeja y
  cada línea del registro de actividad muestran el mismo número.
- **Las actualizaciones** vienen del repositorio público renombrado
  `ElegantCatterpillar/RelayPad`. Si la 0.2.0 no ofrece esta actualización por sí sola,
  descarga el instalador desde Releases una vez; las versiones siguientes se actualizan desde
  el nombre nuevo.
- **Ajustes → Controladores** solo lista los controladores que puedes instalar hoy (ViGEmBus y
  HidHide).
- El NFC salió del editor de perfiles a su propia vista, porque pertenece al control, no a un
  perfil.
- Se quitó la pestaña Apariencia del editor.
- Cada versión muestra el SHA-256 del instalador y un enlace a su análisis de VirusTotal.

### Corregido

- Una batería llena marca 100 % mientras carga, en lugar de quedarse en 99 % o cambiar cada
  segundo.
- La franja de lugares de jugador ya no parpadea "pendiente" mientras un control conectado
  busca su otro enlace (USB o Bluetooth) en segundo plano.
- Iniciar el NFC solo con el cable conectado ya no desconecta el Control Pro de Switch.

## [0.2.0] - 2026-10-21

La primera versión pública, para amigos: un instalador de Windows con actualizaciones
automáticas. Las actualizaciones van firmadas y la app revisa esa firma antes de instalar una;
el instalador todavía no tiene firma de código.

### Agregado

- **Controles:** Control Pro de Nintendo Switch 2 por Bluetooth LE y USB; Control Pro de
  Nintendo Switch (Switch 1) por USB y Bluetooth; Joy-Con 2 por Bluetooth LE, individual (en
  horizontal) o un izquierdo y un derecho unidos en un solo control.
- **Controles virtuales:** Xbox 360 o DualShock 4 mediante ViGEmBus, uno por control, hasta
  ocho controles a la vez, cada uno en un lugar de jugador estable. Los jugadores después del
  cuarto usuario de Xbox pasan a ser un DualShock 4.
- **Relevo entre USB y Bluetooth:** conectar o desconectar el cable mantiene el mismo control
  virtual. Conectar un Control Pro de Switch 2 por USB también lo empareja, así que el
  Bluetooth se reconecta después sin el botón de sincronización.
- **Perfiles (`.repad`):** reasignación de botones, zonas muertas y curvas de respuesta, turbo,
  macros, apuntado con giroscopio y mouse con giroscopio, vibración y LEDs de jugador, con
  importación y exportación. La calibración de los sticks se guarda por control.
- **App de bandeja:** estado con batería, LEDs de jugador, apodo, identificar (vibración),
  valores de los sticks en vivo y una ventana de diagnóstico; ventana emergente en la bandeja,
  notificaciones e inicio con Windows.
- **Posición de jugador:** mueve un control a un jugador libre o intercámbialo con el que esté
  ahí.
- **Página de Controladores:** instala, revisa y quita ViGEmBus y HidHide. HidHide oculta el
  control real para que los juegos solo vean el control virtual.
- **Emparejamiento del Control Pro de Switch 1:** la vista de estado abre "Agregar dispositivo"
  de Windows y muestra los pasos del botón de sincronización.
- **Joy-Con 2:** unir y separar desde la vista de estado; los pares unidos se recuerdan y se
  vuelven a unir.
- Porcentaje de **batería** a partir de curvas ajustadas a descargas medidas de cada modelo.
- **Registro de actividad** dividido en eventos, energía y errores, cada uno en su pestaña,
  etiquetado y filtrable por control.
- **Reportes de diagnóstico:** opcionales y solo locales; se piden en el primer inicio.
- **Idioma:** inglés y español, elegido desde la barra superior.
- **Actualizaciones automáticas** desde el repositorio público de versiones, instaladas cuando
  ningún control está en uso.
