---
id: typescript-intersection-types
title: Intersection Types in TypeScript
sidebar_label: Intersection Types
---

# Intersection Types in TypeScript

## Capitolo 1: Introduzione agli Intersection Types

In TypeScript, un Intersection Type è un tipo di dato che può combinare più tipi in uno. È un modo per aggiungere insieme esistenti tipi di dati.

## Capitolo 2: Sintassi degli Intersection Types

Ecco un esempio di come creare un Intersection Type:

```typescript
type Nome = { nome: string };
type Eta = { eta: number };
type Persona = Nome & Eta;
```

In questo esempio, `Persona` è un Intersection Type che combina i tipi `Nome` ed `Eta`.

## Capitolo 3: Quando usare gli Intersection Types

Gli Intersection Types sono utili quando si desidera che un oggetto possa avere le proprietà di più di un tipo. Ad esempio, se si ha un oggetto che deve avere le proprietà di due interfacce diverse, si può utilizzare un Intersection Type per indicare questo.

Ecco un esempio:

```typescript
interface Nome {
  nome: string;
}

interface Eta {
  eta: number;
}

type Persona = Nome & Eta;

let p: Persona = { nome: "Mario", eta: 30 };
```

In questo esempio, l'oggetto `p` è di tipo `Persona`, che è un Intersection Type che combina le interfacce `Nome` ed `Eta`.
