---
id: typescript-types
title: Types: Interface vs Class vs Type in TypeScript
sidebar_label: Interface vs Class vs Type
---

# Types: Interface vs Class vs Type in TypeScript

## Capitolo 1: Introduzione a Interface, Class e Type

In TypeScript, `interface`, `class` e `type` sono tre modi principali per definire tipi di dati. Ognuno ha i suoi usi e vantaggi.

## Capitolo 2: Interface

Le interfacce sono un modo potente per definire contratti all'interno del tuo codice. Sono utilizzate per definire la forma di un oggetto.

```typescript
interface Persona {
  nome: string;
  eta: number;
}
```

In questo esempio, `Persona` è un'interfaccia che richiede che un oggetto abbia le proprietà `nome` e `eta`.

## Capitolo 3: Class

Le classi sono un modello per la creazione di oggetti e l'implementazione di funzionalità. Una classe può implementare un'interfaccia per garantire che aderisca a un determinato contratto.

```typescript
class Studente implements Persona {
  nome: string;
  eta: number;

  constructor(nome: string, eta: number) {
    this.nome = nome;
    this.eta = eta;
  }
}
```

In questo esempio, `Studente` è una classe che implementa l'interfaccia `Persona`.

## Capitolo 4: Type

`Type` è un alias che può essere utilizzato per dare un nome a un tipo di dato. Può rappresentare un tipo primitivo, unione di tipi, intersezione di tipi, tuple, e altro ancora.

```typescript
type StringOrNumber = string | number;
```

In questo esempio, `StringOrNumber` è un alias di tipo che rappresenta un dato che può essere sia una stringa che un numero.
