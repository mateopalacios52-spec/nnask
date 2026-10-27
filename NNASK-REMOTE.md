# nnask Remote

Dos apps para manejar un Android TV o Xiaomi TV Stick desde un teléfono Android en la misma red Wi-Fi.

- **nnask Remote** se instala en el celular. Muestra la pantalla de la TV y permite tocar, deslizar, mantener pulsado, usar flechas, escribir, abrir apps y controlar la reproducción y el volumen del dispositivo.
- **nnask Remote TV** se instala en el televisor o TV Stick. Comparte la pantalla con tu autorización y recibe las acciones del teléfono vinculado.

## Descargar

[Para el celular](https://github.com/mateopalacios52-spec/nnask/releases/download/remote/nnask-remote.apk) · [Para Android TV](https://github.com/mateopalacios52-spec/nnask/releases/download/remote/nnask-remote-tv.apk)

## Primera conexión

1. Instalá la app correspondiente en cada dispositivo. Android 8 o posterior. No reemplazan la app principal nnask.
2. Conectalos al mismo Wi-Fi. Abrí nnask Remote TV y activá **Control de nnask Remote** en Accesibilidad.
3. En la TV elegí **Compartir pantalla y conectar** y aceptá el aviso de Android. Si ofrece elegir, compartí la pantalla completa. También existe el modo **solo mando**.
4. En el teléfono tocá **Buscar TV** o escribí la IP y el puerto que muestra la TV. Introducí su código una sola vez y tocá **Conectar**.
5. La vinculación queda guardada. Al volver a abrir la app del celular intenta reconectar sin pedir el código. El servicio debe continuar activo en la TV.

## Uso diario

Tocá la imagen para seleccionar, deslizá para desplazar y mantené pulsado para una pulsación larga. Algunas apps diseñadas para TV solo aceptan flechas y OK. Los gestos dependen de la app que estés controlando.

Cerrar la app del teléfono no borra la vinculación. Si cambia la dirección de la TV, usá **Buscar TV**. Si se reinicia la TV o se detiene la captura, abrí nnask Remote TV e iniciá otra conexión: Android puede exigir autorizar de nuevo la pantalla, pero el código no se repite.

**Desvincular** revoca el teléfono. También puede hacerse directamente en la TV. **Detener conexión** en la TV o en su notificación apaga el servicio conservando la vinculación.

Ambas apps buscan actualizaciones y tienen un botón **Buscar actualizaciones**. Android pide confirmar la instalación; no hay instalaciones silenciosas. Se conservan los datos al actualizar con la misma firma.

## Privacidad y límites

Solo red local IPv4 privada. Sin cuentas, nube, grabaciones, root, ADB ni comandos de shell. Código inicial aleatorio con límite de intentos. Credencial aleatoria guardada cifrada con Android Keystore, mensajes e imágenes cifrados con AES-GCM, claves por sesión y desafíos de reconexión de un solo uso. Un teléfono autorizado por TV. La notificación permite detener el acceso.

La captura conserva la autorización visible de Android. No arranca capturas automáticamente después de un reinicio. La vinculación persistente no elimina los permisos del sistema ni garantiza una conexión cuando la TV está apagada, sin Wi-Fi o el sistema detuvo el servicio.

Vista de navegación de hasta 960×540 y cuatro imágenes por segundo, sin audio en el celular. El contenido protegido puede aparecer negro. El volumen corresponde al TV Stick o a la app; no se garantiza encendido, entradas HDMI ni control del televisor físico.

Las actualizaciones se descargan por HTTPS desde este repositorio y comprueban tamaño, SHA-256, paquete, código interno y firma original antes de abrir el instalador.

## Desarrollo

Proyecto Android con módulos `tv`, `phone` y código compartido `shared`. Java 17, Android SDK 35, Gradle 8.11.1. Las versiones internas solo se usan para compatibilidad y actualizaciones; no se muestran en la interfaz ni en los nombres de descarga. No se incluyen claves de firma, datos de dispositivos ni credenciales.
