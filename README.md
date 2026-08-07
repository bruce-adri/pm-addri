# Sistema de Project Management de Adrián

Sistema único para todo (trabajo MPC, personal, ideas y proyectos técnicos).

## Estructura

```
pm/
  roadmap.md              <- vista agregada de todos los proyectos
  inbox.md                <- capturas rápidas sin clasificar
  projects/
    trabajo/               <- proyectos de MPC Group
    personal/              <- proyectos personales (deporte, casa, etc.)
    bruce/                 <- mejoras del agente Bruce (hoja de ruta de David)
    ideas/                 <- ideas a explorar, todavía no son proyectos activos
```

## Formato de un proyecto (`projects/<área>/<nombre>.md`)

```markdown
---
area: trabajo|personal|bruce|ideas
status: 🟢 activo | 🟡 en pausa/en marcha | 🔴 no iniciado/bloqueado | ✅ completado | ❌ descartado | 💡 idea
priority: crítica | alta | media | baja
updated: YYYY-MM-DD
---

# Nombre del proyecto

## Objetivo
## Próxima acción
## Acciones / Tareas
- [ ] ...
## Notas
```

## Flujos habituales

- **"Abre un nuevo proyecto X"** → crear `projects/<área>/x.md` con la plantilla anterior, añadir fila en `roadmap.md`.
- **"Asocia estas tareas a este proyecto"** → añadirlas en la sección "Acciones / Tareas" del archivo del proyecto.
- **"Añade una acción"** → añadir a "Acciones / Tareas" del proyecto correspondiente (o a `inbox.md` si no está claro a qué proyecto pertenece).
- **"He tenido esta idea..."** → añadir a `inbox.md`; si toma forma, se convierte en proyecto en `projects/ideas/` o en el área que corresponda.
- **"¿En qué tengo que trabajar?" / "roadmap" / "propónme"** → leer `roadmap.md` + revisar `inbox.md` y proponer en base a estado/prioridad/próxima acción.

## Relación con Bruce

Los proyectos de MPC estaban antes en `~/bruce/memory/context/active-projects.md`. Ahora la fuente de verdad es este sistema (`pm/`). Ese archivo de Bruce y todas sus referencias cruzadas (CLAUDE.md, MEMORY.md, /wrap, knowledge/) se actualizaron el 2026-06-14 para apuntar aquí en vez de duplicar.
