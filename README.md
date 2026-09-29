# 🚦 Proyecto: Smart City Traffic & Mobility - Equipo 3

**Asignatura:** Ingeniería de Software II
**Rol del Scrum Master:** Juan Esteban Vera Castro  
**Enlace al Proyecto en Jira:** [https://uceva-team-sigabu3.atlassian.net/jira/software/projects/SCM/boards/67/backlog]

---

## 📋 1. Criterios de Calidad del Equipo

### Definition of Ready (DoR) - "Listo para Desarrollar"
Para que una Historia de Usuario (US) pueda entrar a un Sprint activo en Jira, debe cumplir obligatoriamente con:

* **Formato Estándar:** Estar redactada en formato *"Como [actor], quiero [acción], para [beneficio]"*.
* **Criterios de Aceptación:** Tener escenarios definidos usando la sintaxis Gherkin (*Dado / Cuando / Entonces*).
* **Estimación:** Estar estimada en Story Points por el equipo de Developers.
* **Trazabilidad:** Estar vinculada a una de las 4 Epics principales del proyecto.
* **Sin Bloqueos:** No tener dependencias técnicas bloqueantes o ambiguas sin resolver.

### Definition of Done (DoD) - "Terminado"
Para que una Historia de Usuario se mueva a la columna *Done* en Jira, debe cumplir con los siguientes estándares de calidad:

* **Code Review:** El código debe contar con un Pull Request (PR) aprobado por al menos 1 par.
* **Pruebas Unitarias:** Cobertura de pruebas unitarias mayor o igual al $80\%$.
* **Validación en Staging:** Criterios de aceptación probados y validados en el ambiente de pruebas (*staging*).
* **Documentación:** Documentación técnica (API REST, esquemas de BD, diagramas) debidamente actualizada.

---

## 🗓️ 2. Planificación Multi-Sprint (Hoja de Ruta)

| Sprint | Duración | Sprint Goal (Objetivo del Sprint) | Historias Asociadas | Total Story Points |
| :--- | :--- | :--- | :--- | :--- |
| **Sprint 1** | 3 Semanas | Desplegar la infraestructura básica de ingestión de datos de tráfico y el mapa base para operadores. | SCM-5, SCM-6, SCM-7 | 13 pts |
| **Sprint 2** | 3 Semanas | Integrar la lectura de sensores de calidad del aire (PM2.5/PM10) y alertas ambientales en tiempo real. | SCM-8, SCM-9, SCM-10 | 13 pts |
| **Sprint 3** | 3 Semanas | Habilitar el acceso web/móvil para ciudadanos con consulta de rutas alternativas y reporte de incidentes. | SCM-11, SCM-12, SCM-13 | 11 pts |
| **Sprint 4** | 3 Semanas | Consolidar reportes históricos y habilitar el módulo de analítica predictiva de tráfico basado en IA. | SCM-14, SCM-15, SCM-16 | 12 pts |

---

## 📈 3. Análisis de Métricas y Gráficos (Jira Reports)

*(Sube las imágenes de los informes generados en Jira a tu repositorio o arrástralas aquí al editar en GitHub)*

* **Captura del Velocity Chart:** `[Insertar Imagen Aquí]`
* **Captura del Sprint Burndown Chart (Sprint 1 y 2):** `[Insertar Imagen Aquí]`

### Análisis de la Simulación y Acciones Correctivas

Durante el **Sprint 2**, se evidenció una desviación en el *Burndown Chart*, donde la línea real de quema de puntos se mantuvo por encima de la línea ideal. Esto se debió a un bloqueo técnico simulado en la integración de los sensores ambientales, lo que resultó en un cumplimiento de solo el 66% de los Story Points comprometidos, tal como se refleja en la diferencia entre *Commitment* y *Completed* en el *Velocity Chart*.

Para proteger los **Sprints 3 y 4**, el equipo aplicará acciones correctivas enfocadas en la refinación del backlog. Seremos más estrictos con la *Definition of Ready (DoR)*, asegurando que las dependencias técnicas externas (como APIs de sensores) estén resueltas antes de iniciar el Sprint, y ajustaremos nuestra capacidad planificada basándonos en la velocidad real demostrada en las iteraciones anteriores.

---

## 🛠️ 4. Viabilidad Técnica y Arquitectura del Sistema

Para garantizar la escalabilidad, baja latencia y alta disponibilidad requerida por la plataforma Smart City, el equipo de desarrollo define el siguiente stack tecnológico y arquitectura:

* **Ingestión e IoT (Tiempo Real):**
  * **Apache Kafka / MQTT Broker:** Para la recepción concurrente de telemetría proveniente de sensores de tráfico y estaciones de calidad del aire con latencias sub-segundo ($< 5$ segundos).
* **Almacenamiento y Capa de Datos:**
  * **PostgreSQL + PostGIS:** Base de datos relacional con extensión espacial para el modelado geográfico de nodos, tramos viales, ubicaciones de cámaras y zonas urbanas.
  * **TimescaleDB / Redis:** Base de datos de series temporales y caché en memoria para almacenamiento optimizado de lecturas masivas y cálculo de promedios al vuelo.
* **Backend y APIs:**
  * **Node.js / FastAPI (Python):** Microservicios RESTful para la gestión administrativa e integración con servicios de ruteo, junto con **WebSockets / Server-Sent Events (SSE)** para la actualización dinámica de estados en el mapa en tiempo real.
* **Frontend y Portal Ciudadano:**
  * **React.js + Mapbox GL JS / Leaflet:** Renderizado vectorial y dinámico del mapa de la ciudad con capas conmutables (Tráfico y Calidad del Aire) y diseño *Responsive Mobile*.
* **Analítica Predictiva y ML:**
  * **Python (Scikit-Learn / XGBoost):** Pipeline de entrenamiento supervisado que procesa series históricas de velocidad y flujo para predecir congestión vial en ventanas futuras de 30 a 180 minutos.
