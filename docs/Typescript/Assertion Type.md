---
id: typescript-assertion
title: Assertion Type in TypeScript
sidebar_label: Assertion Type
---

# Assertion Type in TypeScript

## Capitolo 1: Introduzione all'Assertion Type

In TypeScript, l'assertion type è un modo per dire al compilatore "fidati di me, so quello che sto facendo". È come un cast di tipo in altri linguaggi di programmazione, ma non esegue alcun controllo speciale o riorganizzazione dei dati. Non ha alcun impatto a runtime e viene utilizzato puramente dal compilatore.

## Capitolo 2: Sintassi dell'Assertion Type

Ci sono due modi per fare un'assertion di tipo in TypeScript:

1. Angle-bracket syntax:

```typescript
let qualcheValore: any = "questo è un string";
let lunghezzaStringa: number = (<string>qualcheValore).length;
```

2. as-syntax:

```typescript
let qualcheValore: any = "questo è un string";
let lunghezzaStringa: number = (qualcheValore as string).length;
```

In entrambi gli esempi, stiamo dicendo al compilatore di fidarsi del fatto che `qualcheValore` è una stringa e quindi ha una proprietà `length`.

## Capitolo 3: Quando usare l'Assertion Type

L'assertion type può essere utile quando si conosce una informazione più specifica su un valore rispetto a quanto il tipo attuale esprima. Tuttavia, dovrebbe essere usato con cautela, poiché forzare un'assertion di tipo può portare a errori se il valore non è del tipo asserito.
