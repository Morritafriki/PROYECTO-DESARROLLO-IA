# 🏋️ GymTracker — Forja tu Legado

GymTracker es una aplicación web (SPA) diseñada para la gestión del rendimiento deportivo, integrando una interfaz de alta visibilidad y un motor de Inteligencia Artificial para la motivación del usuario.

## 👥 Equipo y Roles
*   **@Morritafriki**: Presentación del Proyecto, Gestión de Documentación y Control de Calidad.
*   **@joseeramirezzz**: Arquitectura de Sistemas. Responsable de la reestructuración del núcleo de la página y la supervision de los prompts.
*   **@ccarjim2909**: Auditoría de Seguridad y detección de vulnerabilidades (XSS).
*   **@Pablo Malia Gil**: Lógica de Entrenamiento y Experiencia de Usuario.

---

## 🚀 ¿Qué hace la aplicación?
*   **Registro de Constancia**: Permite marcar los días de entrenamiento y visualizar la racha actual.
*   **Coach Motivacional IA**: Genera consejos personalizados basados en la racha del usuario mediante prompts optimizados.
*   **Gamificación Local**: Gestiona un sistema de puntos y niveles para incentivar el uso diario.
*   **Seguridad de Datos**: Protege la integridad de la racha mediante procesos de ofuscación.

## 🛑 ¿Qué NO hace la aplicación?
*   **Persistencia en la Nube**: No utiliza bases de datos externas; los datos se pierden al limpiar la caché del navegador.
*   **Sincronización Multidispositivo**: Los datos son exclusivos del dispositivo donde se registraron.
*   **Arquitectura Modular**: Por limitaciones de tiempo, el código no está dividido en subcarpetas, manteniéndose en una estructura monolítica funcional.

---

## 📥 Ejemplos de Input y Output

| Acción | Input (Entrada de usuario) | Output (Resultado en pantalla) |
| :--- | :--- | :--- |
| **Registrar Sesión** | Clic en botón "REGISTRAR" | Actualización de racha: "5 días". |
| **Solicitar Consejo** | Petición con racha de 2 días | *"¡No te detengas ahora! El tercer día es el que marca la diferencia."* |
| **Guardado de Datos** | Progreso del usuario | String codificado en Base64 en LocalStorage. |

---

## 🎯 Criterios de Aceptación Cumplidos
*   **Nomenclatura**: Todo el código (IDs, clases, funciones) utiliza nombres en **español**.
*   **Seguridad XSS**: Uso de `textContent` para neutralizar inyecciones de código malicioso.
*   **Precisión de IA**: Prompts ajustados para dar respuestas directas, evitando textos irrelevantes o excesivamente largos.
*   **Diseño Responsive**: Interfaz adaptada para su uso en dispositivos móviles durante el entrenamiento.

---
*Documentación oficial preparada por Stefany para el examen de Desarrollo Web e IA — 2026*