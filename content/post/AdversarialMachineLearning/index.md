---
title: Adversarial Machine Learning
date: '2024-01-02'
summary: Un breve articolo informativo su cosa è AML e una panoramica sugli attacchi principali alle reti neurali.
---

Verso la fine dei miei studi universitari in cybersecurity mi sono approcciato verso il mondo dell'intelligenza artificiale, un campo che per scelta avevo cercato di evitare. Il mio professore mi ha suggerito un argomento di tesi e, nonostante si aspettasse un risultato diverso, ho realizzato che anche il mondo dell'IA è soggetto a possibili attacchi. Effettivamente può sembrare una realizzazione banale ma non è così,  soprattutto capendo come alcuni di questi attacchi funzionano. Quindi, volevo scrivere questo breve articolo per raccontare e spiegare in maniera semplice questi attacchi.

Il primo di questi attacchi in letteratura è conosciuto come Adversarial Example. Il meccanismo di base è quello  di forgiare un esempio di input che viene leggermente manipolato in maniera tale che il modello restituisca un output completamente errato. La manipolazione viene fatta aggiungendo rumore nell'input.
Questo attacco risulta incredibilmente difficile da mitigare.

Nel momento in cui un attaccante riuscisse a ottenere accesso ai dati di training di un modello (banalmente acquistando URL scaduti e rindirizzando sul proprio training set modificato((carlini))) è possibile effettuare attacchi di data poisoning. Il concetto è semplice, se controlli il data set sui cui effettui il training, puoi manipolare il comportamento del modello. In particolare, degradare le performance avendo modificato solo una piccola percentuale del modello (0.1% basta).

 

Un particolare esempio di data poisoning è definito attacco di backdoor. In questo caso, è sufficiente che un trigger faccia scattare il modello, in modo tale che questo faccia comportare male solo nei casi questo trigger si attivi
