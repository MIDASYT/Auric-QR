# Auric QR

Sitio oficial de descarga: https://midasyt.github.io/Auric-QR/

Editor de códigos QR para Windows. El sitio contiene un único `index.html` y utiliza GitHub Releases para ofrecer la descarga del instalador sin páginas intermedias.

## Estado de versiones

- **v1.0.5 (Windows):** última versión publicada y descargable.
- **v1.0.6 (Windows + Android):** versión en desarrollo. No debe publicarse hasta completar las pruebas en ambos sistemas.
- **Android:** proyecto Android con generación, escaneo e historial local. Pendiente de compilar y validar el APK.

## Compilar el APK Android 1.0.6

El workflow **Auric QR Android 1.0.6 - APK de prueba** ya está configurado en `.github/workflows/android-1.0.6.yml`.

Para iniciarlo automáticamente, sube a la raíz del repositorio el archivo `auric-qr-android-1.0.6.zip`, conservando **exactamente ese nombre**. Debe contener la carpeta `Android/` con el proyecto Gradle. Al confirmar la subida en `main`, el workflow se ejecuta.

Luego abre [Actions](https://github.com/MIDASYT/Auric-QR/actions), entra a la ejecución **Auric QR Android 1.0.6 - APK de prueba** y descarga el artefacto `Auric-QR-Android-1.0.6-PRUEBA`. El artefacto contiene un `.apk` de desarrollo; primero hay que probarlo físicamente.

**No publiques directamente el APK de prueba en Releases**. Para actualizaciones estables hace falta firmar la edición de producción con una clave de Android permanente que no debe subirse al repositorio.

## Publicar la versión final cuando esté validada

Crea una Release con etiqueta `v1.0.6`. Adjunta el instalador Windows `Auric-QR-Setup-1.0.6.exe` y el **APK de producción firmado**, denominado `Auric-QR-Android-1.0.6.apk`. La página encontrará ambos archivos por el nombre y enlazará a los binarios directamente.

No necesitas modificar `index.html` para cada versión si los archivos respetan esos nombres.

## Código fuente

Los archivos «Source code (zip/tar.gz)» que GitHub muestra automáticamente en cada Release son capturas del **repositorio**, no equivalentes al ZIP de proyecto completo que se entrega por separado.

El proyecto de Windows y los archivos de Android pueden mantenerse en ZIPs propios de trabajo; no es obligatorio publicarlos como código fuente dentro de un repositorio público.
