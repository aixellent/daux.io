## SASS / SCSS

###Rundungsfehler bei der dynamischen Einheitenberechnung
Die Berechnungen mit SASS+Einheiten(z.B. REM) kann trotz einer höheren Genauigkeit (--precision 9) zu erheblichen Rundungsfehlern führen, was daran erkannt werden kann, dass node-sass trotzdem einfach auf 5 Stellen hinter dem Komma rundet. Das fehlerfreie Funktionieren des Responsive Designs mit der Einheit REM benötigt aber mindestens 7 Stellen damit es funktioniert.

**Die Fehlerquelle ist folgende:**

Versucht man den REM Wert wie folgt zu berechnen `1/3 +rem` errechnet der Kompiler daraus den Wert `0.33337rem`.

**Dieses Problem kann mit Interpolation behoben werden:**

**Link:** http://sass-lang.com/documentation/file.SASS_REFERENCE.html#interpolation_

Besitzen die Werte Einheiten, müssen diese dann allerdings die gleich sein (hier px)

`.selector { font-size: #{(24px / 16px)}rem; }`

Einheitenlos geht hier auch

`.selector { font-size: #{(24 / 16)}rem; }`

Bei Variablen bitte darauf achten das alle Variablen entweder die selbe Einheit oder keine Einheit besitzen

`.selector { font-size: #{($variable1/ $variable2 )}rem; }`

Dabei kann auch auf die innere Klammerung (runde Klammern) verzichtet werden

`.selector { font-size: #{$variable1/ $variable2 }rem; }`

Bitte sämtliche Stellen mit `1/x+rem` oder `x/y+rem` o.ä. wie zuvor beschrieben korrigieren und verifizieren das die Werte erst auf 7 Nachkommastellen gerundet werden.