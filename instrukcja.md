**Lekcja 1 – Markdown lekki język znaczników** 

**Spis treści** 

Lekcja 1 – Markdown lekki język znaczników 1

Wstęp 1

Podstawy składni 3

Definiowanie nagłówków 3

Definiowanie list 4

Wyróżnianie tekstu 4

Tabele 5

Odnośniki do zasobów 5

Obrazki 5

Kod źródłowy dla różnych języków programowania 5

Tworzenie spisu treści na podstawie nagłówków 6

Edytory dedykowane 7

Pandoc – system do konwersji dokumentów Markdown do innych formatów 8


## Wstęp
Obecnie powszechnie wykorzystuje się języki ze znacznikami do opisania dodatkowych informacji umieszczanych w plikach tekstowych. Z pośród najbardziej popularnych można wspomnieć o:
1. html – służącym do opisu struktury informacji zawartych na stronach internetowych,
2. Tex (Latex) – poznany na zajęciach język do „profesjonalnego” składania tekstów,
3. XML (Extensible Markup Language) - uniwersalnym języku znaczników przeznaczonym do reprezentowania różnych danych w ustrukturalizowany sposób.
   
   Przykład kodu _html_ i jego interpretacja w przeglądarce:
"

`<!DOCTYPE html>`                                       

`<html>`

`<head>`

`<meta charset="utf-8" />`

`<title>Przykład</title>`

`</head>`

`<body>`

`<p> Jakiś paragraf tekstu</p>`

`</body>`

`</html>`

 ![alt](Aspose.Words.6c293c22-22c9-4077-926c-4deb54635b92.001.png)


Przykład kodu Latex i wygenerowanego pliku w formacie pdf

\documentclass[]{letter}

\usepackage{lipsum}

\usepackage{polyglossia}

\setmainlanguage{polish}

\begin{document}

\begin{letter}{Szanowny Panie XY}

\address{Adres do korespondencji}

\opening{}

\lipsum[2]

\signature{Nadawca}

\closing{Pozdrawiam}

\end{letter}

\end{document}


 ![alt](Aspose.Words.6c293c22-22c9-4077-926c-4deb54635b92.002.png)

