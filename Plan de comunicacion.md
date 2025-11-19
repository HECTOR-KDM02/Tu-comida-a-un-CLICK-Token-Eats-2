# 📡 Plan de Comunicación del Equipo – **TokenEats**  
## Actividad: “Los Canales de la Constelación”  
### Unidad CASE — Comunicación y Colaboración Profesional  

---

## 1. Propósito del Plan de Comunicación

El propósito de este documento es establecer los **canales de comunicación**, el **formato de informe de progreso semanal** y las **herramientas de colaboración** que el equipo empleará durante el desarrollo del proyecto **TokenEats – Tu comida a un clic**.

Este plan busca garantizar:

- Comunicación **clara y oportuna** entre todos los integrantes.  
- **Transparencia** en el seguimiento del avance del proyecto.  
- Justificación **profesional** del uso de herramientas digitales.  
- Una dinámica fluida con el **profesor (cliente)** y con otros equipos del ecosistema de trabajo de la unidad CASE.

---

## 2. Roles de Comunicación

| Rol                      | Integrante                              | Responsabilidad de Comunicación Principal                            |
|--------------------------|-----------------------------------------|------------------------------------------------------------------------|
| Líder de Proyecto        | **Oliverio Rojas Sánchez**              | Convocar reuniones, consolidar informes semanales y hablar con el profesor. |
| Responsable Front/UX     | **Josue Ángel García Aparicio**         | Comunicar avances/dudas de interfaz, experiencia de usuario y demo.   |
| Responsable QA/Análisis  | **Héctor Eduardo Santiago Bautista**    | Reportar resultados de pruebas, riesgos y propuestas de mejora.       |

> Nota: Todos los integrantes son responsables de revisar diariamente los canales acordados (WhatsApp, GitHub, Classroom u otro).

---

## 3. Canales de la Constelación (Canales Oficiales de Comunicación)

| Canal / Herramienta      | Uso Principal                                             | Frecuencia / Acuerdo                        |
|--------------------------|-----------------------------------------------------------|---------------------------------------------|
| **WhatsApp (grupo)**     | Coordinación rápida, avisos urgentes, recordatorios.      | Revisión diaria. Respuesta ideal: ≤ 12 h.   |
| **GitHub Issues**        | Registro de tareas, bugs, dudas técnicas, feedback.       | Actualización en cada cambio relevante.     |
| **GitHub Projects**      | Tablero Kanban de tareas (To Do / In Progress / Done).    | Actualización mínima: 3 veces por semana.   |
| **Reuniones presenciales / Meet** | Planeación semanal, retrospectivas, decisiones clave. | 1 reunión fija semanal + las necesarias.    |
| **Google Classroom / Plataforma del profesor** | Entrega de actividades oficiales, comunicación formal con el docente. | Según fechas marcadas por la materia. |
| **Correo institucional** | Comunicación formal (solo si el profesor lo solicita).    | Uso ocasional.                              |

---

## 4. Reglas de Comunicación

1. **Respeto y claridad:**  
   - Evitar mensajes ambiguos; usar contexto (enlaces a issues, capturas, etc.).  
   - Trato respetuoso en todo momento.

2. **Compromiso con la respuesta:**  
   - Se espera que los integrantes respondan a mensajes importantes en un lapso **no mayor a 24 horas** en días hábiles.

3. **Uso correcto de canales:**  
   - Dudas técnicas → GitHub Issue.  
   - Organización rápida/logística → WhatsApp.  
   - Entregas para el profesor → Classroom o repositorio GitHub, según se indique.

4. **Registro de decisiones:**  
   - Las decisiones técnicas clave se documentarán en un archivo como `DECISIONES.md` o en Issues etiquetados como `decision`.

---

# 5. Formato de Informe Semanal (“Bitácora de Vuelo”)

A continuación se presenta el **formato acordado** para el informe de progreso semanal, siguiendo la idea del **“Tablero de Control del Progreso”** y el **“Código de los Semáforos”**.

> Este formato se llenará **una vez por semana** y se almacenará, por ejemplo, en `reports/SEMANA_X.md` dentro del repositorio.

---

## 5.1 Formato del Informe

### Informe Semanal de Progreso — Semana X  
**Proyecto:** TokenEats – Tu comida a un clic  
**Periodo:** DD/MM/AAAA – DD/MM/AAAA  
**Responsable del informe:** Nombre del integrante

---

### 1. Estado General del Proyecto

**Semáforo general (seleccionar uno):**  
🟢 Todo avanza según lo planeado  
🟡 Riesgo moderado o retraso potencial  
🔴 Problema crítico que bloquea el avance  

**Comentario breve:**  
> Ejemplo: “Se completó el primer flujo de pago en Testnet, pero faltan pruebas de regresión.”

---

### 2. Tareas Completadas

- [Ejemplo] Instalación y configuración del entorno Soroban en WSL/Ubuntu.  
- [Ejemplo] Definición del objetivo general y funcionalidad principal de TokenEats.  
- [Ejemplo] Creación del repositorio GitHub y estructura básica del proyecto (`/contracts`, `/webapp`, `/docs`).  
- [Ejemplo] Diseño inicial del flujo de compra: seleccionar producto → confirmar → pagar con Freighter.  
- [Ejemplo] Borrador del contrato inteligente de **escrow** para pagos entre cliente y comercio.

**Semáforo de tareas completadas:** 🟢 / 🟡 / 🔴  

*(Elegir el color que mejor represente si las tareas críticas se cumplieron a tiempo.)*

---

### 3. Tareas en Proceso

- [Ejemplo] Implementación del contrato Soroban (funciones de crear, liberar y reembolsar pagos).  
- [Ejemplo] Desarrollo de la interfaz web para seleccionar productos y enviar la orden.  
- [Ejemplo] Integración de la wallet Freighter para autenticar usuarios (SEP-10) y firmar transacciones.  
- [Ejemplo] Pruebas funcionales básicas del flujo “crear pedido → pagar → ver estado”.  
- [Ejemplo] Documentación de la guía de demo para el profesor.

**Semáforo de tareas en proceso:** 🟢 / 🟡 / 🔴  

*(Si hay riesgo de no terminar algunas en la semana, usar 🟡 o 🔴.)*

---

### 4. Obstáculos / Riesgos

- [Ejemplo] Dudas en funciones avanzadas de Soroban (autorizaciones, almacenamiento, eventos).  
- [Ejemplo] Errores intermitentes en Freighter al firmar algunas transacciones de prueba.  
- [Ejemplo] Falta de tiempo para integrar pruebas E2E y accesibilidad en la misma semana.  

**Semáforo de riesgos:** 🟢 / 🟡 / 🔴  

**Comentario / Apoyo requerido:**  
> Ejemplo: “Se requiere apoyo del profesor para revisar el diseño del contrato de escrow y validar buenas prácticas.”

---

### 5. Actividades Planificadas para la Próxima Semana

- [Ejemplo] Completar las pruebas unitarias del contrato Soroban (escrow y casos de timeout).  
- [Ejemplo] Ajustar la interfaz de pago para hacer más claro el uso de la wallet.  
- [Ejemplo] Realizar la primera simulación completa: crear pedido → pagar USDC → liberar/refund.  
- [Ejemplo] Elaborar un video corto de demostración para subir como evidencia al repositorio GitHub.

---

### 6. Necesidades / Solicitudes para el Cliente (Profesor)

- Revisión del contrato inteligente para validar la estructura de funciones y eventos.  
- Asesoría breve sobre el manejo de wallets en entornos de prueba Stellar (Freighter/Testnet).  
- Aprobación y retroalimentación del **formato de informe semanal** para continuar usándolo como estándar.

---

## 6. Calendario de Reuniones
