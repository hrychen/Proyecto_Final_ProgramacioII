# Proyecto Final Programacio II - Gestió de Regals

## Descripció

Sistema de gestió de regals que permet afegir, eliminar, entregar, ordenar i consultar regals utilitzant una llista enllaçada.

---

## Motiu d'Elecció

// He escollit una **Linked List** perquè permet afegir i eliminar regals de forma eficient sense haver de moure altres elements. A més, la mida de la llista creix dinàmicament segons les necessitats, sense haver de reservar memòria extra.

---

## Struct Regal

```cpp
struct Regal {
    string nom;           // Nom del regal
    char tipus[20];       // Tipus (Joguina, Electrònica...)
    string tamany;        // Petit, Mitjà, Gran
    string destinacio;    // Destinatari
    bool entregat;        // true = entregat, false = pendent
};
```

---

## Classe LlistaRegals

La classe gestiona una llista enllaçada de regals amb tres comptadors: nombre total de regals, nombre d'entregats i nombre de pendents.

### Mètodes

| Mètode | Descripció |
|--------|------------|
| `afegeixRegal(nom, tipus, tamany, destinacio)` | Afegeix un nou regal a la llista |
| `eliminarRegal(nomRegal)` | Elimina un regal pel seu nom |
| `entregarRegal(nomRegal, destinacio)` | Canvia l'estat a `entregat = true` |
| `imprimirLlista()` | Mostra tots els regals amb els comptadors |
| `imprimirTipus(tipus)` | Mostra només els regals d'un tipus concret |
| `ordenar(tipusOrdenacio)` | Ordena la llista (1=alfabètic, 2=per tipus) |
| `obrirRegal(nomRegal)` | Mostra tota la informació d'un regal |
| `modificarRegal(nomRegal)` | Permet modificar els valors del struct |
| `afegirTipus("String")` | Afegeix un nou tipus disponible |

---
