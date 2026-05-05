# 🏋️ GymTracker — Forja tu Legado

GymTracker es una plataforma web minimalista diseñada para el seguimiento de la constancia deportiva. Combina una interfaz de estilo "Dark Sport" con un motor de Inteligencia Artificial que actúa como coach personal para evitar el absentismo y motivar al atleta.

## 👥 Equipo y Roles
*   **@Morritafriki**: Líder de Proyecto, Documentación y Diseño de Experiencia (UX).
*   **@ccarjim2909**: Especialista en Ciberseguridad (Auditoría de código y mitigación de riesgos).
*   **@joseeramirezzz**: Arquitectura Backend y Gestión de Servidores (Proxy API).
*   **@Pablo Malia Gil**: Ingeniería de Prompts (Personalidad y lógica del Coach IA).

---

## 🚀 ¿Qué hace la aplicación?
*   **Registro de Constancia**: Permite al usuario marcar sus días de entrenamiento y visualizar su racha actual.
*   **Coach Motivacional IA**: Genera consejos personalizados basados en la racha del usuario mediante una conexión segura con modelos de lenguaje.
*   **Gamificación Local**: Gestiona niveles y puntos de forma persistente en el navegador del usuario.
*   **Protección de Datos**: Implementa una capa de seguridad para evitar la manipulación de progresos.

## 🛑 ¿Qué NO hace?
*   **Base de Datos Centralizada**: No utiliza SQL; los datos se guardan en el `localStorage` del navegador (se pierden si se limpia la caché).
*   **Multiusuario**: Está diseñada para un perfil único por dispositivo.
*   **Seguimiento por GPS**: La actividad se registra de forma manual, no mediante sensores del móvil.

---

## 🛡️ Criterios de Seguridad Aplicados
Tras la auditoría interna, el proyecto cumple con los siguientes estándares de seguridad:

1.  **Prevención de XSS (Cross-Site Scripting)**: Se ha eliminado el uso de `innerHTML` en el renderizado de datos dinámicos, sustituyéndolo por `textContent` y funciones de sanitización de cadenas.
2.  **Seguridad de API (Zero-Exposure)**: La API Key nunca reside en el cliente. Se utiliza un servidor proxy en Node.js que gestiona las credenciales mediante variables de entorno (`.env`).
3.  **Integridad de LocalStorage**: Los datos se almacenan bajo una capa de **ofuscación Base64** para dificultar la manipulación de valores (puntos/rachas) desde la consola del desarrollador.
4.  **Content Security Policy (CSP)**: Se incluye una directiva de seguridad en el encabezado para restringir la carga de scripts externos no autorizados.

---

## 📥 Ejemplos de Input y Output

### 1. Registro de Sesión
*   **Input**: El usuario pulsa el botón "REGISTRAR SESIÓN".
*   **Output**: La interfaz se actualiza instantáneamente: *"Racha actual: 5 días"*. Internamente, el valor se guarda codificado.

### 2. Consulta al Coach IA
*   **Input**: Petición de consejo con una racha de 0 días.
*   **Acción**: El servidor envía el contexto de racha al modelo de IA.
*   **Output**: *"El éxito es la suma de pequeños esfuerzos repetidos día tras día. ¡Empieza hoy con 15 minutos!"*

---

## 🎯 Criterios de Aceptación Técnicos
*   **Nomenclatura**: Todo el código (IDs, clases, funciones y variables) sigue el estándar de nombres en **español**.
*   **Responsive**: La interfaz es adaptable a dispositivos móviles y escritorio.
*   **Optimización**: El frontend es una SPA (Single Page Application) ligera y de carga rápida.

---
*Proyecto final realizado para el curso de Desarrollo Web e IA — Mayo 2026*