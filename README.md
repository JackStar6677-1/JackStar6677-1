<p align="center">
  <img src="./assets/jackstar-orbit.svg" width="100%" alt="JackStar — producción, infraestructura y arquitectura de software" />
</p>

<div align="center">

# JackStar

### Ingeniero en Informática · Operador de Infraestructura · Arquitecto de Software

[![StarSuites](https://img.shields.io/badge/StarSuites-Monorepo_LTS-8B5CF6?style=for-the-badge&logo=github&logoColor=white)](https://github.com/DrakesCraft-Labs/Drakes-Suites)
[![DrakesCraft](https://img.shields.io/badge/DrakesCraft-Producción-22C55E?style=for-the-badge&logo=minecraft&logoColor=white)](https://web.drakescraft.cl)
[![SAORI Core](https://img.shields.io/badge/SAORI-SRE_Engine-8B5CF6?style=for-the-badge)](https://github.com/JackStar6677-1/saori)
[![Java 21](https://img.shields.io/badge/Java-21_LTS-F59E0B?style=for-the-badge&logo=openjdk&logoColor=white)](https://openjdk.org/)
[![Rust](https://img.shields.io/badge/Rust-Off--Heap_FFM-DEA584?style=for-the-badge&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![SRE Triad](https://img.shields.io/badge/SRE_Triad-Antigravity_·_Codex_·_Claude-06B6D4?style=for-the-badge)](https://github.com/JackStar6677-1)

[DrakesCraft Labs](https://github.com/DrakesCraft-Labs) ·
[Proyectos](https://github.com/JackStar6677-1?tab=repositories) ·
[DrakesCraft](https://web.drakescraft.cl)

</div>

---

Construyo, administro y blindo infraestructura donde el software convive con la realidad: alta concurrencia, bases de datos transaccionales, entornos educativos, clústeres físicos de servidores (**Star, Nexus, Nova**) y agentes autónomos.

Mi trabajo se estructura alrededor de **tres pilares independientes y estrictamente delimitados**:

---

## 🏛️ Los Tres Pilares de Trabajo

### 1. 🏫 Tecnología Educativa e Infraestructura Institucional
Mi trabajo y ejercicio profesional en el mundo real está dedicado a la **ingeniería de TI educativa y administración de infraestructura**:
* **Redes y Administración de Campus:** Gestión integral de redes institucionales, salas de servidores, laboratorios de computación y flotas de estaciones de trabajo.
* **Plataformas y Portales Web:** Diseño y despliegue de sistemas internos de reservas de salas ([**CastelRoomKeeper**](https://github.com/JackStar6677-1/CastelRoomKeeper)), portales administrativos y herramientas de apoyo institucional.
* **Automatización de Aulas y Diagnóstico:** Scripts de administración de laboratorios ([**VeyonScripts**](https://github.com/JackStar6677-1/VeyonScripts)), monitoreo preventivo ([**CampusCare-Monitoring**](https://github.com/JackStar6677-1/CampusCare-Monitoring)) y flujos locales de credenciales.

### 2. ⭐ Star / JackStar: Arquitectura de Sistemas, IA Autónoma & StarSuites
Mi identidad personal soberana como arquitecto de software y operador de sistemas:
* **StarSuites Engine (`Drakes-Suites`):** Arquitectura monorepo multi-módulo que consolida y moderniza más de 180 micro-addons en mega-suites desacopladas con persistencia SQLite WAL, configuración modular granular (`modules/*.yml`) y aceleración nativa en Rust off-heap ([**Slimefun-Rust**](https://github.com/DrakesCraft-Labs/Slimefun-Rust)) para eliminar pausas de Garbage Collector.
  > ℹ️ **Reconocimiento Canónico Upstream:** Slimefun es una obra de código abierto creada originalmente por **TheBusyBiscuit** y la comunidad. Mi rol es el de **arquitecto de modernización y rescate**: portabilidad a Paper 1.21.11+ / Purpur 26.X, erradicación de cuellos de botella de tickers, memoria off-heap en Rust y unificación modular.
* **Star Engine (`drakes-server.jar`):** Evolución canónica del motor de servidor Odysseia a **Star**. Kernel unificado de servidor, telemetría Star, verificación idempotente de compras Tebex (`purchases.db`), vigilancia de economía macroeconómica (SII) y enlace nativo Rust (`Star-Rust`).
* **Suite Multiverse (por Chagui68):** Integración oficial de la Suite Multiverse (`drakes-multiverse.jar`), reconociendo la autoría y diseño soberano de mi colaborador **Chagui68** ([`MultiverseCreatures`](https://github.com/DrakesCraft-Labs/MultiverseCreatures) y [`MultiverseNets`](https://github.com/DrakesCraft-Labs/MultiverseNets)).
* **[SAORI Framework](https://github.com/JackStar6677-1/saori)** (*Server Autonomous Orchestrator for Resilient Infrastructure*): Framework SRE omnicanal que coordina la **Tríada Simétrica de IA** (Google Antigravity, OpenAI Codex, Claude Code) mediante inferencia local offline (Needle Tier 0) y cerrojos transaccionales en SQLite WAL.

### 3. 🐉 DrakesCraft: Red de Producción de Minecraft (Dallas, TX)
Red multijugador masiva en producción (Paper/Purpur 1.21.11 en TheGameHosting, Dallas, TX):
* **Arquitectura de Producción:** 5 modalidades aisladas (Survival, OneBlock, SkyBlock, Classic Vanilla, Laboratorio).
* **Motores Propios:** [**Star Engine / Odysseia**](https://github.com/DrakesCraft-Labs/Odysseia), [**DiosesDrakes**](https://github.com/DrakesCraft-Labs/DiosesDrakes), [**ArcanaDrakes**](https://github.com/DrakesCraft-Labs/ArcanaDrakes) y [**DrakesBosses**](https://github.com/DrakesCraft-Labs/DrakesBosses).
* **Forks Endurecidos:** [**BentoBox-Drake**](https://github.com/DrakesCraft-Labs/BentoBox-Drake) (parche crítico anti-pérdida de Data Components en Incidente #276), [**CrazyAuctions-Drake**](https://github.com/DrakesCraft-Labs/CrazyAuctions-Drake), [**AxGraves-Drakes**](https://github.com/DrakesCraft-Labs/AxGraves-Drakes) e [**InvSwitcher-Drake**](https://github.com/DrakesCraft-Labs/InvSwitcher-Drake).

---

## 🛠️ Proyectos Seleccionados

| Proyecto | Enfoque y Rol |
|---|---|
| [**StarSuites**](https://github.com/DrakesCraft-Labs/Drakes-Suites) | Consolidación y modernización modular de 180+ addons con SQLite WAL y Rust FFM. |
| [**Star Engine**](https://github.com/DrakesCraft-Labs/Drakes-Suites) | Kernel soberano de servidor, puente Rust/Java (`Star-Rust`), telemetría y economía. |
| [**DrakesCraft Labs**](https://github.com/DrakesCraft-Labs) | Organización de ingeniería: plugins, motores, IA, multimedia e infraestructura. |
| [**SAORI Core**](https://github.com/JackStar6677-1/saori) | Orquestador SRE autónomo omnicanal con memoria auditable y Tríada de IA. |
| [**Slimefun-Rust**](https://github.com/DrakesCraft-Labs/Slimefun-Rust) | Motor de aceleración off-heap en Rust (JNI/FFM) para cálculo SIMD sin pausas de GC. |
| [**CastelRoomKeeper**](https://github.com/JackStar6677-1/CastelRoomKeeper) | Sistema de reservas de salas y gestión institucional para entornos educativos. |
| [**BentoBox-Drake**](https://github.com/DrakesCraft-Labs/BentoBox-Drake) | Fork soberano con deserialización segura de Paper Data Components (Incidente #276). |
| [**VeyonScripts**](https://github.com/JackStar6677-1/VeyonScripts) | Automatización y administración para laboratorios de computación institucionales. |

---

## ⚙️ Filosofía de Trabajo

Me interesa el software que resiste en el tiempo: despliegues reproducibles, observabilidad rigurosa, integridad de datos, documentación clara y trazabilidad absoluta. La tecnología debe simplificar la vida real, no complicarla.
