# Versión 3 — curso organizado en módulos + navegación del juego

## Qué cambié esta vez

1. **Descubrí que el curso original tenía todo duplicado 4 veces** en Moodle (parece que se restauró/importó varias veces sobre el mismo curso sin querer). Limpié eso — antes tenías 56 "secciones" repetidas y confusas, ahora son **7 módulos reales**, sin duplicados.

2. **Anidé correctamente las subsecciones** dentro de sus módulos (antes se mostraban todas sueltas al mismo nivel, por eso se veía tan plano y largo).

3. **Rediseñé `/curso`**: ahora es una cuadrícula de 7 tarjetas grandes (una por módulo), con número, nombre y cantidad de contenido. Haces clic en una y se expande mostrando su contenido organizado (con las subsecciones agrupadas visualmente).

4. **Limpié el estilo del contenido pegado desde Word** — antes se veía con fuentes raras (Times New Roman mezclada con el tema oscuro); ahora todo el texto usa la tipografía consistente de la plataforma.

5. **Agregué navegación al juego**: una barra fija arriba con "← Volver al dashboard" y "🔄 Reiniciar", un indicador de "Paso 1 de 2 · Clasificación" que cambia a "Paso 2 de 2 · Construcción", y en la pantalla final ahora hay dos botones: "Jugar de nuevo" y "Volver al dashboard".

6. Sobre el ejercicio de "rotación" que mencionaste: revisé el contenido original y **nunca tuvo una imagen** — es un tutorial de código para Unity, solo texto. No es un bug, así estaba armado desde Moodle.

## Cómo subir esta versión

Mismo proceso que la vez pasada (reemplazar archivos):

### Paso A
Descarga `entobio-plataforma-v3.zip` y descomprímelo en tu carpeta de Descargas.

### Paso B
1. Abre la carpeta de tu repositorio clonado (donde ya tienes todo desde la vez pasada).
2. Abre la carpeta nueva `entobio-plataforma-v3` descomprimida.
3. Selecciona todo adentro (Ctrl+A), copia (Ctrl+C).
4. Pégalo (Ctrl+V) dentro de la carpeta del repositorio, dile que sí a "Reemplazar los archivos".
5. Espera a que termine de copiar.

### Paso C
1. Abre GitHub Desktop.
2. En "Summary", escribe: `Curso reorganizado en modulos, sin duplicados, navegacion del juego`
3. Clic en **"Commit to main"**.
4. Clic en **"Push origin"**.
5. Espera a que suba (puede tardar varios minutos).

### Paso D
Ve a Render → tu servicio → pestaña **"Logs"** → espera "Your service is live" (el redeploy es automático).

### Paso E — Probar
1. Entra a tu plataforma, ve al curso.
2. Deberías ver 7 tarjetas de módulo, no una lista larga.
3. Entra a un módulo, confirma que el contenido se ve limpio y organizado.
4. Entra al juego, confirma que aparece la barra de navegación arriba.

---

Avísame en qué paso vas, o si algo se ve distinto a lo que describo.
