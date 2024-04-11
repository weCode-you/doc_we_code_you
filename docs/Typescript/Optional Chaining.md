---
id: optional-chaining
title: Optional Chaining in TypeScript
sidebar_label: Optional Chaining
---

# Optional Chaining in TypeScript

## Capitolo 1: Introduzione all'Optional Chaining

In TypeScript, l'Optional Chaining (`?.`) è un operatore che permette di accedere in modo sicuro a proprietà annidate all'interno di oggetti. Questo può essere particolarmente utile quando si lavora con oggetti che potrebbero avere strutture complesse o non completamente definite.

## Capitolo 2: Utilizzo dell'Optional Chaining

Supponiamo di avere un oggetto `utente` con una struttura annidata:

```typescript
let utente = {
  nome: "Mario",
  indirizzo: {
    via: "Via Roma",
    citta: "Roma",
  },
};
```

Senza l'Optional Chaining, se volessimo accedere alla proprietà `citta` dell'`indirizzo`, dovremmo prima verificare che l'`indirizzo` esista:

```typescript
let citta = utente && utente.indirizzo && utente.indirizzo.citta;
```

Con l'Optional Chaining, possiamo accedere alla `citta` in modo più semplice e sicuro:

```typescript
let citta = utente?.indirizzo?.citta;
```

Se `utente` o `indirizzo` sono `undefined` o `null`, l'espressione restituirà `undefined` invece di generare un errore.

## Capitolo 3: Optional Chaining con Funzioni e Array

L'Optional Chaining può essere utilizzato anche con funzioni e array. Se stiamo cercando di chiamare una funzione che potrebbe non esistere, possiamo usare `?.()`:

```typescript
let risultato = oggetto.miaFunzione?.();
```

Se stiamo cercando di accedere a un elemento di un array che potrebbe non esistere, possiamo usare `?.[]`:

```typescript
let elemento = mioArray?.[indice];
```

In entrambi i casi, se la funzione o l'array sono `undefined` o `null`, l'espressione restituirà `undefined`.

Ricorda, l'Optional Chaining è una caratteristica molto potente di TypeScript che può rendere il tuo codice più sicuro e leggibile. Tuttavia, dovrebbe essere usato con attenzione per evitare comportamenti inaspettati.