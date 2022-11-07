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

`\documentclass[]{letter}`

`\usepackage{lipsum}`

`\usepackage{polyglossia}`

`\setmainlanguage{polish}`

`\begin{document}`

`\begin{letter}{Szanowny Panie XY}`

`\address{Adres do korespondencji}`

`\opening{}`

`\lipsum[2]`

`\signature{Nadawca}`

`\closing{Pozdrawiam}`

`\end{letter}`

`\end{document}`


 ![alt](Aspose.Words.6c293c22-22c9-4077-926c-4deb54635b92.002.png)


 Przykład kodu *XML* – fragment dokumentu SVG (Scalar Vector Graphics)


`<!DOCTYPE html>`

`<html>`

`<body>`

`<svg height="100" width="100">`

`<circle cx="50" cy="50" r="40" stroke="black" stroke-width="3" fill="red" />`

`</svg>`

`</body>`

`</html>`



![alt](Aspose.Words.6c293c22-22c9-4077-926c-4deb54635b92.003.png)


W tym przypadku mamy np. znacznik np. `<circle>` opisujący parametry koła i który może być właściwie zinterpretowany przez dedykowaną aplikację (np. przeglądarki www).
Jako ciekawostkę można podać fakt, że również pakiet MS Office wykorzystuje format XML do przechowywania informacji o dodatkowych parametrach formatowania danych. Na przykład pliki z rozszerzeniem docx, to nic innego jak spakowane algorytmem zip katalogi z plikami xml.

Archive: test.docx
Length Date Time Name
--------- ---------- ----- ----
573 2022-03-20 08:55 _rels/.rels

731 2022-03-20 08:55 docProps/core.xml

508 2022-03-20 08:55 docProps/app.xml

531 2022-03-20 08:55 word/_rels/document.xml.rels

1288 2022-03-20 08:55 word/document.xml

2429 2022-03-20 08:55 word/styles.xml

853 2022-03-20 08:55 word/fontTable.xml

257 2022-03-20 08:55 word/settings.xml

1374 2022-03-20 08:55 [Content_Types].xml

Wszystkie te języki znaczników cechują się rozbudowaną i złożoną składnią i dlatego do ich edycji wymagają najczęściej dedykowanych narzędzi w postaci specjalizowanych edytorów. By wyeliminować powyższą niedogodność powstał **Markdown** - uproszczony język znaczników służący do formatowania dokumentów tekstowych (bez konieczności używania specjalizowanych narzędzi). Dokumenty w tym formacie można bardzo łatwo konwertować do wielu innych formatów: np. html, pdf, ps (postscript), epub, xml i wiele innych. Format ten jest powszechnie używany do tworzenia plików README.md (w projektach open source) i powszechnie obsługiwany przez serwery git’a. Język ten został stworzony w 2004 r. a jego twórcami byli John Gruber i Aaron Swartz. W kolejnych latach podjęto prace w celu stworzenia standardu rozwiązania i tak w 2016 r. opublikowano dokument RFC 7764 który zawiera opis kilku odmian tegoż języka:

* CommonMark,
* GitHub Flavored Markdown (GFM),
* Markdown Extra.

## Podstawy składni

Podany link: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet zawiera opis podstawowych elementów składni w języku angielskim. Poniżej zostanie przedstawiony ich krótki opis w języku polskim.

### Definiowanie nagłówków
W tym celu używamy znaku kratki
Lewe okno zawiera kod źródłowy – prawe -podgląd przetworzonego tekstu

![alt](Aspose.Words.6c293c22-22c9-4077-926c-4deb54635b92.004.jpeg)


### Definiowanie list
![alt](Aspose.Words.6c293c22-22c9-4077-926c-4deb54635b92.005.jpeg)

Listy numerowane definiujemy wstawiając numery kolejnych pozycji zakończone kropką.

Listy nienumerowane definiujemy znakami: *,+,-

### Wyróżnianie tekstu
![alt](Aspose.Words.6c293c22-22c9-4077-926c-4deb54635b92.006.png)
### Tabele
![alt](Aspose.Words.6c293c22-22c9-4077-926c-4deb54635b92.007.png)

Centrowanie zawartości kolumn realizowane jest poprzez odpowiednie użycie znaku dwukropka:

### Odnośniki do zasobów

[odnośnik do zasobów](www.gazeta.pl pl)

[odnośnik do pliku](LICENSE.md)

[odnośnik do kolejnego zasobu][1]

[1]: http://google.com
`[1]:http://google.com`

#### Obrazki

`![alt text](https://server.com/images/icon48.png "Logo 1")` – obrazek z zasobów internetowych

`![](logo.png)` – obraz z lokalnych zasobów


#### **Kod źródłowy dla różnych języków programowania**
![alt](Aspose.Words.6c293c22-22c9-4077-926c-4deb54635b92.008.png)

#### **Tworzenie spisu treści na podstawie nagłówków**
![alt](Aspose.Words.6c293c22-22c9-4077-926c-4deb54635b92.009.jpeg)

### **Edytory dedykowane**

Pracę nad dokumentami w formacie Markdown( rozszerzenie md) można wykonywać w dowolnym edytorze tekstowym. Aczkolwiek istnieje wiele dedykowanych narzędzi

1. marktext - https://github.com/marktext/marktext
2. https://hackmd.io/ online editor
3. Visual Studio Code z wtyczką „markdown preview”

![alt](Aspose.Words.6c293c22-22c9-4077-926c-4deb54635b92.010.jpeg)

## Pandoc – system do konwersji dokumentów Markdown do innych formatów

Jest oprogramowanie typu open source służące do konwertowania dokumentów pomiędzy różnymi formatami.

Pod poniższym linkiem można obejrzeć przykłady użycia:

https://pandoc.org/demos.html

Oprogramowanie to można pobrać z spod adresu: https://pandoc.org/installing.html

Jeżeli chcemy konwertować do formatu latex i pdf trzeba doinstalować oprogramowanie składu Latex (np. Na windows najlepiej sprawdzi się Miktex https://miktex.org/)

Gdyby podczas konwersji do formatu pdf pojawił się komunikat o niemożliwości znalezienia programu pdflatex rozwiązaniem jest wskazanie w zmiennej środowiskowej PATH miejsca jego położenia

![alt](Aspose.Words.6c293c22-22c9-4077-926c-4deb54635b92.011.png)

![alt](Aspose.Words.6c293c22-22c9-4077-926c-4deb54635b92.012.jpeg)

Pod adresem (https://gitlab.com/mniewins66/templatemn.git) znajduje się przykładowy plik Markdown z którego można wygenerować prezentację w formacie pdf wykorzystując klasę latexa beamer.

W tym celu należy wydać polecenie z poziomu terminala:

$pandoc templateMN.md -t beamer -o prezentacja.pdf

