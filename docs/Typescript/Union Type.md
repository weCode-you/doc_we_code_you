---
id: typescript-union-types
title: Union Types in TypeScript
sidebar_label: Union Types
---

# Union Types in TypeScript

## Capitolo 1: Introduzione ai Union Types

In TypeScript, un Union Type è un tipo di dato che può essere uno tra diversi tipi. È un modo per gestire situazioni in cui una variabile potrebbe avere più di un tipo.

## Capitolo 2: Sintassi dei Union Types

Ecco un esempio di come creare un Union Type:

```typescript
let valore: number | string;
```

In questo esempio, `valore` è un Union Type che può essere sia un numero che una stringa.

## Capitolo 3: Quando usare i Union Types

I Union Types sono utili quando si desidera che una variabile possa avere più di un tipo. Ad esempio, se si ha una funzione che accetta sia stringhe che numeri come argomenti, si può utilizzare un Union Type per indicare questo.

Ecco un esempio:

```typescript
function stampaValore(valore: number | string) {
  console.log(valore);
}
```

In questo esempio, la funzione `stampaValore` accetta un argomento `valore` che può essere sia un numero che una stringa.