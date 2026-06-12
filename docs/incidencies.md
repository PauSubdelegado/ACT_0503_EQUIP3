# Incidències i solucions

## Incidència 1 · Productes sense estoc a l'API
**Descripció**: Els productes retornats per l'API no disposaven d'estoc
disponible, fet que provocava que el botó 'Afegir al carret' apareguera
desactivat automàticament a la botiga.

**Impacte**: No era possible afegir productes al carret ni verificar
el funcionament correcte del flux de compra.

**Solució aplicada**: Es va modificar localment el fitxer `shop.jsx`,
afegint valors d'estoc manualment mitjançant el localStorage.

**Estat**: Solució temporal. La solució definitiva requereix que
l'API retorne el camp d'estoc correctament.

## Incidència 2 · Coincidència amb les pràctiques externes
**Descripció**: L'inici de les pràctiques externes va coincidir amb
el desenvolupament del Sprint 5, reduint considerablement la
disponibilitat horària de l'equip.

**Impacte**: Les hores reals dedicades no van coincidir amb les
67 hores estimades inicialment.

**Solució aplicada**: Es va replantejar el pla de treball, prioritzant
les tasques més crítiques del projecte.

## Incidència 3 · Vaga de professors
**Descripció**: La vaga de professorat durant el Sprint 5 va afectar
les sessions de classe planificades.

**Impacte**: Es van reduir les oportunitats de col·laboració i
seguiment del projecte amb el professorat.

**Solució aplicada**: L'equip va mantenir la coordinació de manera
autònoma i va adaptar el calendari de tasques.

## Resum d'hores (Clockify)
| Assignatura | Hores estimades | Adrià | Pau | Rubén |
|-------------|----------------|-------|-----|-------|
| DWEC | 12 | 30 | 5 | 34 |
| PI | 5 | 13 | 24 | 43 |
| DAW | 19 | 11 | 2 | 9 |
| DIW | 22 | 20 | 18 | 41 |
| Altres | 9 | 21 | 0 | 16 |
| **Total** | **67** | **94** | **45** | **143** |