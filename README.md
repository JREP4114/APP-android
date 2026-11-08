# LINCE GUARD — Hackatón LinceCode 2026

Aplicación Android de pruebas que escanea QR y códigos de barras continuamente con CameraX + ML Kit y valida las entradas desde el servidor LINCE ACCESS.

## Cómo generar el APK sin Android Studio

1. Descarga del chat el archivo **LINCE_GUARD_GITHUB_ACTIONS_LISTO.zip** (archivo fuente, ~17 KB).
2. En GitHub, en este repositorio, pulsa **Add file → Upload files**.
3. Sube el **ZIP SIN DESCOMPRIMIR**, con el nombre exacto `LINCE_GUARD_GITHUB_ACTIONS_LISTO.zip`, a la **raíz** del repositorio. Haz clic en **Commit changes** en `main`.
4. Abre **Actions → LINCE GUARD - Compilar APK Android**. Se ejecutará automáticamente cuando llegue el ZIP.
5. Si la compilación queda en verde, entra en la ejecución y descarga el artefacto **LINCE_GUARD_APK_ANDROID**.
6. Extrae el ZIP del artefacto; dentro estará `LINCE_GUARD_V0_3_1_DEBUG.apk` para instalarlo en tu teléfono Android.

El flujo `.github/workflows/compilar-apk.yml` ya está configurado para extraer el ZIP, probar Java, compilar el APK y publicarlo.

Si se muestra una X roja en Actions, comparte la captura del primer paso fallido para corregir el problema de compilación.

## Prueba con laptop y teléfono

- En la laptop ejecuta `iniciar-lince.bat` **de la V0.3.1 completa**.
- Conecta el Android a la misma red local compartida (por ejemplo `JREP 2821`).
- Configura la dirección IP real de la laptop en la app Android; `http://192.168.137.1:3000` es un ejemplo frecuente para el punto de acceso de Windows.
- Usa únicamente usuarios y alumnos ficticios durante las pruebas.

**Aviso de seguridad:** este es un prototipo educativo que utiliza HTTP en red local y credenciales de prueba. No subir bases de datos ni datos personales de estudiantes.
