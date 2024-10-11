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

```kotlin
dependencies {
    implementation("androidx.appcompat:appcompat:1.4.0")
    implementation("com.google.android.material:material:1.4.0")
    implementation("androidx.activity:activity:1.4.0")
    implementation("androidx.constraintlayout:constraintlayout:2.1.2")
    implementation("com.squareup.retrofit2:retrofit:2.9.0")
    implementation("com.squareup.retrofit2:converter-gson:2.9.0")
}
