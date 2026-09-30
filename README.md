# restrunt

The original site was one big HTML file. It is now split into frontend and backend files.

## Folder map

```
restrunt/
  frontend/
    index.html          page structure
    css/style.css       all site styles
    js/config.js        filters, fallback menu, reviews
    js/api.js           talks to the backend
    js/menu.js          menu filters and cards
    js/orders.js        cart and checkout
    js/app.js           theme, nav, toasts, events
  backend/
    server.js           Express server
    routes/menu.js      GET /api/menu
    routes/orders.js    GET/POST /api/orders
    data/menu.json      dishes
    data/orders.json    saved orders
```

## Run it

```bash
cd restrunt
node backend/server.js
```

Then open http://localhost:3000

## What the backend does

- `GET /api/menu` returns the full menu
- `GET /api/menu?category=Bowls` filters dishes
- `POST /api/orders` saves an order to `backend/data/orders.json`

The server uses only built-in Node modules. No npm install is required.

If the API is not running, open `frontend/index.html` directly. The page still shows a small fallback menu.
