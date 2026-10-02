# Web personal de Sergio Esteban Bruña

Web estática inspirada en la estructura académica y minimalista de seigal.github.io, pero con contenido, estilo y jerarquía propios.

## Archivos

- `index.html`: contenido de la página.
- `styles.css`: diseño responsive.
- `script.js`: actualiza automáticamente el año del pie.
- `.nojekyll`: evita procesamiento innecesario de Jekyll en GitHub Pages.

## Verla en tu ordenador

La forma más simple es abrir `index.html` con el navegador.

También puedes levantar un servidor local:

```bash
python -m http.server 8000
```

Después abre `http://localhost:8000`.

## Publicarla en GitHub Pages

### Opción recomendada: repositorio `<tu-usuario>.github.io`

1. Entra en https://github.com e inicia sesión.
2. Pulsa **New repository**.
3. Nombra el repositorio exactamente `<tu-usuario>.github.io`. Por ejemplo, si tu usuario fuera `sergioeb`, sería `sergioeb.github.io`.
4. Déjalo como **Public** y crea el repositorio.
5. Dentro del repositorio, pulsa **Add file → Upload files**.
6. Sube `index.html`, `styles.css`, `script.js` y `.nojekyll`.
7. Pulsa **Commit changes**.
8. Ve a **Settings → Pages**.
9. En **Build and deployment**, selecciona **Deploy from a branch**.
10. Elige la rama `main` y la carpeta `/ (root)`, y pulsa **Save**.
11. Tu web quedará publicada en `https://<tu-usuario>.github.io/`.

### Si quieres usar un repositorio con otro nombre

Puedes llamarlo, por ejemplo, `personal-website`. Sigue los mismos pasos y GitHub Pages publicará normalmente la web en:

`https://<tu-usuario>.github.io/personal-website/`

## Cómo editar el contenido

Abre `index.html` con VS Code o cualquier editor de texto.

Busca estas secciones:

- `id="bio"`
- `id="areas"`
- `id="formacion"`
- `id="proyectos"`
- `id="writing"`
- `id="reconocimientos"`
- `id="contacto"`

Modifica solo el texto entre las etiquetas HTML. Después vuelve a subir el archivo cambiado a GitHub y haz commit.

## Añadir tu foto

1. Crea una carpeta llamada `assets`.
2. Guarda tu foto como `assets/profile.jpg`.
3. En `index.html`, sustituye:

```html
<div class="portrait" aria-label="Iniciales de Sergio Esteban Bruña" role="img">SEB</div>
```

por:

```html
<img class="portrait portrait-photo" src="assets/profile.jpg" alt="Sergio Esteban Bruña" />
```

4. Añade al final de `styles.css`:

```css
.portrait-photo {
  object-fit: cover;
  display: block;
}
```

## Añadir email y GitHub

En `index.html`, busca la sección `id="contacto"`. Puedes añadir:

```html
<a href="mailto:tuemail@dominio.com">tuemail@dominio.com</a>
<a href="https://github.com/TU-USUARIO" target="_blank" rel="noreferrer">GitHub ↗</a>
```

## Dominio propio (opcional)

Si más adelante compras un dominio, por ejemplo `sergioesteban.dev`, ve a **Settings → Pages → Custom domain**, introduce el dominio y sigue las indicaciones DNS de GitHub.

## Contenido a completar

La web evita inventar datos no visibles públicamente. Te recomiendo completar:

- Experiencia profesional / empresa actual.
- Grado, universidad y fechas exactas.
- Máster de Inteligencia Artificial y universidad, si quieres hacerlo público.
- Proyectos de GitHub o TFM.
- Email profesional.
- Usuario de GitHub.
- Foto de perfil.
