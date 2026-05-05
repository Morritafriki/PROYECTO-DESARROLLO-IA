# 🏋️ GymTracker — Forja tu Legado

GymTracker es una aplicación web (SPA) diseñada para optimizar la constancia deportiva mediante gamificación e Inteligencia Artificial. Este proyecto destaca por una arquitectura segura, una documentación técnica exhaustiva y una interfaz orientada al rendimiento.

## 👥 Equipo y Roles
*   **@Morritafriki (Stefany)**: Presentación del Proyecto y Gestión de Documentación Técnica.
*   **@ccarjim2909**: Auditoría de Seguridad y Mitigación de Riesgos.
*   **@joseeramirezzz**: Desarrollo Backend y Arquitectura de Servidor Proxy.
*   **@Pablo Malia Gil**: Ingeniería de Prompts y Lógica del Coach IA.

---

## 🚀 Funcionalidades Principales
*   **Gestión de Rachas**: Sistema de seguimiento de días consecutivos de entrenamiento.
*   **Coach Motivacional**: Integración con IA para generar consejos personalizados basados en el estado del usuario.
*   **Sistema de Gamificación**: Asignación de puntos y niveles para fomentar la retención del usuario.
*   **Persistencia Local**: Almacenamiento de datos en el navegador para una carga inmediata.

## 🛡️ Estándares de Seguridad y Calidad
Como parte de la gestión de calidad y documentación, se han certificado los siguientes puntos:

1.  **Protección contra XSS**: Se ha auditado el código para eliminar el uso de `innerHTML`, sustituyéndolo por `textContent` y procesos de **sanitización** de datos para prevenir inyecciones maliciosas.
2.  **Seguridad de Credenciales**: La arquitectura utiliza un **Servidor Proxy** en Node.js. Esto garantiza que la API Key de la IA se gestione mediante variables de entorno (`.env`), evitando su exposición en el lado del cliente.
3.  **Integridad de Datos**: Los progresos del usuario en el `localStorage` están protegidos mediante **ofuscación Base64**, dificultando la alteración manual de puntos o rachas.
4.  **Nomenclatura Estandarizada**: Todo el proyecto (IDs, clases, funciones y variables) sigue una convención de nombres en **español** para garantizar la legibilidad y el mantenimiento profesional.

---

## 📥 Ejemplos de Uso (Input/Output)

| Acción | Input (Entrada) | Output (Salida) |
| :--- | :--- | :--- |
| **Registrar Sesión** | Clic en "Registrar" | Incremento de racha y actualización de nivel en UI. |
| **Consultar Coach** | Racha de 0 días | *"El primer paso es el más difícil. ¡Empieza hoy!"* |
| **Almacenamiento** | Datos de usuario | String ofuscado en LocalStorage (Seguridad). |

---

## 🛑 Limitaciones y Alcance
*   **Ámbito Local**: Los datos se almacenan por dispositivo; no hay sincronización entre diferentes navegadores.
*   **Dependencia de API**: El funcionamiento del Coach IA requiere conexión activa a internet y configuración del servidor proxy.

---
*Documentación preparada por Stefany para el examen de Desarrollo Web e IA — 2026*