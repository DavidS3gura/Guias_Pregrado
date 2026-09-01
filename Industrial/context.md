# Contexto del Proyecto: OVAs Pregrado — Ingeniería Industrial

## Descripción general

Este repositorio contiene **Objetos Virtuales de Aprendizaje (OVAs)** interactivos en formato web para estudiantes de **pregrado** del programa de **Ingeniería Industrial**. Cada OVA es una página HTML autocontenida que aborda un tema específico combinando conceptos clave, elementos visuales interactivos y actividades prácticas, organizados por semestre y unidad temática.

> ⚠️ **Independencia visual:** Esta carpeta (`Pregrado/Industrial`) usa una **identidad visual propia e independiente**, sin relación con plantillas o repositorios institucionales anteriores. No se deben copiar ni mezclar colores, logotipo ni estilos ajenos.

---

## Audiencia objetivo

Los OVAs están diseñados para **estudiantes universitarios de pregrado**. Por esto:

- Se puede usar un lenguaje más técnico que en el nivel técnico, pero debe seguir siendo claro, directo y motivador.
- Los ejemplos deben estar **contextualizados a escenarios reales de la ingeniería industrial**: procesos productivos, logística, calidad, operaciones, manufactura, sostenibilidad.
- El tono es de acompañamiento profesional: cercano, pero con la seriedad del nivel universitario.
- Los emojis se usan de forma **moderada y funcional** para destacar conceptos clave, no para infantilizar el contenido.

---

## Filosofía de diseño del contenido

Los OVAs son **guías prácticas**, no libros de teoría:

- Usar la **menor cantidad de texto posible**. El texto extenso solo está justificado para la definición o fundamentación de un concepto.
- Priorizar: ejemplos visuales, elementos interactivos, actividades con clicks, tablas, comparaciones rápidas y simulaciones.
- El estudiante debe **hacer** más de lo que lee: responder, arrastrar, seleccionar, ejecutar, calcular, explorar.
- Cada sección debe invitar al usuario a interactuar antes de explicar.

---

## Relación con la guía de aprendizaje del curso

El OVA se construye a partir de la guía de aprendizaje del curso. El mapeo de secciones es obligatorio:

- **Introducción, Objetivos, Actividades, Recursos y Bibliografía → SE MANTIENEN.** Reflejan el contenido de la guía: mismos objetivos, actividades, recursos/anexos y bibliografía. Se adaptan al formato web interactivo, pero su **sustancia es la misma**.
- **Contenido → ES EL ÚNICO APARTADO QUE PUEDE (Y DEBE) CONTENER INFORMACIÓN DIFERENTE Y COMPLEMENTARIA** a la guía. Aquí se amplía el tema con ángulos, datos, contexto, cifras, casos o profundizaciones, sin repetir literalmente el "Desarrollo del contenido" de la guía.
- **Evaluación → ES COMPLETAMENTE NUEVA.** La guía no la incluye. Se construye con mínimo 5 preguntas de selección múltiple de dificultad progresiva.

**Regla de tono (obligatoria):** el OVA **nunca debe hacer referencia a la guía de aprendizaje ni comparar ambos recursos**.

---

## Identidad visual de Industrial Pregrado

### Paleta de colores

| Rol | Color Tailwind | Hex | Uso |
|-----|----------------|-----|-----|
| Primario | `teal-900` | `#134e4a` | Títulos principales, borde del logo, sidebar activo |
| Secundario | `teal-600` | `#0d9488` | Enlaces, botones principales, acentos |
| Acento | `rose-500` | `#f43f5e` | Destacados, insignias, gamificación, llamados a la acción |
| Fondo claro | `slate-50` | `#f8fafc` | Fondo general |
| Fondo acento | `rose-50` | `#fff1f2` | Cajas motivacionales y de gamificación |
| Borde acento | `rose-300` | `#fda4af` | Bordes de recursos y actividades |
| Éxito | `green-700` | `#15803d` | Respuestas correctas en quiz |
| Error | `red-600` | `#dc2626` | Respuestas incorrectas en quiz |

### Logo

- **Archivo:** `img/logo.svg` (en cada carpeta `img/` del OVA).
- **Dimensiones desktop:** 150×150 px con borde redondeado de 2 px en `rose-500`.
- **Dimensiones mobile:** 100×100 px.
- Si el logo oficial no está disponible, se mantiene el `logo.svg` de la plantilla como referencia. No usar logotipos de otros repositorios.

### Tipografía

- **Inter** (Google Fonts), pesos 400, 500, 600, 700.
- Tamaños de encabezado conservados del template.

---

## Estructura de cada OVA

- **Sidebar de navegación** (desktop) con logo circular y enlaces por sección.
- **Menú desplegable** (mobile) con logo reducido.
- **Secciones estándar:** Introducción, Objetivos, Contenido, Actividades, Evaluación, Recursos, Bibliografía.
- **Elementos interactivos** según la materia: consolas de código, simuladores, cuestionarios, arrastrar y soltar, calculadoras, gráficos, planillas.
- **Acordeones** para organizar el contenido y evitar muros de texto.
- **Actividades prácticas** que requieren interacción del usuario en cada sección.

---

## Tecnologías usadas

- **HTML + TailwindCSS** (via CDN) para layout y estilos.
- **JavaScript vanilla** para interactividad.
- **Google Fonts (Inter)** para tipografía.
- Imágenes en formato `.webp` o `.svg`.

---

## Reglas para interactividad (OVAs de programación)

Cuando el OVA incluye playgrounds de código JavaScript/React:

1. **NO usar JSX directamente** en playgrounds.
2. Simular conceptos de React con **JavaScript puro válido**.
3. Mostrar JSX como **strings con template literals**.
4. Garantizar que el código **se ejecute sin errores** cuando el estudiante presione "Ejecutar".

Para otras materias, los elementos interactivos deben igualmente funcionar sin errores y dar retroalimentación inmediata.

---

## Estructura del repositorio

```
Pregrado/Industrial/
├── template/                    # Plantilla vacía oficial
│   └── index.html
├── README.md
├── context.md
└── semestre_<N>/
    └── <materia>/
        └── [unidad_<N>/]
            └── <tema-del-ova>/
```

---

## Reglas para crear nuevos OVAs

### Lo que NO se puede modificar

- **Estructura base:** el layout (sidebar + contenido principal + mobile header) no se toca.
- **Estilos y diseño base:** los colores de la paleta, tipografía (Inter), espaciados, clases de TailwindCSS estructurales y esquema visual general deben mantenerse.
- **Logo:** el logo circular en el sidebar desktop no se modifica en posición, tamaño ni estilo.
- **Iconos y elementos estructurales:** los iconos de navegación del menú lateral y mobile no se cambian.
- **Secciones estándar:** las 7 secciones deben estar presentes siempre.
- **Créditos a Ing. Ivan D. Mejia Segura:** son obligatorios en cada OVA.

### Sección de Recursos (estructura intocable)

La sección de **Recursos** mantiene esta estructura HTML fija. Solo se reemplazan datos:

```html
<li class="bg-white p-4 rounded-lg shadow-md hover:shadow-lg transition-shadow border-l-4 border-rose-500 flex flex-col sm:flex-row sm:items-center justify-between">
    <div>
        <h3 class="font-bold text-teal-900">[Nombre del recurso]</h3>
        <p class="text-slate-600 mb-2">[Descripción breve]</p>
        <a href="[URL]" target="_blank" class="underline text-slate-700 hover:text-teal-700">Ir al recurso</a>
    </div>
    <div class="mt-4 sm:mt-0 sm:ml-6 flex-shrink-0">
        <div class="bg-rose-50 border border-rose-300 rounded flex items-center justify-center" style="width:2cm;height:2cm;">
            <img src="img/[nombre-qr].png" alt="QR [Nombre del recurso]" class="max-w-full max-h-full object-contain" loading="lazy">
        </div>
    </div>
</li>
```

### Lo que SÍ se puede (y debe) personalizar

- **Sección de Contenido:** libre para adaptarse al tema.
- **Sección de Actividades:** libre para diseñar las actividades prácticas.

### Gamificación (obligatoria en Contenido y Actividades)

Las secciones de **Contenido** y **Actividades** deben aplicar estrategias de gamificación:

- Sistema de puntos o estrellas.
- Retroalimentación inmediata con refuerzo positivo.
- Niveles o progreso visible.
- Retos y mini-misiones.
- Revelación progresiva.
- Temporizador opcional.
- Tabla de logros o insignias.

**Límite obligatorio:** toda mecánica de gamificación debe estar **contenida dentro de la sección Contenido o Actividades**. Ninguna estrategia puede modificar el layout global del OVA.

### Recursos externos multimedia

Cuando el contenido de un acordeón se beneficiaría de un video, simulador u otro recurso externo, la IA **debe** insertar una card de recurso externo. **Nunca** incrustar un `<iframe>` de YouTube ni inventar URLs.

Reglas:

1. Cada card tiene un `id` único e incremental: `recurso-ext-1`, `recurso-ext-2`, etc.
2. El botón nace desactivado (`href="#"`, con clases `opacity-50 cursor-not-allowed`).
3. La card muestra un mensaje ejemplo para que el docente sepa qué decirle al agente de IA en el chat.
4. **La card usa la paleta teal/rose de Industrial:** `bg-teal-50`, `border-teal-300`, botón `bg-teal-600`.
5. La IA incluye en el comentario HTML encima de cada card el tema y términos de búsqueda sugeridos.

### Plugin de accesibilidad (obligatorio)

Todo OVA generado debe incluir el siguiente script **antes del cierre de `</body>`**:

```html
<script src="https://elens.ecodestudio.dev/elens.js"></script>
```

Este plugin no se debe omitir, modificar ni mover de posición. No agregar controles de voz propios.

### Proceso para crear un nuevo OVA

1. Tomar como base la carpeta `template/`.
2. Copiarla y renombrarla según el tema.
3. Reemplazar el contenido de las secciones **Contenido** y **Actividades**, siguiendo las reglas de gamificación.
4. Verificar que el logo, créditos, navegación y estilos globales permanezcan intactos.
5. Ajustar los textos de navegación solo si el tema lo requiere, sin alterar el estilo visual.
