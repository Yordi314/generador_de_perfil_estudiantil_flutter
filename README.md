# Generador de Perfil Estudiantil 🎓

Una aplicación móvil interactiva desarrollada en Flutter que permite a los usuarios generar un carnet estudiantil digital y personalizado a través de un formulario dinámico.

## 📌 Características Principales
* **Formulario Interactivo:** Captura de datos en tiempo real (Nombre, Universidad, Carrera y Matrícula) mediante controladores de texto (`TextEditingController`).
* **Validación de Datos:** Uso de `GlobalKey<FormState>` para asegurar que ningún campo del formulario quede vacío antes de procesar la información.
* **Navegación Nativa (Routing):** Implementación de `Navigator.push` para transicionar de manera fluida entre la pantalla de captura de datos y la vista del carnet generado.
* **Diseño Modular:** Creación de widgets personalizados reutilizables (como `_buildTextField`) para mantener un código limpio (Clean Code) y fácil de mantener.

---

## 🏗️ Arquitectura de la Aplicación

El proyecto está estructurado en un solo archivo principal (`lib/main.dart`) dividido lógicamente en dos vistas principales:

### 1. `FormScreen` (Vista de Ingreso)
Un `StatefulWidget` encargado de manejar el estado del formulario. Contiene validaciones de campos obligatorios y gestiona el teclado del dispositivo (ocultándolo automáticamente al enviar el formulario). Al validar correctamente, pasa los argumentos a la siguiente ruta.

### 2. `ProfileCardScreen` (Vista de Visualización)
Un `StatelessWidget` que recibe los parámetros pasados desde el formulario a través de su constructor y renderiza un carnet estilizado utilizando los componentes de Material Design 3 (como `Card`, `CircleAvatar` y `ListTile` adaptados).

---

## 🚀 Cómo ejecutar el proyecto

Para probar esta aplicación en tu entorno local:

1. Asegúrate de tener el [SDK de Flutter](https://flutter.dev/docs/get-started/install) instalado en tu computadora.
2. Clona este repositorio o descarga el código fuente.
3. Abre una terminal en la raíz del proyecto y descarga las dependencias:
   ```bash
   flutter pub get
