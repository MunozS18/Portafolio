# Portafolio

Portafolio personal en un solo archivo. Sin frameworks, sin build, sin dependencias.

## 1. Personalizar

Abre `index.html` y busca el bloque marcado como **ZONA EDITABLE** (cerca del final, dentro de `<script>`). Ahí está todo tu contenido en un objeto `DATA`:

| Campo | Qué poner |
|---|---|
| `perfil` | Nombre, rol, pitch, correo, GitHub, LinkedIn, ruta del CV |
| `cifras` | 3 o 4 números verificables que te describan |
| `bio` | Dos párrafos sobre cómo trabajas |
| `stack` | Tecnologías agrupadas por categoría |
| `proyectos` | Un bloque por proyecto — duplica uno para agregar más |
| `trayectoria` | Formación y experiencia, de lo más reciente a lo más antiguo |

También cambia el `<title>`, la `<meta name="description">` y las etiquetas `og:` al inicio del archivo. Eso es lo que ve Google y lo que se muestra cuando compartes el link por WhatsApp o LinkedIn.

Todo el contenido está en español e inglés (`{ es: "...", en: "..." }`). El botón EN/ES del menú cambia el idioma sin recargar la página.

## 2. Imágenes y CV

Crea una carpeta `assets/` junto a `index.html`:

```
portafolio/
├── index.html
├── README.md
└── assets/
    ├── CV-TuNombre-ATS.pdf
    ├── foto.jpg
    ├── og.png          (1200x630, para redes sociales)
    ├── proyecto1.png
    └── proyecto2.png
```

Luego apunta las rutas en `DATA`: `foto: "assets/foto.jpg"`, `imagen: "assets/proyecto1.png"`, `cv: "assets/CV-TuNombre-ATS.pdf"`.

Las capturas de proyectos importan mucho. Un proyecto con captura se ve terminado; uno sin captura se ve como tarea.

## 3. Subir a GitHub

```bash
cd portafolio
git init
git add .
git commit -m "Portafolio inicial"
git branch -M main
git remote add origin https://github.com/TUUSUARIO/portafolio.git
git push -u origin main
```

## 4. Publicar con GitHub Pages

1. En el repositorio → **Settings** → **Pages**
2. En *Source* elige **Deploy from a branch**
3. Branch: `main`, carpeta: `/ (root)` → **Save**
4. En uno o dos minutos queda en `https://TUUSUARIO.github.io/portafolio/`

Si nombras el repositorio `TUUSUARIO.github.io`, la URL queda limpia: `https://TUUSUARIO.github.io`.

Para actualizar después: edita, `git add .`, `git commit -m "..."`, `git push`. Pages se redespliega solo.

## 5. Antes de enviarlo a un reclutador

- Abre el sitio en el celular y revisa que todo se lea bien.
- Verifica que el PDF del CV descargue y que todos los links de repos abran.
- Cada repositorio enlazado necesita su propio README con qué hace, cómo correrlo y una captura.
- Pon la URL del portafolio en tu CV, en tu LinkedIn y en la bio de tu perfil de GitHub.
