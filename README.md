# Taller de Métricas para la Gestión de Proyectos de Software
Este repositorio contiene un ejercicio autoguiado para medir el avance, calidad, eficiencia y costos
de un mini-proyecto de software usando GitHub Projects, GitHub Issues, GitHub Actions y un dashboard
web.
## Objetivo
Aplicar métricas de gestión de proyectos de software para tomar decisiones basadas en datos.
## Métricas analizadas
- Porcentaje de tareas completadas.
- Velocity del sprint.
- Bugs abiertos y cerrados.
- Tiempo promedio de resolución.
- Horas estimadas vs. horas reales.
- Variación de presupuesto.
- Tareas vencidas.
- Riesgos del proyecto.
## Análisis de resultados

### 1. Avance del proyecto
**Porcentaje de avance:** 60% (6 de 10 tareas completadas)

El proyecto se encuentra en un estado **MEDIO-ALTO de avance**. Con el 60% de las tareas completadas y una velocity de 12 story points en el sprint actual, el equipo mantiene un ritmo de trabajo constante. Se espera alcanzar el 80-100% en el siguiente sprint si se mantiene la velocidad actual.

**Datos:**
- Total de tareas: 10
- Tareas cerradas: 6
- Tareas abiertas: 4
- Story points completados: 12

### 2. Calidad
**Estado:** La calidad del producto está **EN RIESGO**. 

Existen 2 bugs abiertos (#8 y #3: "Corregir error en cálculo de porcentaje") sin resolver, lo que representa el 100% de los bugs identificados permaneciendo sin cerrar. Aunque no hay bugs resueltos aún, el bajo volumen de defectos mantiene la calidad dentro de rangos aceptables.

**Datos:**
- Total de bugs: 2
- Bugs abiertos: 2 (100%)
- Bugs cerrados: 0 (0%)
- Tiempo promedio de resolución: 0.04 horas

**Recomendación:** Asignar máxima prioridad a la corrección del bug de cálculo de porcentaje antes de nuevas funcionalidades.

### 3. Costos
**Estado:** Los costos están **PERFECTAMENTE CONTROLADOS**.

La comparación entre horas estimadas y reales muestra **CERO desviación**. El equipo cumplió exactamente con las estimaciones de tiempo:
- Horas estimadas: 20h
- Horas reales: 20h
- Variación: $0 USD (0%)
- Costo actual: $400 USD
- ROI: 50% sobre inversión

Este resultado indica que el proceso de estimación es muy preciso y puede usarse como baseline para futuros sprints.

### 4. Riesgos
**Nivel de riesgo calculado:** **ALTO** 🔴

**Factores de riesgo identificados:**

| Riesgo | Descripción | Impacto | Acción |
|--------|-------------|---------|--------|
| **Bugs sin resolver** | 2 bugs críticos abiertos | Crítico | Resolver antes de release |
| **Tareas bloqueadas** | 1 tarea marcada como bloqueada (#10) | Medio | Desbloquear dependencias |
| **Tareas vencidas** | 0 tareas vencidas | Bajo | Continuar monitoreo |

### 5. Decisiones recomendadas
Como jefe de proyecto, basándome en los datos, se recomienda:

**🔴 Inmediatas (Próximas 24 horas):**
- **Prioridad máxima:** Asignar recursos para corregir el bug #8 (#3) de cálculo de porcentaje
- **Desbloquear:** Revisar y resolver bloqueos de la tarea #10 (Validar interpretación de métricas)

**⚡ Corto plazo (Esta semana):**
- Implementar code review obligatorio para prevenir bugs futuros
- Acelerar las 4 tareas abiertas restantes para alcanzar 100% de completitud
- Establecer gates de calidad antes de cierre de sprint

**📊 Mediano plazo (Próximas 2 semanas):**
- Usar la precisión de estimaciones actuales como baseline
- Establecer SLA máximo de 24 horas para bugs críticos
- Implementar tests unitarios para cálculos numéricos

### 6. Respuesta a preguntas de análisis

**1. ¿Cuál es el porcentaje de avance del proyecto?**
60% de completitud (6/10 tareas cerradas). Avance MEDIO-ALTO.

**2. ¿La velocity del sprint es suficiente frente al alcance planeado?**
Sí. Con 12 story points completados y 4 tareas abiertas restantes, el equipo puede completar el proyecto en 1-2 sprints más.

**3. ¿Existen bugs abiertos que afecten la entrega?**
Sí. 2 bugs abiertos (100% de bugs identificados) relacionados con cálculo de porcentaje. Deben resolverse antes de release.

**4. ¿Las horas reales superaron las horas estimadas?**
No. Las horas reales (20h) coinciden exactamente con las estimadas (20h). Variación = 0%.

**5. ¿El proyecto presenta desviación de costo?**
No. Costo estimado = $400 USD. Costo real = $400 USD. Variación = $0 USD (0%).

**6. ¿Qué tareas representan mayor riesgo?**
- Bug #8/#3: Error en cálculo de porcentaje (alta prioridad, abierto)
- Tarea #10: Validación de métricas (bloqueada, dependencia crítica)

**7. ¿Qué decisión debería tomar el jefe de proyecto con base en los datos?**
Parar nuevas funcionalidades temporalmente y dedicar 100% de recursos a:
1. Cerrar los 2 bugs abiertos (máxima prioridad)
2. Desbloquear y completar la tarea #10
3. Validar las 4 tareas abiertas antes de cierre

**8. ¿Qué métrica agregaría para mejorar la visibilidad?**
- Tiempo de ciclo (cycle time) por tipo de tarea
- Burndown chart por sprint
- Distribución de bugs por componente
- Índice de calidad del código (code coverage)
- Satisfacción del cliente/stakeholder

## Conclusiones finales

El proyecto está en buen camino con un 60% de avance y costos controlados perfectamente. Sin embargo, el nivel de riesgo es ALTO debido a 2 bugs abiertos que deben resolverse antes de cualquier entrega. Se recomienda usar el siguiente sprint para cerrar todos los issues abiertos y validar la interpretación de métricas con el equipo.

**Cadena de valor generada:** Issues → GitHub Project → GitHub Actions → metrics.json → Dashboard → **Decisiones basadas en datos**
