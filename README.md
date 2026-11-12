# Presentación — Transformación digital en el ámbito municipal (caso Pinamar)

Charla de 30 minutos. Francisco M. Montes, Secretario de Gobierno, Municipalidad de Pinamar.

## Cómo se usa

Abrir `index.html`. Es autocontenido: no carga nada de internet, así que funciona
igual sin conexión y en cualquier máquina prestada.

| Tecla | Qué hace |
|---|---|
| `→` / `espacio` | Siguiente |
| `←` | Anterior |
| `N` | Muestra u oculta las notas del orador con los tiempos |
| `F` | Pantalla completa |
| `Home` / `End` | Primera / última |

También anda con clicks (mitad derecha avanza) y con swipe en celular.
El número de slide queda en la URL, así que se puede saltar directo con `#14`.

## Los GIFs

Cada hueco pendiente está marcado en el HTML con `data-gif`:

| id | Qué va | Dónde se graba |
|---|---|---|
| `01-templates` | Edición de template de notificación | Backoffice |
| `02-consulta` | Consulta en lenguaje natural | Puede ir en vivo |
| `03-paneles` | Paneles de Hacienda y Salud | Captura estática |
| `04-alta-utv` | Alta completa de UTV punta a punta | Staging, datos ofuscados |

Para colocar uno: dejar el archivo en `gifs/<id>.gif` y reemplazar el contenido
del `div.gifslot` por `<img src="gifs/<id>.gif" alt="">`.

## Publicar en GitHub Pages

```bash
git init && git add -A && git commit -m "Presentación caso Pinamar"
gh repo create presentacion-pinamar --public --source=. --push
gh api -X POST repos/:owner/presentacion-pinamar/pages \
  -f 'source[branch]=main' -f 'source[path]=/'
```

Ojo: GitHub Pages sobre repo público es público e indexable. El `index.html` ya
lleva `noindex`, pero eso evita el buscador, no el acceso directo por URL.

## Tiempos

| Bloque | Desde | Duración |
|---|---|---|
| Apertura | 0:00 | 3 min |
| Cap. 1 — De reactivo a proactivo | 3:00 | 8 min |
| Cap. 2 — Información para decidir | 11:00 | 7 min |
| Cap. 3 — Trámites que nacen digitales | 18:00 | 9 min |
| Cierre | 27:00 | 3 min |
