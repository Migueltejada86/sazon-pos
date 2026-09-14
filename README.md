# Sazón POS

Prototipo de punto de venta para **El Descanso** (y el segundo local, cuentas separadas).

Repo: https://github.com/Migueltejada86/sazon-pos

Demo (cuando Pages esté activo):

- Caja: https://migueltejada86.github.io/sazon-pos/
- Mozo: https://migueltejada86.github.io/sazon-pos/mozo.html

## Activar GitHub Pages

1. Repo → **Settings** → **Pages**.
2. Source: **GitHub Actions** (hay workflow `pages.yml`) **o** Branch `main` / folder `/ (root)`.
3. Esperá 1 minuto.

## Subir el prototipo desde la PC

El HTML grande vive en el proyecto (`artifacts/sazon/`). En una terminal:

```bash
git clone https://github.com/Migueltejada86/sazon-pos.git
cd sazon-pos
# copiá index.html, app.js y js/ desde artifacts/sazon
git add index.html app.js js mozo.html
git commit -m "Prototipo caja + app mozo"
git push origin main
```

## Qué hay hoy

- Plano de mesas de El Descanso
- Abrir mesa → carta → bandeja amarilla → confirmar
- Ticket 80 mm XP-E200M (no fiscal)
- Cierre de caja de noche + abrir a la mañana con fondo
- Datos en localStorage de ese navegador

Dos PCs todavía no comparten mesas (eso va en DonWeb).
