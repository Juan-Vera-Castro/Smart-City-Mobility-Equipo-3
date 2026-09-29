# 🚦 Proyecto: Smart City Traffic & Mobility - Equipo 3

**Asignatura:** Ingeniería de Software II
**Rol del Scrum Master:** Juan Esteban Vera Castro  
**Enlace al Proyecto en Jira:** [https://uceva-team-sigabu3.atlassian.net/jira/software/projects/SCM/boards/67/backlog]

---

## 📋 1. Criterios de Calidad del Equipo

### Definition of Ready (DoR) - "Listo para Desarrollar"
Para que una Historia de Usuario (US) pueda entrar a un Sprint, debe cumplir obligatoriamente:
* Estar redactada en formato: *"Como [actor], quiero [acción], para [beneficio]"*.
* Tener Criterios de Aceptación definidos usando el formato Gherkin (*Dado / Cuando / Entonces*).
* Estar estimada en Story Points por los Developers.
* Estar vinculada a una de las 4 Epics principales.
* No tener dependencias técnicas bloqueantes o ambiguas.

### Definition of Done (DoD) - "Terminado"
Para que una Historia de Usuario se mueva a la columna *Done*, debe cumplir:
* El código debe tener un Pull Request aprobado por al menos 1 par (Code Review).
* Cobertura de pruebas unitarias mayor o igual al 80%.
* Los criterios de aceptación han sido probados y validados en el ambiente de *staging* (pruebas).
* La documentación técnica (ej. API, diagramas) está actualizada.

---

## 🗓️ 2. Planificación Multi-Sprint (Hoja de Ruta)

| Sprint | Duración | Sprint Goal (Objetivo) | Historias Asociadas | Total Story Points |
| :--- | :--- | :--- | :--- | :--- |
| **Sprint 1** | 3 Semanas | Desplegar la infraestructura básica de ingestión de datos de tráfico y el mapa base para operadores. | SCM-1, SCM-2, SCM-3 | 13 pts |
| **Sprint 2** | 3 Semanas | Integrar la lectura de sensores de calidad del aire (PM2.5/PM10) y alertas ambientales en tiempo real. | SCM-4, SCM-5, SCM-6 | 13 pts |
| **Sprint 3** | 3 Semanas | Habilitar el acceso web/móvil para ciudadanos con consulta de rutas alternativas y reporte de incidentes. | SCM-7, SCM-8, SCM-9 | 11 pts |
| **Sprint 4** | 3 Semanas | Consolidar reportes históricos y habilitar el módulo de analítica predictiva de tráfico basado en IA. | SCM-10, SCM-11, SCM-12 | 12 pts |

---

## 📈 3. Análisis de Métricas y Gráficos (Jira Reports)

*(Sube las imágenes a tu repositorio o arrástralas aquí cuando estés editando en GitHub)*

**Captura del Velocity Chart:** 
[Insertar Imagen Aquí]

**Captura del Sprint Burndown Chart (Sprint 1 y 2):** 
[Insertar Imagen Aquí]

### Análisis de la Simulación y Acciones Correctivas
Durante el **Sprint 2**, se evidenció una desviación en el *Burndown Chart*, donde la línea real de quema de puntos se mantuvo por encima de la línea ideal. Esto se debió a un bloqueo técnico simulado en la integración de los sensores ambientales, lo que resultó en un cumplimiento de solo el 66% de los Story Points comprometidos, tal como se refleja en la diferencia entre *Commitment* y *Completed* en el *Velocity Chart*.

Para proteger los **Sprints 3 y 4**, el equipo aplicará acciones correctivas enfocadas en la refinación del backlog. Seremos más estrictos con la *Definition of Ready (DoR)*, asegurando que las dependencias técnicas externas (como APIs de sensores) estén resueltas antes de iniciar el Sprint, y ajustaremos nuestra capacidad planificada basándonos en la velocidad real demostrada en las iteraciones anteriores.
