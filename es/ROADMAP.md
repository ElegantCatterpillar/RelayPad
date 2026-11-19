# Lo que viene para RelayPad

[English](../ROADMAP.md) · **Español (México)**

La meta de RelayPad es simple: todos los controles de Nintendo Switch, funcionando con todas
sus funciones, en todos los dispositivos donde juegas. Esta página dice en qué va cada control
y cada plataforma hoy, y qué sigue. Las prioridades pueden cambiar conforme probamos en hardware
real, y tus [ideas](https://github.com/ElegantCatterpillar/RelayPad/issues) ayudan a decidir el
orden.

Lo que ya salió: el [registro de cambios](CHANGELOG.md). ¿Quieres acelerarlo? [Apoya a RelayPad](README.md#apoya-a-relaypad):
el apoyo compra los controles de abajo y paga Linux, macOS y un controlador propio de RelayPad.

✅ funciona · 🧪 hecho, en pruebas con hardware · 🔜 lo siguiente · ⬜ planeado · 🔍 en estudio ·
❌ la plataforma no lo permite · — el control no tiene ese hardware

## Plataformas

| Plataforma | Estado | Qué esperar |
|---|---|---|
| Windows 10 y 11 | ✅ Disponible | Los juegos ven un control de Xbox 360 o DualShock 4. |
| Linux | 🔜 Lo siguiente | Los mismos controles, presentados a los juegos como un control estándar. |
| macOS | ⬜ Planeado, después de Linux | Necesita un permiso de Apple que todavía tenemos que obtener. |
| Android | ⬜ Planeado, más adelante | Una app que conecta los controles de Switch 2, que Android no puede emparejar por sí solo, y se los ofrece a tus juegos. Necesitará Shizuku, una app auxiliar gratuita; sin root. |
| iOS y iPadOS | ⬜ Planeado, como app de apoyo | iOS no permite que una app ofrezca un control a otros juegos, así que ahí RelayPad no puede hacer que tus juegos vean el control. La app servirá para cuidar tus controles de Switch 2. |

### Qué cubrirá cada plataforma

| Función | Windows | Linux | macOS | Android | iOS y iPadOS |
|---|---|---|---|---|---|
| Jugar tus juegos con el control | ✅ | ⬜ | ⬜ | ⬜ | ❌ |
| Movimiento y vibración en los juegos | ✅ | ⬜ | ⬜ | ⬜ | ❌ |
| Perfiles: reasignación, turbo, macros, curvas de los sticks, apuntado con giroscopio | ✅ | ⬜ | ⬜ | ⬜ | ❌ |
| Varios jugadores a la vez, cada uno con su control | ✅ | ⬜ | ⬜ | ⬜ | ❌ |
| Conectar por Bluetooth | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| Conectar con cable USB | ✅ | ⬜ | ⬜ | 🔍 | ❌ iPhone · 🔍 iPad |
| Estado y nivel de batería | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| Probar botones, sticks y movimiento | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| Calibración de los sticks | ✅ | ⬜ | ⬜ | ⬜ | 🔍 |
| LEDs de jugador | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |
| NFC: leer amiibo con el control | ✅ | ⬜ | ⬜ | ⬜ | 🔍 |

### Qué hará y qué no hará la app de iOS y iPadOS

Las marcas ❌ son límites del sistema, no de RelayPad: solo Apple decide qué controles pueden
ver los juegos.

**Sí hará**, con controles de Switch 2 por Bluetooth:

- mostrar el estado y el nivel de batería de cada control;
- dejarte probar botones, sticks y movimiento;
- cambiar los LEDs de jugador.

**No hará:**

- que tus juegos vean el control, así que no hay perfiles, ni movimiento o vibración en los
  juegos, ni jugadores;
- conectar un control con cable USB en un iPhone;
- agregar nada a los controles de Switch 1. iOS ya los conecta a tus juegos por sí solo, y no
  da a las apps una línea directa con ellos, así que funciones como NFC quedan fuera de alcance.

**Todavía en estudio:** el cable USB en un iPad, leer amiibo con controles de Switch 2 en iOS y
iPadOS, y la calibración de los sticks.

La columna de Windows dice lo que la app hace hoy; qué control tiene cada función se lista
abajo. Las demás plataformas tendrán su propio detalle conforme lleguen.

## Controles de Switch 2

### Control Pro de Switch 2

| Función | Estado | Notas |
|---|---|---|
| Bluetooth | ✅ | |
| Cable USB | ✅ | |
| Emparejar por Bluetooth al conectar el cable | 🧪 | |
| Cambiar entre cable y Bluetooth mientras juegas | ✅ | El juego nunca pierde el control. |
| Botones, sticks y gatillos | ✅ | Incluye GL, GR y C. |
| Movimiento (giroscopio y acelerómetro) | ✅ | |
| Vibración HD | ✅ | |
| LEDs de jugador | ✅ | |
| Nivel de batería | ✅ | |
| Ocultar el control real a los juegos (HidHide) | 🧪 | |
| NFC: leer amiibo y etiquetas | ✅ | Por Bluetooth y USB, con el nombre del personaje. |
| NFC: escribir un texto en una etiqueta en blanco | ✅ | |
| NFC: respaldar un amiibo tuyo y grabarlo en una etiqueta en blanco | ✅ | Con tu propio archivo de claves. Ver [Respalda tus amiibo](amiibo-backup.md). |

### Joy-Con 2, (L) o (R) por separado

| Función | Estado | Notas |
|---|---|---|
| Bluetooth | ✅ | |
| Cable USB | — | Los Joy-Con 2 no tienen puerto USB. |
| Botones y stick | ✅ | En horizontal, como un control pequeño. |
| Movimiento (giroscopio y acelerómetro) | ✅ | |
| Vibración | ✅ | |
| LEDs de jugador | ✅ | |
| Nivel de batería | ✅ | |
| Ocultar el control real a los juegos (HidHide) | 🧪 | |
| Modo mouse | ⬜ | |
| NFC: leer amiibo y etiquetas | ✅ | Solo el Joy-Con derecho; el izquierdo no tiene lector. Apoya la etiqueta sobre el stick derecho. |
| NFC: escribir un texto en una etiqueta en blanco | ✅ | Solo el Joy-Con derecho. |
| NFC: respaldar un amiibo tuyo y grabarlo en una etiqueta en blanco | ✅ | Solo el Joy-Con derecho, con tu propio archivo de claves. |

### Par de Joy-Con 2, (L) y (R) como un solo control

| Función | Estado | Notas |
|---|---|---|
| Las dos mitades como un solo control | ✅ | Mantén pulsados ZL y ZR a la vez. La pareja termina cuando cualquiera de las dos mitades se desconecta. |
| Botones y los dos sticks | ✅ | |
| Movimiento (giroscopio y acelerómetro) | ✅ | |
| Vibración | ✅ | |
| LEDs de jugador | ✅ | |
| Nivel de batería de cada mitad | ✅ | |
| Ocultar los controles reales a los juegos (HidHide) | 🧪 | |
| Modo mouse | ⬜ | |
| NFC: leer, escribir y respaldar amiibo | ✅ | Con el Joy-Con derecho del par. |

### Control de Nintendo GameCube (Nintendo Switch Online)

| Función | Estado | Notas |
|---|---|---|
| Compatibilidad completa | ⬜ | Sin empezar. |

## Controles de Switch 1

### Control Pro de Switch

| Función | Estado | Notas |
|---|---|---|
| Bluetooth | ✅ | Se empareja desde la configuración de Bluetooth de Windows, que se abre desde la app. |
| Cable USB | ✅ | |
| Botones, sticks y gatillos | ✅ | |
| Movimiento (giroscopio y acelerómetro) | ✅ | |
| Vibración HD | ✅ | |
| LEDs de jugador | ✅ | |
| Nivel de batería | ✅ | |
| Ocultar el control real a los juegos (HidHide) | ✅ | |
| NFC: leer amiibo y etiquetas | ✅ | Con el nombre del personaje. |
| NFC: escribir un texto o un ID de amiibo en una etiqueta en blanco | ✅ | La etiqueta no es un amiibo para una Switch ni para un juego. |
| NFC: respaldar un amiibo tuyo y grabarlo en una etiqueta en blanco | ✅ | Solo por Bluetooth, con tu propio archivo de claves. Ver [Respalda tus amiibo](amiibo-backup.md). |

### Joy-Con, (L) o (R) por separado

| Función | Estado | Notas |
|---|---|---|
| Bluetooth, botones y stick en horizontal | 🔜 | El siguiente control que agregamos. |
| Nivel de batería | 🔜 | |
| Movimiento, vibración y LEDs de jugador | ⬜ | |
| NFC: leer amiibo | ⬜ | Solo el Joy-Con derecho. |

### Par de Joy-Con, (L) y (R) como un solo control

| Función | Estado | Notas |
|---|---|---|
| Las dos mitades como un solo control | ⬜ | Después de que cada Joy-Con funcione por separado. |

### Joy-Con de NES (Nintendo Switch Online)

| Función | Estado | Notas |
|---|---|---|
| Bluetooth y botones | 🔜 | Llega junto con los Joy-Con. |

### Control de SNES (Nintendo Switch Online)

| Función | Estado | Notas |
|---|---|---|
| Compatibilidad completa | ⬜ | Sin empezar. |

### Control de Nintendo 64 (Nintendo Switch Online)

| Función | Estado | Notas |
|---|---|---|
| Compatibilidad completa | ⬜ | Sin empezar. |

### Control de SEGA Genesis (Nintendo Switch Online)

| Función | Estado | Notas |
|---|---|---|
| Compatibilidad completa | ⬜ | Sin empezar. |

## App

| Función | Estado | Notas |
|---|---|---|
| Instalador firmado | 🔜 | Para que Windows deje de advertir. Las actualizaciones ya van firmadas. |
| Ícono de bandeja por control | 🔜 | |
| Consejos para la mejor conexión Bluetooth | 🔜 | |
| Aviso de batería baja | 🔜 | Antes de que tu control se apague a mitad de la partida. |
| Salida DirectInput y GameInput | ⬜ | Además de Xbox 360 y DualShock 4. |
| Vista 3D del control | ⬜ | |

## ¿Tienes una idea?

[Abre un issue](https://github.com/ElegantCatterpillar/RelayPad/issues) con tu control, lo que
quieres que haga, el juego que juegas y el dispositivo donde juegas.

<sub>Traducción de referencia; si algo difiere, prevalece la versión en inglés.</sub>
