# README extendido

Este archivo complementa el README principal. Reune contexto tecnico mas estable sobre mi forma de trabajar, infraestructura, proyectos paralelos y areas de dominio.

No busca ser biografia completa. Es una ficha ampliada de criterio tecnico, experiencia practica y lineas de trabajo.

---

## Perfil base

Soy **Ingeniero en Informatica titulado por DUOC UC**. Trabajo entre desarrollo de software, infraestructura digital, administracion de sistemas, automatizacion para laboratorios, soporte TI y herramientas internas.

Mi forma natural de trabajar es sistemica: entiendo dependencias, separo capas, mido riesgo, documento lo necesario y busco continuidad operacional. Me interesa menos acumular tecnologia y mas construir cosas que puedan vivir, mantenerse y recuperarse si algo falla.

## Areas donde puedo operar

| Area | Ejemplos concretos |
|---|---|
| Desarrollo web | Sitios, landings, paneles, APIs, formularios, dashboards y sistemas internos. |
| Backend y datos | Python, FastAPI, PHP, Java, PostgreSQL, MySQL, SQLite, migraciones y validaciones. |
| Infraestructura | Linux, Docker, Cloudflare Tunnel, Tailscale, systemd, UFW, fail2ban, backups y monitoreo. |
| Soporte TI | Equipos, laboratorios, red, cableado, salas, proyectores, continuidad operativa y diagnostico. |
| Automatizacion | Python, PowerShell, Bash, reportes, scripts reproducibles e integraciones de APIs. |
| Minecraft tecnico | Paper, Spigot, Slimefun, plugins, rendimiento, mantenimiento y ecosistema DrakesCraft. |
| Documentacion | README utiles, runbooks, rollback, procedimientos y guias para continuidad. |

## Infraestructura actual: star

`star` es mi servidor de produccion. No lo trato como experimento desordenado: esta pensado para servicios vivos, con exposicion controlada y operaciones basicas de mantenimiento.

### Componentes generales

- Ubuntu 26.04 LTS.
- Docker para servicios productivos.
- Cloudflare Tunnel para dominios publicos.
- Tailscale para paneles internos y administracion.
- UFW con politica restrictiva.
- fail2ban para SSH.
- Rotacion de logs Docker.
- Healthcheck local con timer systemd.
- Backups Restic con prueba de restore.

### Servicios publicos

| Servicio | Rol |
|---|---|
| `calendar.drakescraft.cl` | CCAACalendar, calendario multicentro con reservas e integracion Google Calendar. |
| `web.drakescraft.cl` | Portal publico del ecosistema DrakesCraft. |
| `jack.drakescraft.cl` | Portal profesional publico con backend liviano y API. |

### Servicios internos protegidos

Uso paneles de administracion y monitoreo, pero no publico sus rutas privadas ni los expongo como servicios abiertos. La idea es separar el plano publico del plano administrativo.

- Webmin.
- Portainer.
- Uptime Kuma.
- Administracion por Tailscale.

## Proyectos productivos

### CCAACalendar

Plataforma multicentro para calendarios institucionales, reservas, centros, permisos e integracion con Google Calendar. El foco es coordinacion real de espacios y visibilidad por centro.

Tecnologias y criterios:

- Backend Python/FastAPI.
- PostgreSQL.
- Docker.
- Migraciones Alembic.
- Integracion Google Calendar.
- Healthcheck publico.
- Control de acceso y separacion por centro.

### jack-portal

Portal profesional publico en `jack.drakescraft.cl`.

Caracteristicas:

- Landing oscura/premium orientada a servicios tecnicos.
- Backend liviano con Python stdlib.
- Endpoints publicos seguros:
  - `/api/health`
  - `/api/profile`
  - `/api/services`
  - `/api/projects`
  - `/api/contact`
- Formulario con validacion, honeypot y rate limit simple.
- Docker en `127.0.0.1:8082`.

### DrakesCraft Web

Portal publico del ecosistema DrakesCraft. Sirve como punto de entrada a comunidad, tienda/informacion y presencia del proyecto.

## Automatizacion y soporte TI

### VeyonScripts

Herramientas de diagnostico y automatizacion para laboratorios con Veyon.

Casos de uso:

- Escaneo de red.
- Mapeo de equipos.
- Diagnostico por sala.
- Operacion masiva de laboratorios.
- Soporte reproducible para entornos Windows.

### Soporte en terreno

Experiencia con:

- Equipos de laboratorio.
- Proyectores.
- Cableado.
- Switches.
- Patch panels.
- Clonado con Clonezilla.
- Despliegues Windows.
- Diagnostico de conectividad.

## Redes y sistemas

Manejo intermedio/practico de:

- IP estatica/dinamica.
- DHCP.
- DNS.
- NAT.
- VLAN basicas.
- Resolucion de conflictos de red.
- Identificacion por MAC.
- Herramientas como `tracert`, `nslookup`, `ipconfig`, `netstat`, `ss`, `curl` y logs de sistema.

Me adapto rapido a infraestructura nueva si tengo acceso, contexto y restricciones claras.

## Servidores Minecraft y DrakesCraft

Administro el ecosistema DrakesCraft desde un enfoque tecnico, no solo comunitario.

Areas:

- Paper / Spigot / Purpur.
- Slimefun.
- Plugins propios o adaptados.
- Rendimiento, TPS, timings y cuellos de botella.
- Backups y mantenimiento.
- Staff tooling.
- Arquitectura de mundos, ranks, crates y sistemas modulares.
- Organizacion [DrakesCraft-Labs](https://github.com/DrakesCraft-Labs).

## Laboratorio personal

Algunas lineas son exploratorias. Las mantengo porque prueban ideas de arquitectura, simulacion, tooling local o automatizacion.

- **Aurexalis:** navegador personal, Gecko/Floorp, Rust y UI reactiva.
- **AstroControlSim:** simulacion/control de sistemas.
- **omnisky-miner:** observatorio virtual local con dashboard y SQLite.
- **Coronalis:** addon Slimefun con conceptos astronomicos.
- **AureonVault:** exploracion de file manager local para Windows.
- **VotV-Points-Editor:** utilidad local con enfoque seguro y backups.
- **StellarDaybook:** bitacora automatizada y memoria tecnica diaria.

## Setup de trabajo

- **PC principal:** Ryzen 5 5500, RTX 4060 8GB, 32GB RAM, almacenamiento NVMe/HDD. Uso para backend, Docker, IA local ligera, compilaciones, multimedia, VMs y servidores locales.
- **Laptop de trabajo:** Intel Core i7, NVIDIA MX450, 16GB RAM, SSD. Uso para desarrollo, scripting, administracion TI y trabajo remoto.
- **Sistemas:** Fedora, Windows, WSL2/Ubuntu y servidores Linux.
- **IDE:** VS Code, PyCharm y herramientas de consola.

## Filosofia de desarrollo

- Hago codigo practico, no adornado para tutoriales.
- Prefiero automatizar antes que repetir procesos manuales.
- Todo lo que construyo debe responder a una necesidad real o aprendizaje tecnico claro.
- Si nadie ordena un sistema, el sistema se degrada.
- La documentacion corta y accionable vale mas que una explicacion enorme imposible de mantener.
- Produccion sin backup, monitoreo o rollback no esta realmente lista.

## Como trabajo

1. Diagnostico el problema y sus restricciones.
2. Identifico dependencias, datos, usuarios y riesgos.
3. Propongo una ruta tecnica realista.
4. Implemento por etapas.
5. Valido con casos reales.
6. Documento lo necesario.
7. Dejo una forma de mantener, respaldar o revertir.

## Lineas de trabajo actuales

- Sistemas de calendario, reservas y coordinacion institucional.
- Portales web publicos con backend ligero.
- Infraestructura personal/profesional en `star`.
- Automatizacion y diagnostico para laboratorios.
- Ecosistema DrakesCraft y plugins/servidores Minecraft.
- Herramientas locales para soporte, bitacora, diagnostico y respaldo.
- Exploracion aplicada de IA como copiloto de investigacion, prototipado y mantenimiento.

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

Estas certificaciones estan otorgadas por el Instituto Profesional DUOC UC segun las disposiciones reglamentarias vigentes.

## Estadisticas extendidas

![Stats](https://github-readme-stats.vercel.app/api?username=JackStar6677-1&show_icons=true&hide_border=true&theme=tokyonight)

![Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=JackStar6677-1&layout=compact&hide_border=true&theme=tokyonight)

![Streak](https://streak-stats.demolab.com/?user=JackStar6677-1&theme=tokyonight&hide_border=true&locale=es&mode=weekly)
