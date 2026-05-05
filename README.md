# 🏋️ GymTracker — Forja tu Legado

Este proyecto es una aplicación web de una sola página (SPA) diseñada para la gestión de actividad física y motivación personalizada mediante Inteligencia Artificial. Permite a los usuarios registrar sus entrenamientos, visualizar su progreso mediante un sistema de niveles y puntos, y recibir consejos motivacionales.

## 👥 Equipo y Roles
*   **@Morritafriki**: Líder de Proyecto, Documentación y Presentación.
*   **@ccarjim2909**: Seguridad (Gestión de variables de entorno y protección de API Keys).
*   **@joseeramirezzz**: DevOps y Desarrollo Backend (Servidor Proxy en Node.js).
*   **@Pablo Malia Gil**: Prompt Engineering (Lógica y personalidad del Coach IA).

---

## 🚀 ¿Qué hace la aplicación?
*   **Registro de Actividad**: Permite seleccionar distintos tipos de ejercicios (Running, Pesas, HIIT, etc.) y registrar el tiempo invertido.
*   **Sistema de Gamificación**: Calcula puntos basados en el tipo de ejercicio y la duración, permitiendo al usuario subir de nivel (desde "Novato" hasta "Leyenda").
*   **Ranking Global**: Clasifica a los usuarios según su puntuación total para fomentar la competitividad sana.
*   **Historial Local**: Almacena las últimas sesiones realizadas directamente en el navegador.
*   **Coach Motivacional IA**: Genera consejos personalizados según la racha y el esfuerzo del usuario.
*   **Sistema de Alerta**: Detecta si el usuario lleva más de 7 días sin entrenar y muestra un aviso visual de "absentismo".

## 🛑 ¿Qué NO hace?
*   **Persistencia en Base de Datos**: Los datos se guardan en el `localStorage` del navegador; si se borra la caché o se cambia de dispositivo, los datos se reinician.
*   **Autenticación Multidispositivo**: No requiere registro con correo o contraseña, se basa en un perfil de usuario local.
*   **Sincronización en Tiempo Real**: El ranking es una simulación basada en datos locales y usuarios de demostración.

---

## 🎯 Criterios de Aceptación
1.  **Seguridad de API**: La API Key de la IA nunca se expone en el código cliente (Frontend). Todas las llamadas pasan por un servidor seguro.
2.  **Nomenclatura Estándar**: Todas las variables, IDs, clases CSS y funciones de JavaScript utilizan nombres en **español**.
3.  **Interfaz Responsiva**: La web es totalmente funcional tanto en dispositivos móviles como en ordenadores.
4.  **Optimización de Archivos**: Proyecto ejecutado en una única página HTML y un único servidor compartido.

---

## 📥 Ejemplos de Input / Output

### 1. Registro de Entrenamiento
*   **Input (Entrada)**: Selección de "HIIT" (multiplicador x5) + Duración: 20 minutos.
*   **Acción**: El usuario pulsa "Registrar Sesión".
*   **Output (Salida)**: Se suman 100 puntos al perfil, la barra de nivel progresa y aparece un "Toast" de éxito con el mensaje "¡SESIÓN REGISTRADA! 💥".

### 2. Consulta al Coach IA
*   **Input (Entrada)**: El sistema detecta una racha de 0 días (usuario inactivo).
*   **Acción**: El usuario pulsa "Obtener Consejo del Coach".
*   **Output (Salida)**: "El primer paso es el más difícil, Atleta. Ponte las zapatillas y solo camina 10 minutos hoy. ¡Mañana me lo agradecerás!"

---

## ⚙️ Instalación y Uso Local
1. Clonar el repositorio: `git clone https://github.com/Morritafriki/PROYECTO-DESARROLLO-IA.git`
2. Instalar dependencias: `npm install`
3. Configurar el archivo `.env` con la `API_KEY` correspondiente.
4. Iniciar el servidor: `node servidor.js`
5. Abrir `http://localhost:3000` en el navegador.