---
id: typescript-generics
title: Generics in TypeScript
sidebar_label: Generics
---

# Generics in TypeScript

## Capitolo 1: Introduzione ai Generics

In TypeScript, i Generics sono un modo per creare componenti riutilizzabili che possono lavorare su una varietà di tipi, piuttosto che su un singolo tipo.

## Capitolo 2: Sintassi dei Generics

Ecco un esempio di come creare una funzione generica:

```typescript
function identity<T>(arg: T): T {
  return arg;
}
```

In questo esempio, `T` è una variabile di tipo. Ciò consente di utilizzare qualsiasi tipo, non solo un tipo specifico.

## Capitolo 3: Utilizzo dei Generics

I Generics possono essere utilizzati in molte situazioni diverse, tra cui classi, interfacce e funzioni.

Ecco un esempio di come utilizzare un Generic in una classe:

```typescript
class GenericNumber<T> {
  zeroValue: T;
  add: (x: T, y: T) => T;
}
```

In questo esempio, `GenericNumber` è una classe che utilizza una variabile di tipo `T`.

## Capitolo 4: Limiti dei Generics

In alcuni casi, potrebbe essere necessario limitare i tipi che possono essere utilizzati con un Generic. Questo può essere fatto utilizzando un'interfaccia e l'estensione di tipo.

Ecco un esempio di come limitare un Generic:

```typescript
interface Lengthwise {
  length: number;
}

function loggingIdentity<T extends Lengthwise>(arg: T): T {
  console.log(arg.length);
  return arg;
}
```

In questo esempio, il Generic `T` è limitato a tipi che implementano l'interfaccia `Lengthwise`.
