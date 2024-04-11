---
id: typescript-type-guards-differentiating-types
title: Type Guards e Differentiating Types in TypeScript
sidebar_label: Type Guards e Differentiating Types
---

# Type Guards e Differentiating Types in TypeScript

## Capitolo 1: Introduzione ai Type Guards

In TypeScript, un Type Guard è un'espressione che esegue un controllo che garantisce il tipo in un determinato ambito. Ciò consente di restringere il tipo di un oggetto all'interno di un determinato blocco di codice.

## Capitolo 2: Sintassi dei Type Guards

Ecco un esempio di come creare un Type Guard:

```typescript
function isString(test: any): test is string {
  return typeof test === "string";
}
```

In questo esempio, `isString` è un Type Guard che verifica se `test` è una stringa.

## Capitolo 3: Differentiating Types

Differentiating Types è il processo di distinzione tra tipi in TypeScript. Questo è spesso necessario quando si lavora con Union Types.

Ecco un esempio di come differenziare i tipi:

```typescript
type StringOrNumber = string | number;

function process(value: StringOrNumber) {
  if (typeof value === "string") {
    // In questo blocco, value è di tipo string
    return value.toUpperCase();
  } else {
    // In questo blocco, value è di tipo number
    return value.toFixed(2);
  }
}
```

In questo esempio, la funzione `process` differenzia tra `string` e `number` utilizzando un Type Guard.
