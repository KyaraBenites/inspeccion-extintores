# Inspección mensual de extintores · QHSE

Aplicación estática para GitHub Pages. Funciona en laptop y celular; no requiere servidor ni base de datos para el uso individual.

## Publicar en GitHub Pages

1. Crea un repositorio público en github.com (por ejemplo `inspeccion-extintores`).
2. Extrae este ZIP y **sube los archivos `index.html`, `styles.css`, `app.js` y `logo-sde.png` a la raíz** del repositorio. No subas solamente el ZIP.
3. En GitHub ve a **Settings → Pages → Build and deployment → Source: Deploy from a branch**.
4. Elige **main** y **/(root)**, luego guarda.
5. El enlace público será `https://TU-USUARIO.github.io/inspeccion-extintores/` (ajusta el usuario y repositorio). Permanecerá mientras mantengas la publicación.

## Funcionalidades

- 45 filas precargadas como referencia visual del formato SDE-QHE-FOR-018; textos editables, comprobables antes de uso oficial.
- 14 casillas de inspección por extintor, observaciones libres y varias imágenes con captura desde cámara.
- En celular se muestran tarjetas; en computadora una tabla de desplazamiento horizontal y vista alternativa de fichas.
- Guardado automático del avance en IndexedDB local, borradores, finalización e historial por navegador/dispositivo.
- Exportar para impresión/PDF desde el navegador, documento `.doc` compatible con Word, imágenes PNG separadas en bloques de 7 extintores, respaldo e importación JSON.

## Avisos importantes

- **GitHub Pages solo publica la aplicación, no sincroniza los registros**: cada navegador mantiene su propio historial local. Para transferir a otro dispositivo, usa Exportar/Importar JSON. Si se borran los datos del navegador, el historial local puede perderse.
- La conversión PNG carga `html2canvas` desde CDN y requiere conexión a Internet. Las demás funciones no requieren conexión después de abrir la web, siempre que los archivos sigan disponibles en la caché del navegador (no incluye modo offline garantizado).
- El archivo Word es `.doc` basado en HTML compatible con Microsoft Word, **no `.docx` nativo**. Para generar PDF, usa el diálogo de impresión: selecciona «Guardar como PDF».
- Las ubicaciones y características transcritas de una captura de pantalla deben cotejarse con el formato maestro antes de usarlo como documento controlado. La captura no muestra con precisión suficiente todos los datos de cada extintor.
- Uso en campo: realiza un respaldo JSON al terminar cada jornada. Para almacenamiento centralizado multiusuario entre celulares se requiere un backend con autenticación (por ejemplo Firebase/Supabase) y reglas de seguridad, no incluido en esta versión estática.

## Actualización: logo y nuevas filas
- Se incluye el logo SDE proporcionado en la cabecera de la aplicación y en las exportaciones Word/PDF/PNG.
- Se pueden añadir una fila o múltiples filas (hasta 500 por operación), sin límite fijo de 45 extintores.
- La tabla en laptop incluye barras horizontales visibles arriba y abajo y admite desplazamiento con teclado; en celular se muestran fichas. La tecla espacio escribe normalmente en campos y observaciones.
