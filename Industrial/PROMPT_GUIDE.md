# Guía de Prompts para crear OVAs de Ingeniería Industrial

Esta guía indica qué escribirle a la IA para obtener un OVA coherente con la identidad visual de `Pregrado/Industrial`.

---

## Paso 1 — Dale el contexto a la IA

Empieza enviando este mensaje:

```
Lee el archivo context.md que está en la carpeta Pregrado/Industrial.
Memoriza todas las reglas que contiene. Usarás la identidad visual azul marino + naranja/ámbar del programa de Ingeniería Industrial.
```

> Si el modelo no tiene acceso a archivos, copia y pega el contenido completo de `context.md` directamente en el chat.

---

## Paso 2 — Prepara tu guía de aprendizaje en Markdown

Tu guía debe tener las secciones del OVA:

```markdown
# [Título del OVA]

## Introducción
[Texto de introducción al tema]

## Objetivos
- [Objetivo 1]
- [Objetivo 2]
- [Objetivo 3]

## Contenido
### [Subtema 1]
[Explicación o puntos clave]

### [Subtema 2]
[Explicación o puntos clave]

## Actividades
- [Descripción de la actividad 1]
- [Descripción de la actividad 2]

## Recursos
1. [Nombre] — [URL]
2. [Nombre] — [URL]

## Bibliografía
- [Referencia APA 1]
- [Referencia APA 2]
```

---

## Paso 3 — Usa esta plantilla de prompt

```
Crea un OVA completo en HTML siguiendo todas las reglas del context.md de Pregrado/Industrial.

Usa la identidad visual verde azulado (#134e4a) y rosa (#f43f5e). No uses la paleta verde de repositorios técnicos ajenos.
El logo debe ser img/logo.svg.

Te entrego mi guía de aprendizaje en Markdown. Respeta este mapeo de secciones:
- Introducción, Objetivos, Actividades, Recursos y Bibliografía: MANTÉN el contenido de mi guía
  (mismos objetivos, mismas actividades, mismos recursos/anexos y misma bibliografía), solo adáptalos
  al formato web interactivo con estilo, emojis moderados y gamificación en las actividades.
- Contenido: es el ÚNICO apartado donde puedes poner información distinta y complementaria a la guía.
  Investiga en internet y enriquece con ángulos, datos, contexto, cifras o casos de ingeniería industrial,
  sin repetir literalmente el desarrollo del contenido de mi guía. Aquí van los elementos interactivos.
- Evaluación: constrúyela tú desde cero (mi guía no la trae), con al menos 5 preguntas de selección
  múltiple de dificultad progresiva.

IMPORTANTE: el OVA NUNCA debe mencionar la guía ni comparar ambos recursos.
El estudiante lo vive como un recurso natural.

Información del OVA:
- Materia: [Ej: Cálculo / Estadística / Procesos de Manufactura / Logística]
- Semestre: [Ej: Semestre 1]
- Programa: Ingeniería Industrial
- Nivel: Pregrado
- Imágenes QR de recursos: [lista los nombres de archivo, ej: img/qr-recurso-1.png]

Actividades interactivas que quiero (con gamificación obligatoria):
- [Ej: Sistema de puntos acumulables por respuesta correcta]
- [Ej: Misión de optimización con variables reales]
- [Ej: Calculadora o simulador de indicadores]
- [Ej: Quiz con puntaje final]

MI GUÍA DE APRENDIZAJE:
---
[PEGA AQUÍ EL CONTENIDO DE TU GUÍA EN MARKDOWN]
---

Usa como base el template/index.html de Pregrado/Industrial.
Genera el HTML completo listo para usar.
```

---

## Ejemplo de guía de aprendizaje

```markdown
# Funciones lineales en la optimización

## Introducción
Las funciones lineales son la base para modelar procesos productivos y tomar decisiones de optimización en contextos industriales.

## Objetivos
- Identificar el comportamiento de una función lineal.
- Aplicar funciones lineales a escenarios de producción.
- Resolver problemas de optimización básicos.

## Contenido
### Definición de función lineal
y = mx + b; interpretación de pendiente e intercepto.

### Aplicaciones industriales
Costos, ingresos y punto de equilibrio.

## Actividades
- Misión: calcular el punto de equilibrio de un proceso productivo.
- Simulador: variar la producción y observar el beneficio.

## Recursos
1. Khan Academy — Funciones lineales — https://es.khanacademy.org/math/algebra

## Bibliografía
- Stewart, J. (2012). Cálculo de una variable. Cengage Learning.
```

---

## Consejos importantes

- Recuerda el mapeo de secciones: Introducción, Objetivos, Actividades, Recursos y Bibliografía se mantienen; Contenido es complementario; Evaluación es nueva.
- Pide gamificación explícitamente: misiones, puntos, insignias.
- Pide a la IA que investigue en internet para enriquecer el contenido con casos industriales reales.
- Los recursos externos se activan mediante cards azules. No uses iframes.
- Nunca le pidas que cambie el sidebar, el footer de créditos ni el plugin de accesibilidad.
- Si algo no se ve bien, dile: *"Corrige [lo que está mal] siguiendo la paleta azul/naranja del template de Pregrado/Industrial"*.

---

## Prompt para corregir un OVA existente

```
Tengo este OVA y necesito corregir lo siguiente: [describe el problema].
Usa la identidad visual azul marino + naranja/ámbar del context.md de Pregrado/Industrial.
No modifiques el sidebar, los créditos ni el plugin de accesibilidad.

[PEGA EL HTML DEL OVA]
```

---

## Lista de verificación antes de usar el OVA

- [ ] Logo en `img/logo.svg`
- [ ] Las 7 secciones: Introducción, Objetivos, Contenido, Actividades, Evaluación, Recursos, Bibliografía
- [ ] Al menos 1 elemento interactivo por sección de contenido
- [ ] Cards de recursos externos activadas (botón con URL real y sin `opacity-50`)
- [ ] Quiz funcional en la sección Evaluación
- [ ] Imágenes QR en `img/` para cada recurso
- [ ] Footer con créditos de Ing. Ivan D. Mejia Segura
- [ ] Plugin de accesibilidad como último script: `<script src="https://elens.ecodestudio.dev/elens.js"></script>`
