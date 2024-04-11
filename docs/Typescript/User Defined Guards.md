---
id: typescript-user-defined-guards
title: User-Defined Type Guards in TypeScript
sidebar_label: User-Defined Type Guards
---

# User-Defined Type Guards in TypeScript

## Capitolo 1: Introduzione ai User-Defined Type Guards

In TypeScript, un User-Defined Type Guard è una funzione che implementa un controllo di tipo personalizzato. Questo tipo di funzione può essere utilizzato per verificare che un oggetto soddisfi un determinato contratto di tipo.

## Capitolo 2: Sintassi dei User-Defined Type Guards

Ecco un esempio di come creare un User-Defined Type Guard:

```typescript
function isFish(pet: Fish | Bird): pet is Fish {
    return (pet as Fish).swim !== undefined;
}
```

In questo esempio, `isFish` è un User-Defined Type Guard che verifica se `pet` è di tipo `Fish`.

## Capitolo 3: Quando usare i User-Defined Type Guards

I User-Defined Type Guards sono utili quando si desidera implementare logiche di controllo del tipo più complesse di quelle che possono essere eseguite con i normali Type Guards di TypeScript.

Ecco un esempio:

```typescript
interface Bird {
  fly(): void;
  layEggs(): void;
}

interface Fish {
  swim(): void;
  layEggs(): void;
}

function getSmallPet(): Fish | Bird {
  // ...
}

let pet = getSmallPet();

if (isFish(pet)) {
  pet.swim();
} else {
  pet.fly();
}
```

In questo esempio, la funzione `isFish` è un User-Defined Type Guard che viene utilizzato per determinare se `pet` è un `Fish` o un `Bird`.
