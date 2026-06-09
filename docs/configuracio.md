# Configuració del projecte

## Variables d'entorn (backend)

El fitxer `.env` del backend ha de contenir les variables següents:

```env
APP_NAME=ApiSelectio
APP_ENV=local
APP_KEY=base64:...
APP_DEBUG=true
APP_URL=http://localhost

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=selectio
DB_USERNAME=root
DB_PASSWORD=

# Credencials FTP per a la importació de CSV
FTP_HOST=comparador.daw.iesevalorpego.es
FTP_USERNAME=...
FTP_PASSWORD=...

# JWT
JWT_SECRET=...
JWT_TTL=60
```

## Bootstrap al frontend

Bootstrap 5 s'ha integrat com a framework principal de maquetació.

S'utilitza per a:

* Sistema de grid (`container`, `row`, `col`) per a layouts responsius.
* Components d'interfície: taules, formularis, botons, modals i alertes.
* Classes d'utilitat per a flexbox, espaiat, ombres i vores arrodonides.

## Autenticació JWT

1. El login envia les credencials al endpoint `POST /api/auth/login`.
2. El backend retorna un token JWT.
3. El token s'emmagatzema al `localStorage` del navegador.
4. Totes les peticions protegides inclouen la capçalera:

```text
Authorization: Bearer {token}
```
