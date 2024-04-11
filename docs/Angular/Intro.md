---
id: introduzione-angular
title: Introduzione ad Angular
sidebar_label: Introduzione ad Angular
---

# Introduzione ad Angular

## Capitolo 1: Installazione di Node.js e npm

Prima di tutto, è necessario installare Node.js e npm (Node Package Manager) sul tuo computer. Puoi scaricarli dal sito ufficiale di Node.js.

```bash
# Verifica l'installazione
node -v
npm -v
```

## Capitolo 2: Installazione di Angular CLI

Angular CLI (Command Line Interface) è uno strumento che ci permette di creare e gestire progetti Angular. Puoi installarlo globalmente sul tuo computer utilizzando npm.

```bash
npm install -g @angular/cli
```

## Capitolo 3: Creazione di un nuovo progetto Angular

Dopo aver installato Angular CLI, puoi creare un nuovo progetto Angular utilizzando il comando `ng new`.

```bash
ng new mio-progetto
```

## Capitolo 4: Esecuzione del progetto Angular

Per eseguire il tuo progetto Angular, naviga nella cartella del progetto e usa il comando `ng serve`.

```bash
cd mio-progetto
ng serve
```

Ora, il tuo progetto Angular dovrebbe essere in esecuzione su `http://localhost:4200/`.

## Capitolo 5: Struttura del progetto Angular

Un progetto Angular ha una struttura di cartelle specifica. Le parti più importanti sono:

- `src/app`: Qui è dove risiede la maggior parte del codice dell'applicazione.
- `src/index.html`: Questo è il file principale HTML che viene visualizzato quando qualcuno visita il tuo sito.
- `angular.json`: Questo file contiene varie configurazioni per il progetto Angular.

## Capitolo 6: Creazione di un componente Angular

In Angular, un componente è una parte di codice che controlla una parte dell'interfaccia utente. Puoi creare un nuovo componente utilizzando il comando `ng generate component`.

```bash
ng generate component mio-componente
```

Questo comando creerà una nuova cartella `mio-componente` in `src/app` con quattro file: `mio-componente.component.css`, `mio-componente.component.html`, `mio-componente.component.spec.ts`, e `mio-componente.component.ts`.

Ricorda, questa è solo una documentazione di base. Angular è un framework molto potente con molte altre funzionalità. Ti consigliamo di leggere la documentazione ufficiale di Angular per saperne di più.