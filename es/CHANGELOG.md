# Registro de cambios

[English](../CHANGELOG.md) · **Español (México)**

> Traducción de referencia. Si algo difiere, manda la versión en inglés, que es la que se
> publica en cada versión de GitHub.

Cada versión de RelayPad que llega al repositorio público de
[versiones de RelayPad](https://github.com/ElegantCatterpillar/RelayPad/releases). El formato
sigue [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/) y las versiones siguen
[Versionado Semántico](https://semver.org/lang/es/) (mientras RelayPad esté en 0.x, una versión
menor puede cambiar el comportamiento).

La sección de cada versión también es el texto de su versión en GitHub, así que está escrita
para jugadores, no para desarrolladores.

## [0.3.0] - Sin publicar

La versión del editor y del NFC: los perfiles se rehacen alrededor de nombres que tú eliges, el
Control Pro de Switch 1 lee y escribe etiquetas NFC, y la batería marca lo mismo en todos los
lugares donde se muestra.

### Agregado

#### NFC (Control Pro de Switch 1)

- **Vista NFC** que se abre con un botón de la pantalla principal, como Ajustes. El botón solo
  se habilita cuando el control conectado tiene lector NFC; si no, su descripción emergente
  dice por qué.
- **Leer etiquetas:** tipo de etiqueta, UID y, para amiibo, el ID del amiibo y el nombre del
  personaje. Los nombres vienen de una base de datos incluida en la app, combinada con
  amiiboapi.org.
- **Lectura continua:** el lector vuelve a empezar después de cada lectura terminada, así que
  puedes acercar una etiqueta tras otra.
- **Historial:** cada etiqueta leída en la sesión, con cuántas veces se vio, exportación a CSV
  y un botón para borrarlo.
- **Escribir etiquetas NTAG en blanco:** un texto corto, o un ID de amiibo que leíste antes
  (guardado con el nombre del personaje). La etiqueta escrita es una etiqueta NDEF simple y sin
  bloquear: RelayPad muestra el texto o el personaje cuando la vuelve a leer, pero no es un
  amiibo para una Switch ni para un juego.
- **Escrituras seguras:** RelayPad se niega a escribir sobre un amiibo, una etiqueta de solo
  lectura o bloqueada, o una etiqueta sin formato NDEF. Nunca activa bits de bloqueo y nunca
  toca las páginas de identidad de la etiqueta.
- **Guía de enlace:** la vista indica, para la conexión actual, si el NFC funciona y qué
  conectar. Por Bluetooth funciona solo; por USB el control también necesita su enlace
  Bluetooth con esta PC, así que RelayPad lo pide en lugar de iniciar una lectura que haría que
  el control soltara el cable.

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

- **Cuatro jugadores** en la franja de lugares, y unión de Joy-Con 2 con un gesto.
- Botón **Desconectar** para un control conectado.
- **Interruptor de búsqueda Bluetooth:** evita que RelayPad busque controles Bluetooth mientras
  no lo necesitas.
- Botón de **Registro de actividad** en la pantalla principal; presionarlo otra vez cierra la
  ventana.
- **Pasos de emparejamiento por control en la pantalla de espera,** con tarjetas de Joy-Con 2
  y una guía que lista los pasos por USB y por Bluetooth de cada modelo.
- Botones de inicio y de regresar en la barra superior reemplazan el botón de regresar de cada
  vista.

#### Otros

- Los LEDs de jugador del Control Pro de Switch 1 se leen de vuelta y se reescriben cuando no
  coinciden con su jugador.
- Todas las advertencias del puente están traducidas (inglés y español).
- Las entradas del registro de actividad conservan el nombre de su control después de que se
  desconecta.
- Los reportes de diagnóstico opcionales también registran los tiempos de conexión Bluetooth.
- **Licencia:** RelayPad es freeware para uso personal. La licencia y los avisos de cada
  dependencia de Rust incluida (`THIRD_PARTY_LICENSES`) vienen con el instalador y se enlazan
  desde Acerca de.

### Cambiado

- **Batería:** el porcentaje se calcula una sola vez, con la curva propia de cada control, y se
  envía junto con su nivel de firmware. La línea de conexión, la línea periódica, la bandeja y
  el registro de energía ahora muestran el mismo número con el mismo formato.
- **Las actualizaciones** vienen del repositorio público renombrado
  `ElegantCatterpillar/RelayPad`. Si la 0.2.0 no ofrece esta actualización por sí sola,
  descarga el instalador desde Releases una vez; las versiones siguientes se actualizan desde
  el nombre nuevo.
- **Ajustes → Controladores** solo lista los controladores que puedes instalar hoy (ViGEmBus y
  HidHide).
- El NFC salió del editor de perfiles a su propia vista, porque pertenece al control, no a un
  perfil.
- Se quitó la pestaña Apariencia del editor.

### Corregido

- Una batería llena marca 100 % mientras carga, en lugar de quedarse en 99 % o cambiar cada
  segundo.
- La franja de lugares de jugador ya no parpadea "pendiente" mientras un control conectado
  busca su otro enlace (USB o Bluetooth) en segundo plano.
- Iniciar el NFC solo por USB ya no hace que el Control Pro de Switch 1 suelte el cable y
  busque a su anfitrión.

## [0.2.0] - 2026-10-21

La primera versión pública, para amigos: un instalador de Windows firmado con actualizaciones
automáticas.

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
