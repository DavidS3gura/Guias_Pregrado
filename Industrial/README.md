# Pregrado — Ingeniería Industrial: OVAs Web

Repositorio de **Objetos Virtuales de Aprendizaje (OVAs)** interactivos en formato web, desarrollados para estudiantes de **pregrado** del programa de **Ingeniería Industrial**.

Cada OVA es una página HTML autocontenida con elementos visuales, actividades prácticas gamificadas e interactividad sin depender de frameworks externos. Esta carpeta usa una **identidad visual propia e independiente**, sin relación con plantillas o repositorios institucionales anteriores.

---

## Identidad visual

- **Nombre corto:** Industrial Pregrado
- **Colores institucionales:** verde azulado `#134e4a` y rosa `#f43f5e`
- **Tipografía:** Inter (Google Fonts)
- **Logo:** `template/img/logo.svg` (reemplazar por el logo oficial cuando esté disponible)
- **Estilo:** profesional, limpio, con acentos energéticos que evocan dinamismo e ingeniería.

> La identidad visual de este proyecto se mantiene independiente. No deben mezclarse los archivos ni las reglas de estilo con otros repositorios.

---

## Estructura del repositorio

```
Pregrado/
└── Industrial/
    ├── README.md               ← Estás aquí
    ├── context.md              ← Instrucciones para la IA (léelas antes de crear un OVA)
    ├── PROMPT_GUIDE.md         ← Guía paso a paso para crear OVAs con IA
    ├── template/               ← Plantilla vacía oficial con la identidad visual de Industrial
    │   ├── index.html
    │   └── img/
    │       └── logo.svg        ← Logo compartido por los OVAs de este programa
    └── semestre_<N>/
        └── <materia>/
            └── [unidad_<N>/]
                └── <tema-del-ova>/
                    ├── index.html
                    └── img/    ← Logo + imágenes QR de los recursos del OVA
```

> Los OVAs crecen agregando carpetas que sigan este patrón. No es necesario actualizar este README al añadir un nuevo semestre, materia o OVA.

---

## ¿Cómo crear un nuevo OVA con IA?

1. **Prepara tu carpeta:** copia `template/` completa (ya incluye `img/logo.svg`) y renómbrala según el tema.  
   Ejemplo: `semestre_1/calculo/unidad_1/funciones/`
2. **Prepara tu guía de aprendizaje** en Markdown con las secciones del OVA: Introducción, Objetivos, Contenido, Actividades, Recursos y Bibliografía.
3. **Dale el contexto a la IA:** dile que lea `context.md` de esta carpeta.
4. **Usa la plantilla de prompt** del archivo `PROMPT_GUIDE.md`.
5. **Activa los recursos externos** buscando las URLs y pidiéndole al agente que actualice las cards azules.

---

## ⚠️ Reglas importantes

- **NO** copiar la identidad verde de `p_tecnico`. Esta carpeta usa la paleta azul/naranja definida en `context.md`.
- **NO** modificar el layout base (sidebar, mobile header, footer de créditos).
- **Gamificación obligatoria** en Contenido y Actividades, contenida dentro de la sección donde aplica.
- **No incrustar iframes** de YouTube; usar las cards de recurso externo.
- **No agregar controles de voz propios**; el plugin de accesibilidad ya los incluye.
- **No omitir** el plugin de accesibilidad: `<script src="https://elens.ecodestudio.dev/elens.js"></script>`

---

## 👥 Créditos

**Ing. Ivan D. Mejia Segura**
