# Wigreen

[Descargar APK](https://github.com/lferraro1103/Wigreen/releases/latest)

App Android independiente para dos widgets de color salvia/oliva:

- Hora y fecha centradas sobre fondo transparente, con temperatura y condición de Samsung Clima.
- Barra Google con accesos a Google, búsqueda, voz y Lens, conservando el verde elegido.

Abrí Wigreen, elegí el widget y tocá Agregar al inicio. Para el clima, permití leer Samsung Clima y elegí una ubicación. Tocando el reloj podés cambiar la ciudad o abrir Samsung Clima; las nuevas ciudades se agregan allí.

Samsung obtiene y actualiza el tiempo. Wigreen lee los datos locales con el permiso `com.samsung.android.weather.permission.READ_DANGEROUS_PROVIDER`. Cuando Samsung usa The Weather Channel, muestra sus datos. Los datos con más de una hora muestran «sin actualizar». Todos los widgets de clima comparten la ubicación seleccionada.

No incluye anuncios, cuentas, Internet, GPS ni captura de micrófono/cámara. Google ejecuta voz y Lens con sus propios permisos. La barra no tiene actualizaciones periódicas. El reloj usa TextClock; el clima se lee aproximadamente cada 30 minutos según Android.

Requiere Android 8+. El clima necesita un Samsung con proveedor compatible; verificado en Galaxy Z Fold 6 con Android 16. La app Google debe estar habilitada para voz y Lens. Las actualizaciones de Samsung/Google pueden cambiar sus interfaces.

Código nativo Java; JDK 17, SDK 35, Gradle 8.9. Configurá ANDROID_HOME y compilá `gradlew.bat assembleDebug`. Para release, configurá tu propia clave en signing.properties como en Licon. Las claves y configuraciones privadas no se publican.

Identificador: ar.wigreen. Versión actual: 1.0.1. Optimización de consultas y redibujado del clima, con cancelación de tareas detenidas. Icono: hoja circular verde oliva.


## Licencia

El código y los recursos propios de esta aplicación se ofrecen bajo **PolyForm Noncommercial License 1.0.0**. Podés usar, estudiar, modificar y compartir la app con fines no comerciales, conservando la licencia y los avisos de autoría. La licencia no autoriza venderla ni explotarla comercialmente.

Para un uso comercial se necesita autorización separada del titular. Consultá el texto completo en [LICENSE.md](LICENSE.md) y los avisos en [NOTICE.txt](NOTICE.txt). Los componentes de terceros mantienen sus respectivas licencias.

## Separación en dos apps

La versión 1.1 separa las funciones: **Wigreen 1** (`ar.wigreen`, proyecto raíz) contiene solo hora, fecha y clima. **Wigreen 2** (`ar.wigreen2`, carpeta Wigreen2) contiene solo la barra de Google. Cada widget abre su propia app. Wigreen 1 actualiza la instalación anterior y conserva la ubicación; la barra anterior debe agregarse nuevamente desde Wigreen 2. Licon no cambia.

Los nuevos APK tienen compilación, Android Lint y firmas verificados. La instalación y las pruebas en dispositivo de clima, reloj, transparencia, cancelación y acciones Google/búsqueda/voz/Lens fueron verificadas. Ambas apps abren su propia pantalla.


Wigreen 2 versión 1.0.1 no tiene pantalla de configuración ni icono en el menú de aplicaciones. Agregá la barra desde **Widgets → Wigreen 2**. Sus botones abren Google, búsqueda, voz y Lens. Los widgets existentes se conservan al actualizar.
