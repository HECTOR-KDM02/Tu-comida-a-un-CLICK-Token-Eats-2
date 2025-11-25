
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

-  Instalación y configuración del entorno Soroban en WSL/Ubuntu.  
-  Definición del objetivo general y funcionalidad principal de TokenEats.  
-  Creación del repositorio GitHub y estructura básica del proyecto (`/contracts`, `/webapp`, `/docs`).  
-  Diseño inicial del flujo de compra: seleccionar producto → confirmar → pagar con Freighter.  
-  Borrador del contrato inteligente de **escrow** para pagos entre cliente y comercio.

**Semáforo de tareas completadas:** 🟢 

*(Elegir el color que mejor represente si las tareas críticas se cumplieron a tiempo.)*

---

### 3. Tareas en Proceso

-  Implementación del contrato Soroban (funciones de crear, liberar y reembolsar pagos).  
-  Desarrollo de la interfaz web para seleccionar productos y enviar la orden.  
-  Integración de la wallet Freighter para autenticar usuarios (SEP-10) y firmar transacciones.  
-  Pruebas funcionales básicas del flujo “crear pedido → pagar → ver estado”.  
-  Documentación de la guía de demo para el profesor.

**Semáforo de tareas en proceso:** 🟢  

---

### 4. Obstáculos / Riesgos

-  Dudas en funciones avanzadas de Soroban (autorizaciones, almacenamiento, eventos).  
-  Errores intermitentes en Freighter al firmar algunas transacciones de prueba.  
-  Falta de tiempo para integrar pruebas E2E y accesibilidad en la misma semana.  

**Semáforo de riesgos:** 🟢

**Comentario / Apoyo requerido:**  
>  “Se requiere apoyo del profesor para revisar el diseño del contrato de escrow y validar buenas prácticas.”

---

### 5. Actividades Planificadas para la Próxima Semana

-  Completar las pruebas unitarias del contrato Soroban (escrow y casos de timeout).  
-  Ajustar la interfaz de pago para hacer más claro el uso de la wallet.  
-  Realizar la primera simulación completa: crear pedido → pagar USDC → liberar/refund.  
-  Elaborar un video corto de demostración para subir como evidencia al repositorio GitHub.

---

### 6. Necesidades / Solicitudes para el Cliente (Profesor)

- Revisión del contrato inteligente para validar la estructura de funciones y eventos.  
- Asesoría breve sobre el manejo de wallets en entornos de prueba Stellar (Freighter/Testnet).  
- Aprobación y retroalimentación del **formato de informe semanal** para continuar usándolo como estándar.

---

## 5.2 Informe Semanal de Avances 

**Proyecto:** Token Eats – *Tu comida a un click*  
**Semana:** del 17/11/2025 al 21/11/2025  
**Equipo:**  
- Oliverio Rojas Sánchez  
- Josue Ángel García Aparicio  
- Héctor Eduardo Santiago Bautista  

---

### 1. Objetivo de la semana

Durante esta semana el objetivo principal fue **formalizar el inicio del proyecto Token Eats**, definiendo claramente el alcance, los roles del equipo, los objetivos generales y específicos, así como los recursos y herramientas que se utilizarán durante el desarrollo. Además, se buscó alinear a todos los integrantes en una misma visión del producto.

---

### 2. Actividades realizadas

1. **Sesión de lluvia de ideas (brainstorming)**  
   - Fecha: 05/09/2025  
   - Se identificaron las principales necesidades del restaurante y de los usuarios finales.  
   - Se definió el concepto central de la plataforma: pedidos y pagos en línea de forma rápida, segura y sencilla.  
   - Se discutieron posibles módulos: gestión de menú, pedidos, pagos, notificaciones y panel administrativo.

2. **Redacción del Acta de Constitución del Proyecto**  
   - Fecha: 07/09/2025  
   - Se estableció oficialmente el **título del proyecto**: *Token Eats – Tu comida a un click*.  
   - Se definió el **objetivo general** y los **objetivos específicos** del proyecto.  
   - Se delimitó el **alcance**: qué incluye y qué queda excluido en esta primera fase (por ejemplo, se aclaró que no se desarrollará un sistema propio de delivery ni un programa avanzado de fidelización en esta etapa).  

3. **Asignación de roles y responsabilidades**  
   - Se definieron los siguientes roles:  
     - **Líder del proyecto y Backend Developer:** Oliverio Rojas Sánchez.  
     - **Frontend/App Developer:** Josue Ángel García Aparicio.  
     - **Analista de requerimientos y QA/Tester:** Héctor Eduardo Santiago Bautista.  
   - Se describieron las funciones principales de cada rol para evitar ambigüedades y facilitar la coordinación.

4. **Definición preliminar del stack tecnológico y recursos**  
   - Se acordó utilizar:  
     - **Frontend:** Vue.js y/o React Native según el alcance.  
     - **Backend:** Spring Boot.  
     - **Base de datos:** MySQL.  
   - Se definió el uso de:  
     - **GitHub** para control de versiones y documentación.  
     - **GitHub Projects/Trello** como tablero Kanban para la gestión de tareas.  

5. **Planeación inicial mediante hitos**  
   - Se establecieron los hitos y fechas estimadas:  
     - Sesión de lluvia de ideas.  
     - Elaboración del acta de constitución.  
     - Diseño de prototipo funcional (wireframes).  
     - Desarrollo de versión beta.  
     - Pruebas de calidad (QA).  
     - Presentación final del proyecto.  

---

### 3. Avances respecto al cronograma

- ✅ **Sesión de lluvia de ideas:** Cumplida en la fecha prevista (05/09/2025).  
- ✅ **Redacción del Acta de Constitución:** Finalizada el 07/09/2025, de acuerdo al cronograma.  
- ✅ **Definición de roles y stack tecnológico:** Completada en esta semana, permitiendo iniciar formalmente la planeación técnica.  
- ⏳ **Diseño de prototipo funcional (wireframes):** Programado para la siguiente semana, aún no iniciado.  

En general, los avances de esta semana se encuentran **alineados con el plan establecido** y se ha logrado una base sólida para continuar con el diseño de la solución.

---

### 4. Dificultades y riesgos identificados

- **Disponibilidad de tiempo de los integrantes:**  
  La coordinación de horarios entre los miembros del equipo puede afectar el ritmo de trabajo si no se mantiene una buena organización.

- **Dependencia de la información del restaurante:**  
  Se identificó que para avanzar en el diseño del menú y el flujo de pedidos será necesario contar con información actualizada por parte del restaurante (productos, precios, tiempos estimados, etc.). Cualquier retraso en esa información podría afectar el avance de las siguientes fases.

- **Alcance futuro del sistema de fidelización:**  
  Aunque en esta primera fase solo se “sientan las bases” para un sistema de recompensas digitales, se considera un punto a tomar en cuenta para no limitar el diseño actual.

---

### 5. Plan de trabajo para la próxima semana

Para la siguiente semana se tiene planeado:

1. **Diseño de prototipos (wireframes) de la aplicación**  
   - Pantallas principales del cliente:  
     - Inicio / Login  
     - Menú de productos  
     - Detalle de producto  
     - Carrito de compra y pago  
     - Seguimiento de pedido  
   - Pantallas del panel administrativo:  
     - Inicio de sesión del administrador  
     - Gestión de menú  
     - Visualización y gestión de pedidos  

2. **Levantamiento más detallado de requerimientos**  
   - Reunión (real o simulada) con el “cliente” (restaurante) para aclarar:  
     - Flujo real del proceso de pedido.  
     - Información necesaria para cada pantalla.  
     - Restricciones o políticas del negocio (horarios, tipos de pago, etc.).  

3. **Creación y organización del tablero Kanban**  
   - Registrar tareas en GitHub Projects o Trello.  
   - Asignar responsables y fechas tentativas por actividad.  

4. **Estructura inicial del repositorio en GitHub**  
   - Crear la estructura del proyecto (carpetas para backend, frontend y documentación).  
   - Subir el README con la información base del proyecto.

---

### 6. Conclusiones

La semana fue **productiva y clave para el arranque del proyecto**, ya que se logró:

- Definir claramente la misión del proyecto Token Eats.  
- Formalizar el acta de constitución con objetivos, alcance y recursos.  
- Establecer roles, responsabilidades y herramientas de trabajo.  
- Alinear expectativas entre los integrantes del equipo.

Con estos elementos, el proyecto cuenta con una **base sólida de organización y planeación**, lo cual permitirá avanzar a la siguiente fase: el diseño de la interfaz y la definición detallada de requerimientos funcionales y no funcionales.

---

## 6. Calendario de Reuniones

A continuación se presenta un **calendario base de reuniones** para mantener una comunicación constante y ordenada durante el desarrollo de TokenEats.

### 6.1 Reuniones Periódicas

| Tipo de reunión                  | Objetivo principal                                          | Frecuencia              | Día / Hora aproximada      | Modalidad        | Participantes principales                      |
|----------------------------------|-------------------------------------------------------------|-------------------------|----------------------------|------------------|-----------------------------------------------|
| Reunión de planeación semanal    | Definir tareas de la semana, asignar responsables.         | 1 vez por semana        | Lunes, 18:00–19:00         | Meet / Presencial| Todo el equipo                                |
| Reunión de seguimiento intermedio| Revisar avances, bloquear problemas, ajustar prioridades.  | 1 vez por semana        | Jueves, 18:00–18:30        | Meet             | Todo el equipo                                |
| Reunión de retrospectiva         | Analizar qué salió bien/mal y qué mejorar.                 | Cada 2 semanas          | Viernes, 18:00–19:00       | Meet / Presencial| Todo el equipo                                |
| Reunión con el profesor (cliente)| Presentar avances formales, resolver dudas y recibir feedback.| Según agenda de la materia | Según indicaciones del profesor | Meet / Aula | Líder de proyecto + quien el profesor indique |

### 6.2 Reglas para las Reuniones

- La **convocatoria** se realizará por el grupo de **WhatsApp** con al menos 24 horas de anticipación.  
- El **Líder de Proyecto** levantará una pequeña minuta (acuerdos y tareas) y la guardará en el repositorio (`/docs/minutas/`).  
- Cualquier reunión extraordinaria (por problemas urgentes o cambios de alcance) deberá:
  - Ser notificada en WhatsApp.  
  - Dejar registro del acuerdo en GitHub (Issue o documento).  

---
```
