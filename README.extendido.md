# README extendido

Este archivo complementa el README principal. Reune contexto tecnico mas estable sobre mi forma de trabajar, infraestructura, proyectos paralelos y areas de dominio.

No busca ser biografia completa. Es una ficha ampliada de criterio tecnico, experiencia practica y lineas de trabajo.

---

## Perfil base

Soy **Ingeniero en Informatica titulado por DUOC UC**. Trabajo entre arquitectura de motores y sistemas de alta concurrencia (Java 25 + Rust Panama FFM), desarrollo de software full-stack, infraestructura Linux/Windows, automatizacion para laboratorios, soporte TI institucional y orquestacion de agentes de IA.

Mi forma natural de trabajar es sistemica: entiendo dependencias, separo capas, mido riesgo con datos reales, documento lo necesario y busco continuidad operacional. Me interesa menos acumular tecnologia de moda y mas construir sistemas que puedan vivir en produccion, mantenerse y recuperarse limpiamente si algo falla.

## Areas donde puedo operar

| Area | Ejemplos concretos |
|---|---|
| Motores y Sistemas (Java × Rust) | `DrakesPurpur 26.2` (Java 25 + Rust Panama FFM), `DrakeStar-Launcher` (Tauri 2 + Rust + Svelte 5), `Slimefun-Rust`, optimizacion de chunks y protocolos binarios (`horizon:lod` v1, SLP `0x00`). |
| Compiladores, Grafos e IA | `OmniAST / GraphLang`, `graphify`, `SAORI 3.0` (Antigravity, Codex, Claude, NVIDIA Cloud NIM), MCP `ai_hub_memory`, observabilidad y reduccion de tokens. |
| Desarrollo web y escritorio | Sitios, landings, paneles, APIs, Tauri 2, Svelte 5, TypeScript, dashboards y sistemas internos. |
| Backend y datos | Python, FastAPI, Rust, Java 21/25, PHP, PostgreSQL, MySQL, SQLite WAL, migraciones y validaciones transaccionales. |
| Infraestructura | Linux (Ubuntu/Debian/Fedora/Kubuntu), Docker, Cloudflare Tunnel, Tailscale, systemd, UFW, fail2ban, backups Restic/7z y monitoreo. |
| Soporte TI e Instituciones | Equipos, laboratorios, servidores fisicos (`ccg-fisico`), red, cableado, salas, proyectores, continuidad operativa y diagnostico. |
| Ecosistema Open-Source | Mas de 200 repositorios en [`SlimefunNewHorizons` (DrakesCraft Labs)](https://github.com/SlimefunNewHorizons): suites autonomas (`Multiverse` junto a Chagui68), forks open-source endurecidos (`BentoBox-Drake`, `PlayerVaultZ-Drake`, `CrazyAuctions`, `WorldwideChat`), `StarSuites` y division Linux/HUDs (junto a DrgX89). |

## Infraestructura actual: Star, Nexus y Clúster Distribuido

Opero una topologia coordinada por Tailscale y SSH entre la nube y estaciones locales:

- **`star` (VPS 24/7 en produccion):**
  - Ubuntu LTS + Docker para servicios productivos (`SAORI`, `ai_hub_memory` MCP en `:8077`, portales web, calendarios, monitoreo).
  - Cloudflare Tunnel para dominios publicos (`web.drakescraft.cl`, `calendar.drakescraft.cl`, `jack.drakescraft.cl`).
  - Tailscale para plano administrativo interno (Webmin, Portainer, Uptime Kuma, MCP).
  - UFW restrictivo, fail2ban, rotacion de logs, healthchecks por timers systemd y backups Restic con prueba de restauracion.
- **`nexus` (Estacion de Ingenieria Local):**
  - Windows 11 + WSL2 Ubuntu + JDK 21 & JDK 25 Temurin + Rust 1.94+ + Node 24 + RTX 4060.
  - Espejo sincronizado de los **241+ repositorios** (organizacion y personales) con grafos AST locales (`graphify` + `omniast`) para compilacion pesada, benchmarks JFR y pruebas de integracion de **Project Purple**.

## Project Purple y Organización DrakesCraft Labs (`SlimefunNewHorizons`)

La organizacion **[Slimefun: New Horizons · DrakesCraft Labs](https://github.com/SlimefunNewHorizons)** abarca mucho mas que solo Slimefun:

1. **Project Purple (`DrakesPurpur` + `DrakeStar-Launcher`):**
   - **[`DrakesPurpur`](https://github.com/SlimefunNewHorizons/DrakesPurpur):** Motor de servidor hibrido en Java 25 + Rust (`native/drakes-hybrid` via Panama FFM) con paridad bit a bit verificada en NBT y ruido, prefetch direccional de chunks en dos niveles (`P-promovido`), codec y cache LRU $O(1)$ de terreno lejano (`HorizonLodProtocol` / `HorizonLodCache`), Crash Guard y aislamiento de 6 modalidades.
   - **[`DrakeStar-Launcher`](https://github.com/SlimefunNewHorizons/DrakeStar-Launcher):** Launcher hibrido de escritorio en Tauri 2 + Rust + Svelte 5 para gestionar clientes, servidores locales (`Local Forge` con consola en vivo, instalador de preset Slimefun y backups de mundos) y estado online (`mc_status_ping` SLP `0x00`), con 51/51 tests en Rust pasando en Windows y Linux.
2. **Suite Multiverse y Pumpkin-Launcher (por [Chagui68](https://github.com/Chagui68)):**
   - Plugins 100% autonomos (`MultiverseNets`, `MultiverseCreatures`, `MultiverseTinker`, `MultiverseProgramming`, `MultiverseGambling`) que funcionan sin depender de Slimefun, junto con [`Pumpkin-launcher`](https://github.com/Chagui68/Pumpkin-launcher).
3. **Forks Open-Source Endurecidos (Independientes de Slimefun):**
   - Mantenimiento oficial de forks open-source para Paper 1.21.11 y Purpur 26.2: `BentoBox-Drake`, `InvSwitcher-Drake`, `PlayerVaultZ-Drake`, `CrazyAuctions`, `sbank`, `LevelledMobs-Drake`, `WorldwideChat` e `InteractiveChat-DiscordSRV-Addon`.
4. **División de Escritorio Linux, Temas Cyberpunk y HUDs (junto a [DrgX89 / Nixcobt](https://github.com/DrgX89)):**
   - Integracion de proyectos de personalizacion avanzada de Linux en QML y Python (`Blackwall-Kubuntu`, bootloaders GRUB y `Hud-Linux`).
5. **`StarSuites` (`Drakes-Suites`) y `Slimefun4-Drake`:**
   - Consolidacion modular en 8 Mega-Suites para Paper/Purpur 26.2 (JDK 25) y matriz automatizada en 8 shards para 112 addons.

## Proyectos Institucionales y Soporte TI

### CastelRoomKeeper / CCAACalendar
Plataforma multicentro para calendarios institucionales, reservas, centros, permisos e integracion con Google Calendar (FastAPI, PostgreSQL, Docker, Alembic).

### VeyonScripts y Automatización de Laboratorios
Herramientas de diagnostico, escaneo de red, mapeo de equipos y operacion masiva para laboratorios de computacion con Veyon, junto con soporte en terreno (cableado, switches, patch panels, proyectores y clonado con Clonezilla).

## Laboratorio Personal

- **OmniAST / GraphLang:** kernel de grafos intermedios para agentes de IA y transpilacion multi-objetivo.
- **Aurexalis:** navegador personal basado en Gecko/Floorp, Rust y UI reactiva.
- **AstroControlSim & omnisky-miner:** simulacion de control y observatorio virtual local con SQLite.
- **AureonVault & StellarDaybook:** explorador local seguro para Windows y bitacora tecnica automatizada.

## Setup de trabajo

- **PC principal (`Nexus`):** Ryzen 5 5500, RTX 4060 8GB, 32GB RAM, almacenamiento NVMe/HDD.
- **Laptop de trabajo (`Nova`):** Intel Core i7, NVIDIA MX450, 16GB RAM, SSD.
- **Sistemas:** Fedora / Ubuntu / Kubuntu Linux, Windows 11 y WSL2.

## Certificaciones DUOC UC

- Titulo profesional: Ingeniero en Informatica.
- Curriculum completo de la carrera.
- Arquitectura de Software.
- Programacion de Software.
- Analisis y Desarrollo de Modelos de Datos.
- Gestion de Proyectos Informaticos.
- Inteligencia de Negocios (BI).
- Calidad de Software.
- Analisis y Planificacion de Requerimientos Informaticos.
- Ingles Internacional - Nivel Intermedio Alto.

## Estadisticas extendidas

![Stats](https://github-readme-stats.vercel.app/api?username=JackStar6677-1&show_icons=true&hide_border=true&theme=tokyonight)

![Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=JackStar6677-1&layout=compact&hide_border=true&theme=tokyonight)

![Streak](https://streak-stats.demolab.com/?user=JackStar6677-1&theme=tokyonight&hide_border=true&locale=es&mode=weekly)
