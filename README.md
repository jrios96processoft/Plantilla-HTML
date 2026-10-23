# Portafolio personal

Sitio estático servido localmente con Node.js, sin dependencias externas.

## Requisitos

- Node.js 18 o superior

## Iniciar

```bash
npm run dev
```

También puedes usar `npm start`. Abre `http://localhost:3000` en el navegador.

## Producción con Docker y Nginx

Requiere Docker con Docker Compose. Desde la raíz del proyecto, ejecuta:

```bash
docker compose up -d --build
```

El sitio quedará disponible en `http://localhost:8080`. Para elegir otro puerto del host, define `WEB_PORT` antes de iniciar; por ejemplo, `WEB_PORT=80` en Linux/macOS o `$env:WEB_PORT=80` en PowerShell.

Para detenerlo:

```bash
docker compose down
```

Nginx sirve directamente las páginas y recursos estáticos; Node.js se conserva para el servidor local de desarrollo.