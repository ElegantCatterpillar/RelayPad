# Respalda tus amiibo

[English](../amiibo-backup.md) · **Español (México)**

RelayPad puede leer un amiibo tuyo con tu control y guardar una copia en tu PC. Si la figura o
la tarjeta se pierde o se daña, puedes grabar esa copia en una etiqueta en blanco y seguir
usándola.

Funciona con el Control Pro de Switch 2 y el Joy-Con 2 derecho. En el Control Pro de Switch
(Switch 1) ya está hecha y sigue en pruebas con hardware.

## Solo para uso personal

- Respalda únicamente amiibo que te pertenecen, para tu propio uso.
- No compartas, vendas ni distribuyas los archivos de las copias ni las etiquetas grabadas con
  ellos.
- RelayPad no incluye datos de amiibo ni claves de Nintendo, no los descarga y no enlaza a
  sitios que los ofrezcan. Todo sale de tu propio amiibo, de tu propia consola y de tu propia
  PC.
- Las copias y las claves se quedan en tu PC. RelayPad nunca las sube y nunca las escribe en sus
  registros ni en sus reportes de diagnóstico.

Las leyes sobre copias de respaldo cambian de un país a otro. Revisa qué aplica donde vives.

## Qué necesitas

- Un control con lector NFC:
  - un **Control Pro de Switch 2**, por Bluetooth o con cable USB;
  - un **Joy-Con 2 derecho**, solo o unido a uno izquierdo. Apoya la etiqueta plana sobre su
    stick derecho. El Joy-Con 2 izquierdo no tiene lector;
  - un **Control Pro de Switch** (el modelo de Switch 1) por **Bluetooth**, con el cable USB
    desconectado. Mantiene apagado su lector NFC mientras el cable está conectado, aunque
    también haya conexión Bluetooth.
- El amiibo que quieres respaldar.
- Para grabar una copia en una etiqueta: una etiqueta **NTAG215** en blanco y **tu archivo de
  claves** (ver abajo).

## Hacer una copia

1. Abre la vista **NFC** desde la pantalla principal.
2. Apoya el amiibo en el control y mantenlo quieto.
3. RelayPad muestra el nombre y la imagen del personaje. Presiona **Guardar copia**.
4. La copia se guarda como un archivo `.bin` en tu carpeta de copias de amiibo. **Abrir
   carpeta** te la muestra. En **Configuración** puedes cambiar la carpeta, o hacer que cada
   amiibo que leas se guarde solo.

Hacer una copia solo lee el amiibo. No lo modifica.

## El archivo de claves

Un amiibo está firmado para la etiqueta en la que vive. Para pasar una copia a otra etiqueta,
RelayPad tiene que firmarla de nuevo para esa etiqueta, y eso requiere dos claves que son de
Nintendo.

- RelayPad no trae las claves y no puede conseguirlas.
- El archivo de claves tiene que salir de **tu propia consola**. Esta guía no explica cómo
  sacarlo, y RelayPad no ayuda con ese paso.
- Es un solo archivo de 160 bytes con las dos claves.

Sin el archivo de claves puedes hacer copias y ver qué amiibo contiene una copia. Solo lo
necesitas para grabar una copia en una etiqueta.

Para cargarlo, presiona **Escribir** en la vista NFC, elige el amiibo y en el paso 2 presiona
**Cargar archivo de claves…**. Con **Guardar una copia en esta PC** activado lo cargas una sola
vez: la copia se queda en la carpeta de RelayPad en tu PC. **Olvidar claves** borra esa copia.

## Grabar una copia en una etiqueta en blanco

Grabar sella la etiqueta para siempre. Se convierte en ese amiibo y no se puede volver a
escribir, por eso RelayPad pregunta antes de grabar.

1. En la vista NFC presiona **Escribir**, o **Copiar a otro tag** en un amiibo que acabas de
   respaldar.
2. Elige el amiibo: una de tus lecturas recientes, o una copia `.bin` con **Cargar .bin…**.
3. Carga tu archivo de claves si aún no está cargado. RelayPad te dice si la copia se verifica
   con tus claves; una que no se verifica no se graba.
4. Pon una NTAG215 en blanco en el control y presiona **Grabar amiibo**.
5. RelayPad lee la etiqueta y pregunta, nombrando el amiibo y la etiqueta. Revisa los dos y
   presiona **Sí, grabarlo**.
6. Mantén la etiqueta quieta hasta que RelayPad diga que terminó.

Solo se graba una NTAG215 en blanco. Cualquier otra etiqueta, incluido un amiibo, queda intacta.
Si cambias la etiqueta después de confirmar, no se graba nada en la nueva.

RelayPad no puede leer de vuelta los dos últimos valores que escribe en la etiqueta (su
contraseña), porque el control no los reporta. La forma de estar seguro es leer la etiqueta
nueva otra vez en RelayPad y probarla en tu consola.

## Preguntas

**¿La etiqueta grabada funciona en una consola?**
Esa es la idea: la etiqueta queda firmada y sellada como un amiibo original. Vuelve a leerla en
RelayPad para comprobarla y luego pruébala en tu consola.

**¿Puedo grabar encima de un amiibo o reutilizar una etiqueta?**
No. Un amiibo está sellado, igual que toda etiqueta que RelayPad graba.

**¿Puedo usar un `.bin` hecho con otra herramienta?**
Sí, si es una copia completa de un amiibo que te pertenece.

**¿De dónde saco el archivo de claves o los archivos de amiibo?**
Solo de tu propia consola y de tu propio amiibo. RelayPad no los proporciona ni enlaza a ellos.
