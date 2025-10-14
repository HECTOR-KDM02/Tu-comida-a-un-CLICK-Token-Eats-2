# 🧭 Manifiesto de Viabilidad del Proyecto — **TokenEats**
**Proyecto:** *TokenEats – Tu comida a un clic*  
**Stack Web3.0/Stellar:** Soroban (contratos), USDC en Stellar, SEP-10 (WebAuth), SEP-24 (on/off-ramp), Freighter (wallet), Horizon/RPC  

---

## 1) 🎯 Resumen Ejecutivo
**TokenEats** es un MVP de pedidos y pagos para restaurantes que opera sobre **Stellar Testnet**. El flujo clave es: el cliente realiza un pedido, paga con **USDC en Stellar**, los fondos quedan en **escrow on-chain** mediante un contrato **Soroban** y se liberan al comercio tras la confirmación de entrega. El objetivo es demostrar **rapidez, transparencia y seguridad** con costos mínimos, preparando el terreno para recompensas tokenizadas en una fase posterior.

**Objetivo SMART:** En **6 semanas** entregar un prototipo funcional con registro/autenticación vía **SEP-10**, pago USDC con **escrow Soroban**, panel simple de pedidos y notificaciones de confirmación on-chain, documentado y operando en **Testnet**.

---

## 2) 📦 Alcance del MVP
Incluye aplicación web responsive (checkout, pago y recibo on-chain), panel básico para el restaurante (órdenes/estados), contrato Soroban de **escrow** (crear, liberar, reembolsar con timeout), autenticación **SEP-10**, integración con **Freighter** y notificaciones tras `tx_successful`.  
Quedan fuera de esta fase: delivery propio, fidelización avanzada (solo *base técnica* del token de recompensas), pasarelas fiat nativas (se usará **SEP-24** con anchor de prueba cuando aplique).

---

## 3) 🧱 Arquitectura y Stack
**Front/App:** React (Vite) con conexión de wallet **Freighter** y flujos SEP-10/24.  
**Back/API:** Gateway ligero para orquestar órdenes, escuchar Horizon y emitir notificaciones.  
**On-chain:** Contrato **Soroban** para **escrow** con eventos `EscrowCreated`, `Released`, `Refunded`, política de timeout y soporte para *fee bump*.  
**Infra de pruebas:** **Stellar Testnet/Futurenet**, **soroban-cli** y **Horizon/RPC**.  
**Seguridad:** Firma en cliente (nunca llaves privadas en el backend), validación de `stellar.toml` y dominios, límites por pedido/activo.

---

## 4) 🔍 Viabilidad 360°
### 4.1 Técnica  
**Viable** con los recursos actuales. Los principales retos son la correcta implementación del **escrow Soroban** y los flujos **SEP-10/24**. Se mitigará con una primera iteración enfocada en **escrow + pago** y pruebas automatizadas del contrato.  
**Recursos clave:** soroban-cli, ejemplos oficiales, repositorio GitHub, CI básico (lint/tests/coverage), Figma para UI.

### 4.2 Operativa  
Equipo reducido con roles definidos y coordinación por GitHub Projects. Flujo de trabajo **GitFlow ligero** (feature → PR → tests/coverage → merge a `develop` → staging Testnet). Reuniones breves semanales y *issues* con criterios de aceptación y definición de terminado (DoD).

### 4.3 Económica  
**Presupuesto MVP:** **$1,525 USD** por **50 h** (incluye margen 10%). Se apoya en herramientas *free-tier* y costos de red **muy bajos** en Stellar. El modelo de ingresos propuesto (comisiones micro, planes premium y marketplace) sostiene la operación sin depender solo de patrocinios.

---

## 5) 👥 Organización (roles reales del equipo)
| Rol | Responsable | Funciones |
|---|---|---|
| Líder del Proyecto | **Oliverio Rojas Sanchez** | Plan, coordinación, CI básico, documentación |
| Backend (Soroban/API) | **Oliverio Rojas Sanchez** | Contrato `escrow`, API gateway, integraciones |
| Front/App | **Josue Angel Garcia Aparicio** | UI/UX en React, wallet connect, checkout |
| Analista/QA | **Hector Eduardo Santiago Bautista** | Requerimientos, pruebas funcionales y regresión |

> RACI de calidad alineado al *Plan de Calidad — SCF (Stellar Only)* incluido en el repositorio.

---

## 6) 🗓️ Hitos y cronograma base
- Lluvia de ideas: **05/09/2025**  
- Acta de constitución: **07/09/2025**  
- Prototipo UI (wireframes): **15/09/2025**  
- Versión **beta** (escrow + pago Testnet): **01/10/2025**  
- QA y smoke tests: **15/10/2025**  
- Presentación del MVP: **30/10/2025**

---

## 7) 💰 Presupuesto del MVP (resumen)
**Total estimado:** **$1,525 USD** (50 h).  
Desglose principal: contrato Soroban (10 h), frontend web + wallet (8 h), API gateway (6 h), CI básico (3 h), QA/usabilidad (8 h), diseño (6 h), documentación (3 h).  
**Metodología:** planning poker + consenso; etiquetas de costo por *issue* en GitHub; *BUDGET.md* con evidencias (hash/tx en Testnet).

---

## 8) 📈 Calidad y Métricas (línea base)
- **Cobertura de pruebas (contrato+back+front):** ≥ **80%**  
- **p95 confirmación de pago:** ≤ **10 s** (submit → `tx_successful`)  
- **Éxito de tx:** ≥ **98%** (excluye saldo insuficiente)  
- **Accesibilidad web:** ≥ **90** (Lighthouse/axe)  
- **Uptime backend:** ≥ **99.5%**  
- **Satisfacción UAT:** ≥ **4.2/5**  
Procedimientos: ADRs para decisiones on-chain, *gate* manual a Testnet/Mainnet, smoke/E2E del flujo “crear pedido → pagar USDC → release/refund”.

---

## 9) 💼 Modelo de Ingresos (MVP→Fase 2)
- **Comisión micro (1–2%)** por transacción/retirada del e
