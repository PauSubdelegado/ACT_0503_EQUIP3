# Arquitectura del projecte

## Visió general

El projecte segueix una arquitectura client-servidor desacoblada:

- El **frontend** és una SPA (Single Page Application) construïda amb React.
- El **backend** és una API REST desenvolupada amb Laravel.
- La comunicació entre capes es realitza mitjançant peticions HTTP/JSON amb Axios.
- L'autenticació es gestiona amb tokens JWT.

## Estructura del frontend

src/
├── components/       # Components reutilitzables (modals, taules, formularis)
├── pages/            # Pàgines principals (Shop, Cart, Backoffice...)
├── services/         # Crides Axios a l'API
└── context/          # Context global (autenticació, carret)

## Estructura del backend (Laravel)

app/
├── Http/Controllers/ # Controladors REST
├── Models/           # Models Eloquent
├── Console/Commands/ # Comandes Artisan (csv:import)
└── Middleware/       # Autenticació JWT

## Flux d'autenticació

1. L'usuari introdueix credencials al formulari de login.
2. Formik/Yup validen les dades al frontend.
3. Axios envia la petició POST al backend.
4. Laravel valida i retorna un token JWT.
5. El token s'emmagatzema i s'adjunta a les peticions protegides.