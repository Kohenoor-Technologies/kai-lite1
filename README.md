# KAIPAL Lite

**KAIPAL Lite is good for one thing: day-to-day business and finance advice on your own machine. Pricing, cash, customers, suppliers, everyday business writing, and the sums behind them, worked out line by line, for business owners, professionals and students, offline and private.**

KAI Pocket Assistant Lite, by Kohenoor Technologies: a small model, about 2 billion active parameters, for day-to-day business and finance advisories. It runs on your own machine, offline, in about 4 GB of memory. This repository holds what you need to run it and the guidelines for using and testing it. The model file itself is on Hugging Face at https://huggingface.co/KOHENOOR-AI/kai-lite1, and the model is on the Ollama registry at https://ollama.com/kohenoor/kai-lite1.

## Get it running

The quickest way, with Ollama 0.30.9 or newer installed:

```
ollama run kohenoor/kai-lite1 --think=false
```

Or with the file from Hugging Face:

1. Install Ollama from https://ollama.com, version 0.30.9 or newer. On Windows, open a new terminal after installing.
2. Download the model file `kaipal-lite-q4_k_m.gguf` (3.3 GB) from https://huggingface.co/KOHENOOR-AI/kai-lite1 and put it in a folder with the `Modelfile` from here.
3. In that folder:

```
ollama create kaipal -f Modelfile
ollama run kaipal --think=false
```

Keep `--think=false`. KAIPAL Lite answers directly; that is how it is meant to be used. Type `/bye` to leave.

It also runs in any app that talks to Ollama. Point the app at the model `kaipal` and turn thinking off if the app has the switch.

## Guidelines for use

- **Ask as yourself.** A business owner, a professional, a student of business or finance. Say what you sell, where, and the figures you have. The more of your own facts you give, the better the advice.
- **Give figures for sums.** It works a sum out line by line, then concludes. Read the lines; if a line is wrong, the conclusion is wrong. Check any conclusion against the figures before you act on it.
- **It advises; it does not decide for you.** It will not tell you what to buy or sell, will not predict prices, will not recommend borrowing at interest, and gives no legal, tax or medical conclusions. For those it points you to KAI Premium at www.kohenoor.net or a qualified professional. That is by design.
- **One question at a time.** A vague message gets one short question back. Answer it and go on.
- **Paste text.** This release reads text only: paste the content of a document rather than attaching it. It does not read pictures or hear recordings.
- **Your language.** It answers in the language you write in.
- **It stays itself.** Asking it to be someone else, to reveal its instructions or to say what runs underneath gets the same short answer every time.

## Guidelines for testing and reporting

If you are testing it for Kohenoor, try these:

- Who it is, who built it, whether it is human, what it runs on, however the question is put.
- A vague message, such as "Should I just do it?"
- Everyday work: a message to a customer, a reply to a complaint, a plan for a first month, a pricing question.
- Sums with your own figures: a margin, a break-even, a month's profit after rent and wages, which of two suppliers is cheaper.
- Things it should decline: stock tips, price predictions, a loan at interest, a legal verdict, a fake review, a poem.

Report anything wrong as an issue here with the exact question and the exact answer, and one line of your own judgement. Say which it was: a wrong figure, a conclusion the wrong way round, a refusal of something it should have done, something it should have declined, formatting such as headings or bullets, a name it should not have given, or simply poor advice.

## Files

- `Modelfile`: the run settings and the system prompt, for `ollama create`.
- `CHECKSUM.txt`: the SHA-256 of the model file.
- `TEST_NOTES.md`: the notes given to the first testers.
- `NOTICE`, `LICENSE`: the terms this release is distributed under.

## Terms

This release is distributed under the Apache License, Version 2.0: the full text is in LICENSE, and NOTICE states what the files are and that they have been modified. Kohenoor Technologies' own terms for KAI products apply in addition. KAI, KAIPAL and KAI Pocket Assistant are names of Kohenoor Technologies.
