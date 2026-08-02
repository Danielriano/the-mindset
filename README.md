# MNDST · The Mindset — linktree

Sitio estático de una sola página. Dominio: **themindst.com**

Sin build, sin dependencias. Lo que está en este repo es exactamente lo que se publica.

## Previsualizar en local

```bash
python3 -m http.server 8001
```

Abrir <http://localhost:8001>

## Publicar

```bash
git add -A && git commit -m "descripción del cambio" && git push
```

Hostinger publica solo en menos de 10 segundos.

## Diseño

Paleta del cliente: carbón `#222831`, turquesa `#00ADB5`, verde turquesa `#00AD85`. Todo vive en las variables de `:root` en `css/style.css`.

El lema del logo ("Programa tu cuerpo. Domina tu mente.") está como texto vivo, no como imagen, y conserva el mismo quiebre de color que el logo original: primera mitad en claro, segunda en turquesa.

### Nota técnica sobre el logo

Ninguno de los archivos entregados traía el isotipo recortado: `fondoblanco.PNG` es el logo sobre blanco sólido y `logosolooscuro.PNG` tiene canal alpha pero fondo negro opaco. Se resuelve con `mix-blend-mode: screen`, que disuelve el negro contra el fondo oscuro y deja solo el trazo, aprovechando el brillo y el reflejo que la imagen ya trae.

**Si aparece el vector original (SVG o AI), vale la pena cambiarlo:** el PNG pesa 213 KB de los 224 KB del sitio. En SVG serían ~2 KB, y el `mix-blend-mode` dejaría de ser necesario.

## Enlaces que ya funcionan

| Botón | Destino |
|---|---|
| Reprograma tu cerebro — Mujeres | pay.hotmart.com/B106990362O (40% fundadores) |
| Reprograma tu cerebro — Hombres | pay.hotmart.com/B106989870G (40% fundadores) |
| Training Athletic Club | dash.fitmewise.com (46% OFF) |
| Servicio VIP trimestral | dash.fitmewise.com |
| Julian Fitrainer | julianfitrainer.com |
| Instagram | @themindst |
| TikTok | @themnset |


## Oferta de fundadores

Los dos enlaces de Hotmart apuntan hoy a la oferta de **primera generación, 40% fundadores** (parámetro `?off=` en la URL). Cuando esa tanda cierre hay que reemplazarlos por los enlaces a precio completo y quitar la etiqueta `40% fundadores` del bloque `.grupo__cabecera` en `index.html`.

## Pendiente menor

- [ ] `og-image` propio de 1200×630 para cuando se comparta el link.

Los archivos originales sin optimizar están en `../_originales/`, fuera del repo, para que no se publiquen.
