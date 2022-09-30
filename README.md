# Harry Potter Sentiment-Analyse

In dieser Arbeit werden die Originaltexte von Harry Potter sowie verschiedener
Fan-Fiction-Texte behandelt.

Mittels einer Netzwerkanalyse werden die Beziehungen zwischen den handelnden 
Personen untersucht.
Dabei wird die Python-Bibliothek SpaCy verwendet, um die *Named Entity
Recognition* durchzuführen.

Anschließend werden die gefundenen Namen mit Variationen davon gematcht.
Beispielsweise werden "Harry" und "Harry Potter" nicht als eine Entity erkannt.

Darauffolgend sollen die Interaktionen zwischen handelnden Personen erkannt 
werden.
Dabei wird untersucht, ob ein Satz mehrere Figuren erwähnt.
Mittels des BERT-Modells wird eine Sentimentanalyse durchgeführt, um das 
Sentiment der einzelnen Sätze zu untersuchen.

Gibt es in dem Satz zwei handelnde Personen, dann wird der zugehörige 
Sentiment-Score auf die jeweilige Beziehung zwischen zwei Figuren addiert.

Der ermittelte Graph wird visuell dargestellt.
Dabei entsprechen die Knoten einzelnen Figuren, die Kanten den Beziehungen der 
Figuren untereinander.

Knoten werden je nachdem, ob sie positiv oder negativ beschrieben werden,
eher grün (positiv) oder rot (negativ) dargestellt.
Die Kanten werden dicker, je mehr Interaktionen es zwischen den Figuren gibt.
Auch diese werden je nachdem, ob es sich um positive oder negative Interaktionen
handelt, eher grün (positiv) oder eher rot (negativ) eingefärbt.

## Installation

Mittels

```
$ pip3 install -r requirements.txt
```

können die notwendigen Abhängigkeiten installiert werden.

Anschließend kann das Jupyter Notebook mittels

```
$ jupyter notebook
```

gestartet und geöffnet werden.