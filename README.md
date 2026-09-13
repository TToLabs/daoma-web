# DAOMA — descargas y respaldo web

Este repo es **público y de solo lectura por diseño**: es un espejo generado
a mano desde `Agenda Acupuntura` (privado), que es la única fuente de
verdad del código. Acá NUNCA se edita directo — todo cambio se hace en el
repo privado y se vuelve a copiar acá cuando se quiere publicar una
actualización.

Qué hay acá:
- `www/index.html` — web del paciente (respaldo si la app falla).
- `www/admin.html` — web del panel del acupunturista, con login (respaldo si la app falla).
- `www/img/` — fondos decorativos.
- `index.html` (raíz) — landing **pública, para pacientes**: web + APK.
  Deliberadamente NO enlaza a la página del panel.
- `admin.html` (raíz) — landing **separada, solo para el acupunturista**:
  web + APK. No está enlazada desde `index.html` ni indexada por buscadores
  (`robots.txt`, `<meta name="robots" content="noindex">`) — se comparte a
  mano, nunca con un paciente.
- Releases (tag `latest`) — los `.apk` de "DAOMA" (paciente) y "DAOMA
  Panel" (acupunturista), cuando existan. El link no cambia entre
  versiones, solo el archivo detrás (se actualiza con
  `gh release upload latest <archivo> --clobber`).

Qué NO hay acá (y nunca debe copiarse): `backend/Codigo.gs` ni ninguna API
key. El backend vive solo en Google Apps Script, dentro del proyecto
privado.
