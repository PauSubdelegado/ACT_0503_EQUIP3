# Instal·lació del projecte

## Requisits previs

* Node.js >= 18
* PHP >= 8.1
* Composer
* MySQL
* Git

## Frontend (React)

```bash
# Clonar el repositori del frontend
git clone https://github.com/equip3/selectio-frontend

cd selectio-frontend

# Instal·lar dependències
npm install

# Iniciar el servidor de desenvolupament
npm run dev
```

## Backend (Laravel)

```bash
# Clonar el repositori del backend
git clone https://github.com/equip3/apiSelectio

cd apiSelectio

# Instal·lar dependències PHP
composer install

# Copiar el fitxer d'entorn
cp .env.example .env

# Generar la clau de l'aplicació
php artisan key:generate

# Executar les migracions
php artisan migrate

# Iniciar el servidor
php artisan serve
```

## Dependències principals

| Paquet            | Versió | Ús                      |
| ----------------- | ------ | ----------------------- |
| react             | ^18    | Framework frontend      |
| bootstrap         | ^5     | Estils i components UI  |
| axios             | ^1     | Peticions HTTP          |
| formik            | ^2     | Gestió de formularis    |
| yup               | ^1     | Validació de formularis |
| laravel/framework | ^10    | Framework backend       |
| tymon/jwt-auth    | ^2     | Autenticació JWT        |
