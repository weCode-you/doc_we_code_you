---
id: typescript-type-identification
title: Identificazione del Tipo in TypeScript
sidebar_label: Identificazione del Tipo
---

# Identificazione del Tipo in TypeScript

## Capitolo 1: Type Predicate

Un Type Predicate è una funzione che agisce come un guardiano del tipo. Questo tipo di funzione ritorna un booleano che indica se l'argomento corrisponde a un certo tipo.

Ecco un esempio di Type Predicate:

```typescript
function isNumber(x: any): x is number {
  return typeof x === "number";
}
```

## Capitolo 2: "typeof"

"typeof" è un operatore che ritorna una stringa che indica il tipo di un'operando.

Ecco un esempio di "typeof":

```typescript
let x = "hello";
console.log(typeof x); // Outputs: "string"
```

## Capitolo 3: "in" operator

L'operatore "in" ritorna true se la proprietà specificata è nell'oggetto specificato o nella sua catena di prototipi.

Ecco un esempio di "in" operator:

```typescript
let x = { prop: 0 };
console.log("prop" in x); // Outputs: true
```

## Capitolo 4: "instanceof" operator

L'operatore "instanceof" è un modo per verificare il tipo di un oggetto al momento dell'esecuzione. Viene utilizzato per confermare se un oggetto è un'istanza di una particolare classe.

Ecco un esempio di "instanceof":

```typescript
class MyClass {
  // ...
}

let x = new MyClass();
console.log(x instanceof MyClass); // Outputs: true
```

## Capitolo 56: User-Defined Type Guards

Un User-Defined Type Guard è una funzione che implementa un controllo di tipo personalizzato. Questo tipo di funzione può essere utilizzato per verificare che un oggetto soddisfi un determinato contratto di tipo.

Ecco un esempio di User-Defined Type Guard:

```typescript
function isFish(pet: Fish | Bird): pet is Fish {
    return (pet as Fish).swim !== undefined;
}
```

## Capitolo 6: Type Assertions

Le Type Assertions sono un modo per dire al compilatore "fidati di me, so quello che sto facendo". Una Type Assertion è come un cast di tipo in altri linguaggi, ma non esegue alcun controllo speciale o ristrutturazione dei dati.

Ecco un esempio di Type Assertion:

```typescript
let someValue: any = "this is a string";
let strLength: number = (someValue as string).length;
```
