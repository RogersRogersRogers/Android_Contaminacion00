# Android Contaminación

Este proyecto es una aplicación de Android que permite la búsqueda de dispositivos **Bluetooth Low Energy (BTLE)**, así como la interacción con un servidor para enviar datos utilizando la librería Retrofit.

## Características

- Búsqueda de dispositivos BTLE cercanos.
- Conexión y escaneo de dispositivos BTLE específicos.
- Envío de datos a un servidor mediante **Retrofit**.
- Visualización de los datos recibidos de los dispositivos BTLE en la interfaz de usuario.

## Requisitos

- Android SDK **26** o superior.
- Target SDK **34**.
- Compile SDK **34**.
- JDK 1.8.

## Dependencias principales

El proyecto utiliza las siguientes dependencias:

- **AndroidX Libraries**: Para compatibilidad y componentes de diseño.
- **Retrofit 2.9.0**: Para manejar peticiones HTTP y trabajar con APIs REST.
- **Gson Converter**: Para la conversión de respuestas JSON a objetos Java.

## Permisos
- Bluetooth y Bluetooth Admin: Para búsqueda y gestión de dispositivos Bluetooth.
- Bluetooth Scan y Bluetooth Connect: Para escanear dispositivos BTLE y conectarse a ellos.
- Acceso a Ubicación (Fina y Aproximada): Necesario para escanear dispositivos BTLE, ya que el escaneo Bluetooth en Android requiere permisos de ubicación.
- Permiso de Internet: Para conectarse a un servidor remoto utilizando Retrofit.

## Configuración del Proyecto
- build.gradle.kts
Este archivo define las configuraciones del proyecto:

El compileSdk y targetSdk están configurados en 34.
Se establecen las configuraciones de lanzamiento (build types), habilitando Proguard para el entorno de producción.

- AndroidManifest.xml
Este archivo especifica los permisos requeridos por la aplicación, así como la configuración de seguridad de la red para permitir el tráfico HTTP a una dirección local específica.

- Seguridad de la Red
El archivo network_security_config.xml permite el tráfico no cifrado (HTTP) a una IP local específica (por ejemplo, 192.168.1.26). Para producción, se recomienda utilizar HTTPS para mayor seguridad.

## Uso
1. Buscar dispositivos BTLE
La aplicación puede buscar dispositivos BTLE cercanos presionando el botón "Buscar Dispositivos BTLE".

2. Detener la búsqueda de dispositivos BTLE
Para detener el escaneo de dispositivos, el usuario puede presionar "Detener búsqueda Dispositivos BTLE".

3. Enviar datos al servidor
El usuario puede introducir un valor numérico en el campo de texto y luego presionar el botón "Enviar" para enviar los datos a un servidor usando Retrofit.

4. Mostrar los datos recibidos
Los datos recibidos de los dispositivos BTLE o del servidor se mostrarán en el área designada en la interfaz de usuario.

## Funciones
Retrofit
El proyecto utiliza Retrofit para realizar llamadas HTTP al servidor. Se ha configurado un convertidor de JSON utilizando Gson para gestionar las respuestas del servidor.

## Respaldo y Restauración de Datos
La aplicación utiliza reglas de respaldo definidas en los archivos backup_rules.xml y data_extraction_rules.xml para permitir la copia de seguridad automática y la transferencia de datos en dispositivos con Android 12 o superior.

## Desarrollo
Requisitos
Android Studio
JDK 8

## Clonar el proyecto
git clone https://github.com/usuario/android_contaminacion.git
cd android_contaminacion


```kotlin
dependencies {
    implementation("androidx.appcompat:appcompat:1.4.0")
    implementation("com.google.android.material:material:1.4.0")
    implementation("androidx.activity:activity:1.4.0")
    implementation("androidx.constraintlayout:constraintlayout:2.1.2")
    implementation("com.squareup.retrofit2:retrofit:2.9.0")
    implementation("com.squareup.retrofit2:converter-gson:2.9.0")
}
