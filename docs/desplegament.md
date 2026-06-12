# Desplegament del projecte

## Importació automàtica de dades via CSV/FTP

El backend disposa d'una comanda Laravel que automatitza la descàrrega i importació de fitxers CSV des d'un servidor FTP extern.

### Execució de la comanda

```bash
php artisan csv:import
```

### Flux de la importació

1. S'estableix connexió amb el servidor FTP usant les credencials del `.env`.
2. Es descarreguen els fitxers `familia.csv` i `producto.csv`.
3. **Importació de famílies** (dues passades):
   - Primera passada: es creen o actualitzen les famílies sense `parent_id`.
   - Segona passada: es resolen les relacions pare-fill.
4. **Importació de productes**: cada producte s'associa a la seua subfamília (o família principal com a fallback).
5. El sistema de logging mostra registres creats, actualitzats i saltats.

### Exemple de sortida

```text
Iniciant importació - 06:06:51
Connectant al servidor FTP comparador.daw.iesevalorpego.es...
✓ familia.csv descarregat
✓ producto.csv descarregat
✓ familia.csv importat (0 nous, 11 existents)
✓ producto.csv importat (0 nous, 50 actualitzats, 0 saltats)
Importació completada.
```

## Desplegament del frontend

```bash
# Generar el build de producció
npm run build

# Els fitxers estàtics es generen a la carpeta dist/

# Pujar-los al servidor web (Apache/Nginx)
```

## Desplegament del backend

```bash
# En el servidor de producció

composer install --no-dev --optimize-autoloader

php artisan config:cache

php artisan route:cache

php artisan migrate --force
```