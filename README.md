# Sazón POS

Prototipo de punto de venta para **El Descanso** (y el segundo local, cuentas separadas).

Demo en GitHub Pages:

- Caja / escritorio: https://migueltejada86.github.io/sazon-pos/
- App mozo (celular): https://migueltejada86.github.io/sazon-pos/mozo.html

Marca propia Sazón. No usa Fudo.

## Qué hay hoy

Un HTML único (`index.html`) con:

- Plano de mesas (Galería, Salón, Patio, Extras, Frente, Pileta)
- Abrir mesa → carta → bandeja amarilla → confirmar
- Ticket 80 mm para Xprinter XP-E200M (no fiscal)
- Cierre de caja de noche (corte por medio, efectivo contado, diferencia)
- Abrir caja a la mañana con fondo
- Persistencia en `localStorage` de este navegador

Todavía no hay servidor ni cuentas por local. Dos PCs no ven las mismas mesas.

## Estructura del repo

```
sazon-pos/
├── index.html      # caja + backoffice + carta
├── mozo.html       # entra directo a la app del mozo
├── .nojekyll       # GitHub Pages sirve el HTML tal cual
└── README.md
```

Estructura objetivo cuando suba a DonWeb (no está en Pages):

```
apps/caja  apps/mozo  apps/cocina  apps/admin
server/    db/        shared/      deploy/
```

Un servidor, dos tenants: `descanso` y el local nuevo.

## Uso rápido

1. Abrí la demo de caja.
2. Mesas → abrir → cargar código (01, 20, 501…) → Confirmar → Ticket y cerrar.
3. Ícono reportes / Ventas → Arqueos → cierre de noche.
4. En el celu: `/mozo.html`.

## Stack futuro

Ubuntu + Node + PostgreSQL en Cloud Server DonWeb (Argentina). Pages es solo la maqueta pública.
