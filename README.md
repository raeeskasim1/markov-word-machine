# Markov Word Machine

Train a tiny next-word sampler on a paragraph and watch its word transitions invent new combinations.

## Run

Open `index.html` in a modern browser. HTML, CSS, and JavaScript are all in that file. No server, packages, internet connection, API key, build step, or downloaded model is required.

## Try it

Generate multiple outputs, change the training paragraph, and inspect successor probabilities for a frequent starting word.

## How it works

Lowercase word tokens train a first-order Markov chain. Repeated successor words appear repeatedly in the transition list, so uniform sampling of that list matches observed transition frequencies. Generation stops at a word with no outgoing transition. Punctuation and sentence boundaries are ignored; this is a deliberately simple statistical text toy.

