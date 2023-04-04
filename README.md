# Aplicación de Android con WebView

Este es un tutorial para crear una aplicación de Android que incluye un WebView para cargar un archivo HTML local. El lenguaje utilizado es Java y el entorno de desarrollo es Android Studio Electric Eel (2022.1.1).

## Pasos

* Abre Android Studio y crea un nuevo proyecto.
* Selecciona "teléfonos y tabletas" y después la plantilla de "actividad vacía".
* Dale un nombre a tu aplicación y selecciona el lenguaje Java.
* Abre el archivo `activity_main.xml` y agrega el siguiente código:
```
<WebView android:id="@+id/webview" android:layout_width="match_parent" android:layout_height="match_parent" />
```
* Abre el archivo `MainActivity.java` y agrega el siguiente código:
```
import android.webkit.WebView;
import android.webkit.WebSettings;

WebView webView = findViewById(R.id.webview);
WebSettings webSettings = webView.getSettings();
webSettings.setJavaScriptEnabled(true);
webView.loadUrl("file:///android_asset/index.html");
```
* Crea la carpeta de recursos (`assets`) para los archivos adicionales.
* Agrega un archivo `index.html` estándar.
* Define el idioma del texto en el archivo como español mexicano (`es-MX`).
```
<html lang="es-MX">
```
* Agrega un título descriptivo.
```
<title>MiApp</title>
```
* Agrega un mensaje de saludo como contenido.
```
<body>Hola ✋</body>
```
* Inicia el proceso para generar el archivo empaquetado `apk` para instalar la aplicación.
* Sube el archivo a la memoria de tu teléfono.
* Ejecuta la instalación de la aplicación.
