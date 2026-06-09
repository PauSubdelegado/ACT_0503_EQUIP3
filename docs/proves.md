# Proves del projecte

## Carret de compra (Selectio)

### Funcionalitats provades

| Funcionalitat | Resultat |
|---------------|----------|
| Afegir producte al carret | ✅ Correcte |
| Modificar quantitat | ✅ Correcte |
| Eliminar producte del carret | ✅ Correcte |
| Aplicar codi promocional | ✅ Correcte |
| Validació de dades d'enviament (Yup) | ✅ Correcte |
| Confirmació de comanda | ✅ Correcte |

### Problema detectat durant les proves

Els productes retornats per l'API no disposaven d'estoc disponible, fet que desactivava el botó "Afegir al carret".

**Solució temporal**: es van afegir valors d'estoc manualment via localStorage al fitxer `shop.jsx` per poder realitzar les proves.

## Backoffice NextApp

### Gestió d'usuaris

| Acció | Resultat |
|-------|----------|
| Llistar usuaris | ✅ Correcte |
| Crear usuari nou | ✅ Correcte |
| Editar usuari | ✅ Correcte |
| Eliminar usuari | ✅ Correcte |
| Filtrar per rol | ✅ Correcte |

## Autenticació JWT

| Escenari | Resultat |
|----------|----------|
| Login amb credencials correctes | ✅ Token rebut |
| Login amb credencials incorrectes | ✅ Error mostrat |
| Accés a ruta protegida amb token | ✅ Correcte |
| Accés a ruta protegida sense token | ✅ Redirigit al login |