Polskie znaki są prawidłowo wyświetlanie na stronie internetowej,
jeśli kodowanie pliku z kodem HTML strony zgadza się z kodowaniem
ustawionym w przeglądarce internetowej.

Jeszcze niedawno najpopularniejszym kodowaniem dla stron
angielskojęzycznych było `iso-8859-1`, a dla stron polskojęzycznych
`iso-8852-2` zwane również `Latin-2`. Obecnie standardem jest
kodowanie `utf-8`, które zawiera znaki dla wszystkich alfabetów
łacińskich (i nie tylko).

Aby sprawdzić rodzaj zastosowanego kodowanie dla pliku wystarczy
posłużyć się poleceniem:

    $ file --mime index.html 

które na wyjściu powinno zwrócić:

    index.html: text/html; charset=utf-8
    
Jeśli kodowanie wymaga zmiany, to można się posłużyć programem
`iconv`. Przykładowo, aby zmienić kodowanie pliku z `iso-8859-2` na
`utf-8` należy wykonać polecenie:

    $ iconv -f ISO-8859-2 -t UTF-8 index.html

Wiele przeglądarek internetowych albo rozpoznaje kodowanie `utf-8`
albo, jeśli nie może rozpoznać kodowania to zakłada, że jest to
właśnie to kodowanie. Mimo tego zdecydowana większość twórców stron
zamieszcza w kodzie strony internetowej informację dla przeglądarki o
rodzaju stosowanego kodowania. Służy do tego znacznik `<meta>`. W
HTML5 deklaracja kodowania wygląda następująco:

    <html>
      <head>
        <meta charset="utf-8" />    
        ...
      </head>
      <body>
        ...
      </body>
    </html>

Przeglądarka po odczytaniu tego kodu będzie dekodować znaki na stronie
używając kodowania `utf-8`, nawet jeśli plik nie jest zakodowany w tym
standardzie.
