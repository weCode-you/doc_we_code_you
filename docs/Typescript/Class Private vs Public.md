---
id: classi-typescript
title: Classi e Private vs Public in TypeScript
sidebar_label: Classi e Private vs Public
---

# Classi e Private vs Public in TypeScript

## Capitolo 1: Introduzione alle Classi

In TypeScript, una classe è un modello per la creazione di oggetti. Una classe può includere campi (proprietà) e metodi. Ecco un esempio di una classe semplice:

```typescript
class Persona {
  nome: string;
  eta: number;

  constructor(nome: string, eta: number) {
    this.nome = nome;
    this.eta = eta;
  }

  saluta() {
    console.log(`Ciao, il mio nome è ${this.nome} e ho ${this.eta} anni.`);
  }
}
```

## Capitolo 2: Private vs Public

In TypeScript, ogni membro di una classe è pubblico di default. Ciò significa che può essere accessibile da qualsiasi parte del codice. Tuttavia, possiamo rendere un membro privato utilizzando la parola chiave `private`. Un membro privato può essere accessibile solo all'interno della classe stessa.

```typescript
class Persona {
  private nome: string;
  private eta: number;

  constructor(nome: string, eta: number) {
    this.nome = nome;
    this.eta = eta;
  }

  saluta() {
    console.log(`Ciao, il mio nome è ${this.nome} e ho ${this.eta} anni.`);
  }
}
```

In questo esempio, `nome` e `eta` sono privati, quindi non possono essere accessibili al di fuori della classe `Persona`.

## Capitolo 3: Getter e Setter

Se abbiamo membri privati in una classe e vogliamo comunque permettere l'accesso a questi membri in qualche modo, possiamo utilizzare i getter e i setter.

```typescript
class Persona {
  private _nome: string;
  private _eta: number;

  constructor(nome: string, eta: number) {
    this._nome = nome;
    this._eta = eta;
  }

  get nome() {
    return this._nome;
  }

  set nome(nuovoNome: string) {
    this._nome = nuovoNome;
  }

  saluta() {
    console.log(`Ciao, il mio nome è ${this._nome} e ho ${this._eta} anni.`);
  }
}
```

In questo esempio, abbiamo un getter e un setter per `nome`. Questo ci permette di leggere e modificare il valore di `nome` al di fuori della classe, pur mantenendo il controllo sull'accesso attraverso i metodi getter e setter.

Ricorda, le classi e i modificatori di accesso come private e public sono strumenti potenti in TypeScript che ti aiutano a scrivere codice più sicuro e strutturato. Tuttavia, dovrebbero essere usati con attenzione per evitare comportamenti inaspettati.