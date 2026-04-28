# Propuesta de Práctica Temática: Diseño Documentado de Mini Proyecto en Terminal

## 1) Título de la práctica
**Diseño de Práctica Temática Pequeña: Toolkit Académico en Terminal**

> Puedes ajustar el nombre final de tu propuesta (por ejemplo: *Mini Toolkit en ARM64*, *Asistente de Estudio en Terminal*, *Reporteador de Información del Sistema*, *Organizador de Archivos* o *Juego de Aprendizaje en Línea de Comandos*).

---

## 2) Descripción general
En esta actividad vas a **diseñar y documentar** una propuesta de proyecto pequeño que pueda implementarse en poco tiempo y con herramientas sencillas.

### Objetivo
Que el estudiante entregue una propuesta clara, realista y bien estructurada para una práctica temática, priorizando:
- documentación técnica,
- planeación,
- estructura de repositorio,
- y justificación del caso de uso.

### Lenguaje principal (elige solo uno)
- ARM64 Assembly
- C
- Python
- Bash

### Alcance y restricciones
- El proyecto debe ser **pequeño** y viable para trabajar con cuentas gratuitas de IA (Codex u otras con límite de uso).
- **No** se permiten proyectos grandes ni con complejidad de infraestructura.
- Evita: frameworks pesados, APIs pagadas, bases de datos, nube, contenedores y dependencias complejas.
- Si eliges **ARM64 Assembly**, se recomienda que sea un programa **muy pequeño y acotado** (por ejemplo, utilerías mínimas de consola).

### Enfoque de evaluación
Primero se evalúa la **calidad de la propuesta escrita**. El código es opcional y secundario en esta fase.

---

## 3) Entregables del estudiante
Tu repositorio debe incluir, como mínimo:

- `README.md`
- `docs/propuesta.md`
- `docs/caso_de_uso.md`
- `docs/estructura_repositorio.md`
- `docs/plan_de_pruebas.md`

Opcional:
- `src/`
- `scripts/`
- `tests/`

---

## 4) Estructura recomendada del repositorio
Usa como base la siguiente estructura mínima:

```text
nombre-del-proyecto/
├── README.md
├── docs/
│   ├── propuesta.md
│   ├── caso_de_uso.md
│   ├── estructura_repositorio.md
│   └── plan_de_pruebas.md
├── src/
│   └── main.<ext>
├── scripts/
│   └── run.sh
└── tests/
    └── test_plan.md
```

> `<ext>` depende del lenguaje: `s` (Assembly), `c`, `py`, `sh`.

---

## 5) Contenido esperado por archivo

### `README.md`
Incluye:
1. Nombre tentativo del proyecto.
2. Problema que resuelve (en 1–2 párrafos).
3. Lenguaje elegido y justificación.
4. Alcance del proyecto (qué sí hace / qué no hace).
5. Instrucciones rápidas para ejecutar (si hay prototipo).
6. Estructura general del repositorio.

### `docs/propuesta.md`
Incluye:
1. Tema de la práctica.
2. Objetivo general y 2–3 objetivos específicos.
3. Público objetivo o usuario principal.
4. Lista breve de funcionalidades (máximo 5).
5. Cronograma pequeño (por fases o checklist).
6. Riesgos técnicos y mitigación.

### `docs/caso_de_uso.md`
Incluye:
1. Descripción del escenario.
2. Actor principal.
3. Entrada esperada.
4. Proceso general.
5. Salida esperada.
6. Criterios de aceptación del caso.

### `docs/estructura_repositorio.md`
Incluye:
1. Árbol del repositorio.
2. Propósito de cada carpeta/archivo.
3. Convenciones de nombres.
4. Flujo de trabajo propuesto (edición, pruebas, documentación).

### `docs/plan_de_pruebas.md`
Incluye:
1. Estrategia de pruebas manuales (mínimo 5 casos).
2. Formato para registrar resultados (pasó/falló, evidencia, observaciones).
3. Casos límite básicos.
4. Criterio de “listo para entregar”.

---

## 6) Guía para definir un proyecto pequeño (muy importante)
Para que tu propuesta sea aprobada, debe cumplir:
- Se entiende en menos de 2 minutos.
- Se puede prototipar en pocos archivos.
- Requiere pocas dependencias o ninguna.
- Puede correrse en terminal local.
- Tiene valor práctico para un caso real y simple.

Ejemplos de tamaño adecuado:
- Script que organiza archivos por extensión.
- Mini reporte de recursos del sistema (CPU/RAM/disco) en texto.
- Juego básico de preguntas en terminal.
- Convertidor simple (temperatura, unidades, etc.).
- Utilidad pequeña de parsing de logs locales.

---

## 7) Rúbrica sugerida (100 puntos)
- **Calidad de documentación** (40 pts)
  - Claridad, orden, redacción técnica y consistencia.
- **Diseño del caso de uso** (20 pts)
  - Coherencia entre problema, proceso y resultado.
- **Estructura del repositorio** (20 pts)
  - Organización, nombres y mantenibilidad.
- **Plan de pruebas** (15 pts)
  - Cobertura mínima, casos límite y criterio de aceptación.
- **Viabilidad del alcance** (5 pts)
  - Proyecto realista, pequeño y ejecutable.

---

## 8) Criterios de rechazo automático
Se puede rechazar la propuesta si:
- El alcance es demasiado grande para una práctica corta.
- Depende de servicios pagados o infraestructura compleja.
- No incluye los archivos obligatorios de `docs/`.
- No justifica el lenguaje elegido.
- No existe plan de pruebas.

---

## 9) Entrega en GitHub Classroom
1. Acepta la tarea en GitHub Classroom.
2. Crea tu propuesta con la estructura indicada.
3. Haz commits claros (ej. `docs: agrega caso de uso inicial`).
4. Sube cambios a tu repositorio remoto.
5. Verifica que todos los archivos mínimos estén presentes.

---

## 10) Recomendaciones finales del instructor
- Empieza por escribir, luego programa.
- Si usas ARM64 Assembly, mantén alcance mínimo y bien delimitado.
- Evita “prometer de más”; una propuesta pequeña y sólida vale más.
- Documenta decisiones técnicas brevemente pero con fundamento.

¡Éxito! La meta es que aprendas a **diseñar bien** antes de implementar.
