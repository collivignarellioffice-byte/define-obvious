# Definisci l’ovvio

An Italian word-definition game built to explore a simple question: **how well can we explain the words we use every day?**

[Play the live demo](https://collivignarellioffice-byte.github.io/define-obvious/)

## The problem

Familiar words often feel obvious until we have to define them precisely. *Definisci l’ovvio* turns that gap into a short learning and party experience: players describe a word in their own language, compare the answer with its essential concepts and learn what makes a definition clear.

## The experience

The prototype offers two modes:

- **Training:** write a definition, receive a score from 0 to 100 and see which essential concepts were included or missed.
- **Turn-based game:** 2–8 players pass the device, reveal one word at a time, judge each definition and finish with a leaderboard.

The 18 cards are divided into three levels—**Concrete**, **Everyday** and **Abstract**—so the task becomes progressively less dependent on visible characteristics.

## How evaluation works

Training mode uses a transparent, deterministic scoring system. Each card contains:

- essential concepts and accepted related terms;
- a reference definition;
- a link to the corresponding Treccani entry.

The score combines concept coverage, answer structure, precision signals and concision. This makes feedback immediate and keeps the prototype fully client-side. It is a heuristic evaluation rather than a semantic or LLM-based assessment, so valid synonyms outside the current vocabulary may not be recognised.

## Product and design choices

- **One action at a time:** the interface keeps the word, input and feedback in a clear sequence.
- **Explainable feedback:** players see the concepts they covered and those they missed, instead of receiving only a number.
- **Shared-device play:** multiplayer works without accounts, rooms or setup beyond entering player names.
- **Responsive and accessible UI:** semantic controls, visible focus states, ARIA attributes and layouts for desktop and mobile.
- **No backend:** the game loads instantly and does not collect or transmit player answers.

## Stack

- HTML5
- CSS3
- Vanilla JavaScript
- GitHub Pages

The complete prototype lives in [`index.html`](./index.html); it has no framework, package manager or runtime dependency.

## Run locally

Clone the repository and open `index.html` in a browser:

```bash
git clone https://github.com/collivignarellioffice-byte/define-obvious.git
cd define-obvious
open index.html
```

You can also serve the folder with any static web server.

## Current limits and next steps

- Expand the card set and accepted vocabulary.
- Test comprehension and scoring with real users.
- Add semantic evaluation while keeping the feedback explainable.
- Separate content from presentation to make editorial updates easier.
- Add automated checks for scoring rules and keyboard flows.

## Sources

Reference definitions and essential concepts are derived and rewritten from entries in the [Treccani Italian Vocabulary](https://www.treccani.it/vocabolario/). Each result links to its specific source entry.

## Author

Designed and built by [Martina Colli Vignarelli](https://martinacollivignarelli.com/).
