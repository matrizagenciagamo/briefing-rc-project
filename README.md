# Briefing web RC Project · GAMO Agencia Creativa

Landing/formulario estático para publicar en GitHub Pages y recibir las respuestas por email mediante FormSubmit.

## Archivos

- `index.html`: landing + formulario completo.
- `gracias.html`: página de confirmación opcional.

## Email de recepción

El formulario está configurado para enviar las respuestas a:

`alberto@agenciagamo.es`

Para cambiarlo, edita esta línea en `index.html`:

```html
<form action="https://formsubmit.co/alberto@agenciagamo.es" method="POST" enctype="multipart/form-data">
```

Sustituye el email por el correo definitivo de GAMO.

## Publicación rápida en GitHub Pages

1. Entra en GitHub y crea un repositorio nuevo, por ejemplo: `briefing-rc-project`.
2. Sube `index.html` y `gracias.html` a la raíz del repositorio.
3. Entra en `Settings` → `Pages`.
4. En `Build and deployment`, selecciona `Deploy from a branch`.
5. Elige rama `main` y carpeta `/root`.
6. Guarda.
7. GitHub generará una URL similar a:

`https://TU-USUARIO.github.io/briefing-rc-project/`

## Activar recepción por email

La primera vez que se envíe el formulario, FormSubmit enviará un email de verificación al correo receptor. Hay que abrir ese correo y confirmar la activación. A partir de ahí, los briefings llegarán al email.

## Página de gracias

Por defecto, FormSubmit puede mostrar su propia página de confirmación. Si quieres redirigir a `gracias.html`, cuando ya tengas la URL pública añade este campo dentro del `<form>` en `index.html`:

```html
<input type="hidden" name="_next" value="https://TU-USUARIO.github.io/briefing-rc-project/gracias.html">
```

## Dominio personalizado

Se puede configurar un subdominio tipo:

`briefing.gamoestudio.es`

Para ello, configura GitHub Pages con dominio personalizado y ajusta los DNS del dominio.

## Nota sobre PDF

Esta versión prioriza rapidez: las respuestas llegan al email en formato tabla y pueden incluir archivos adjuntos. Para generar automáticamente un PDF maquetado por cada respuesta haría falta una automatización adicional con Make, Apps Script, Zapier o similar.
