# LinguaStep A1 - Maquetación y Prototipo HTML / Tailwind

Este proyecto contiene la estructura HTML y assets extraída y organizada a partir del prototipo de Stitch (`cssTail.html`), preparada especialmente para su futura migración a componentes de **React**.

---

## 📁 Estructura del Proyecto (`Documents/avance2`)

```text
avance2/
├── index.html                  # Portada pública (Landing Page)
├── login.html                  # Autenticación (Login y Registro)
├── student-dashboard.html      # Panel principal del estudiante
├── lesson.html                 # Pantalla de lección interactiva (Números 1-10)
├── quiz-results.html           # Resultados del cuestionario / evaluación
├── teacher-dashboard.html      # Panel principal del docente
├── lesson-editor.html          # Editor y creador de lecciones para el profesor
├── question-management.html    # Gestión y banco de preguntas
├── teacher-progress.html       # Tabla de seguimiento y progreso de alumnos
├── README.md                   # Documentación del proyecto
└── assets/
    ├── font/                   # Tipografías locales / .gitkeep
    ├── css/
    │   └── styles.css          # Estilos globales, inputs, animaciones y Material Symbols
    ├── js/
    │   └── tailwind.config.js  # Configuración unificada de Tailwind (tokens de diseño)
    ├── img/                    # 14 imágenes descargadas localmente (avatares, portadas, miniaturas)
    ├── video/                  # Videos de lecciones / .gitkeep
    └── audio/                  # Audios de pronunciación / .gitkeep
```

---

## 🚀 Páginas Incluidas y Flujo de Navegación

1. **[index.html](file:///home/diedox/Documents/avance2/index.html)**:
   - Portada inicial con información del curso, Bento Grid de unidades, vista previa de metodología y pie de página.
   - Enlaces directos a "Sign In" y "Comenzar curso".
2. **[login.html](file:///home/diedox/Documents/avance2/login.html)**:
   - Formulario dual de Iniciar Sesión y Registro mediante pestañas interactivas.
   - Al enviar el formulario, redirige automáticamente al Dashboard del Estudiante.
3. **[student-dashboard.html](file:///home/diedox/Documents/avance2/student-dashboard.html)**:
   - Panel del alumno con resumen de progreso, Bento Grid de unidades y tabla de actividad reciente.
4. **[lesson.html](file:///home/diedox/Documents/avance2/lesson.html)**:
   - Vista de lección con contenido multimedia (imagen, audio simulado, video) y práctica interactiva con retroalimentación inmediata (Toast). Al acertar, avanza a los resultados.
5. **[quiz-results.html](file:///home/diedox/Documents/avance2/quiz-results.html)**:
   - Pantalla de puntaje (85%), desglose de respuestas correctas e incorrectas y opciones de reintento o regreso al panel.
6. **[teacher-dashboard.html](file:///home/diedox/Documents/avance2/teacher-dashboard.html)**:
   - Panel del docente con tarjetas de métricas, acceso rápido a creación de lecciones y tabla de lecciones activas.
7. **[lesson-editor.html](file:///home/diedox/Documents/avance2/lesson-editor.html)**:
   - Formulario completo para editar título, nivel, contenido multimedia, taxonomía y estado de publicación de lecciones.
8. **[question-management.html](file:///home/diedox/Documents/avance2/question-management.html)**:
   - Interfaz para crear preguntas de opción múltiple, listar preguntas existentes y modal animado de confirmación para eliminar.
9. **[teacher-progress.html](file:///home/diedox/Documents/avance2/teacher-progress.html)**:
   - Tabla detallada de estudiantes con filtros por unidad y estado, progreso porcentual y fechas de última actividad.

---

## ⚛️ Preparación para Migración a React

- **Etiquetas autocerradas (Self-closing tags):** Todos los elementos vacíos (`<img ... />`, `<input ... />`, `<br />`, etc.) están formateados con sintaxis autocerrada, garantizando compatibilidad directa con JSX.
- **Tokens de Diseño Unificados:** `assets/js/tailwind.config.js` contiene todos los colores (`primary`, `secondary`, `surface`, etc.), fuentes (`Plus Jakarta Sans`, `Atkinson Hyperlegible Next`), escalas de texto y espaciados listos para usarse tanto en navegador como en un archivo `tailwind.config.js` de Vite/Next.js/CRA.
- **Componentización:** Cada archivo incluye comentarios indicando la delimitación de bloques reutilizables (SideNavBar, Header, Bento Cards, Modales).
- **Recursos Locales:** Todas las imágenes están almacenadas en `assets/img/`, sin dependencias obligatorias de conexión externa para renderizar los elementos gráficos.
