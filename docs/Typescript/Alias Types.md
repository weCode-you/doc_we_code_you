---
id: typescript-alias-types
title: Alias Types in TypeScript
sidebar_label: Alias Types
---

# Alias Types in TypeScript

## Capitolo 1: Introduzione agli Alias Types

In TypeScript, un alias di tipo è un nome alternativo per un tipo. Gli alias di tipo sono creati con la parola chiave `type`.

## Capitolo 2: Sintassi degli Alias Types

Ecco un esempio di come creare un alias di tipo:

```typescript
type StringOrNumber = string | number;
```

In questo esempio, `StringOrNumber` è un alias di tipo che rappresenta un dato che può essere sia una stringa che un numero.

## Capitolo 3: Quando usare gli Alias Types

Gli alias di tipo sono utili quando si desidera utilizzare un tipo complesso più volte. Ad esempio, se si ha un tipo di unione complesso o un tipo di intersezione che si utilizza in più luoghi nel codice, può essere utile definire un alias di tipo per semplificare.

Ecco un esempio:

```typescript
type ComplexType = { nome: string, eta: number } | null;
```

In questo esempio, `ComplexType` è un alias di tipo che rappresenta un oggetto con le proprietà `nome` e `eta`, o `null`.

