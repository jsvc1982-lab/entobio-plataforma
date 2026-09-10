# Versión 4 — arreglé los 3 problemas que reportaste

## 1. "Contenidos Temáticos" en blanco → ahora es un índice de módulos (tu idea de la "escalera")

Esa sección en el Moodle original solo contenía un contenedor vacío llamado "MODULOS" (sin nada adentro — así estaba en el curso real, no era un bug de copiado). En vez de mostrarlo vacío, ahora esa sección muestra una lista con los módulos reales (1, 2, 3, 4...) — haces clic en cualquiera y te lleva directo a él.

## 2. "Enlace de guía de insectos" → Not Found → arreglado de raíz

El nombre original del archivo tenía tildes, espacios y paréntesis (`Manual-de-identificaciòn-de-Insectos-Arañas...(1).pdf`), lo cual puede romperse al copiarse en Windows o en URLs. La vez pasada lo arreglé a mano, pero al regenerar el curso completo se me olvidó y volvió el nombre problemático.

Esta vez lo arreglé **en el programa que genera el curso**, no a mano — así que aunque vuelva a regenerar todo en el futuro, cualquier archivo con nombre problemático se renombra automáticamente a algo simple y seguro (ejemplo: `manual-de-identificacion-de-insectos-aranas-y-otros-artropod.pdf`).

## 3. Módulo 2 — imagen del visor de rotación (label) no cargaba → arreglado

Encontré la causa real: esa imagen no usa el sistema normal de Moodle para referenciar archivos — usa uno especial (`$@PLUGINFILEBYCONTEXT@$`) que se usa específicamente en visores interactivos de 360°/sliders. Mi programa solo sabía reconocer el formato normal; le agregué soporte para este formato especial también. Ahora las imágenes "Vista Lateral", "Vista Dorsal" y "Vista Frontal" del visor 360° del Módulo 2 cargan correctamente.

**Extra:** gracias a este arreglo, en total ahora se resuelven **40 archivos** (antes 28) — o sea que probablemente había más imágenes rotas por este mismo motivo en otras partes del curso que ni siquiera habías notado todavía.

---

## Cómo subir esta versión

Exactamente el mismo proceso de siempre:

### Paso A
Descarga `entobio-plataforma-v4.zip` y descomprímelo.

### Paso B
1. Abre tu carpeta del repositorio clonado (la de siempre).
2. Abre la carpeta nueva descomprimida.
3. Selecciona todo (Ctrl+A), copia (Ctrl+C).
4. Pégalo en la carpeta del repositorio, dile que sí a "Reemplazar los archivos".
5. Espera a que termine.

### Paso C
1. GitHub Desktop → Summary: `Arreglo de imagenes de rotacion, nombre de archivo seguro, e indice de modulos`
2. **"Commit to main"**
3. **"Push origin"**
4. Espera a que suba.

### Paso D
Render redespliega solo — espera "Your service is live" en Logs.

### Paso E — Probar los 3 puntos específicos
1. Entra a **"Contenidos Temáticos"** → deberías ver la lista de módulos, no vacío.
2. Entra a **Módulo 1** → "GUIA IDENTIFICACION DE INSECTOS" → debería descargar/abrir el PDF sin error.
3. Entra a **Módulo 2** → busca el visor de rotación → mueve el control deslizante → la imagen debería aparecer y rotar.

Avísame cómo te fue con estos tres, o si aparece algo más.
