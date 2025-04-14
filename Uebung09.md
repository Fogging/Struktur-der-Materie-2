<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.0.1
language: de
narrator: Deutsch Female
comment:  Struktur der Materie 2 - Übung 08

@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md
import: https://github.com/liascript/CodeRunner
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 8


## Aufgabe 1

> Bestimmen Sie den Reflexionskoeffizienten $R$ bei der senkrechten Reflexion. Betrachten Sie eine sich in $z$-Richtung ausbreitende elektromagnetische ebene Welle im Vakuum, welche bei $z=0$ auf die Oberfläche eines Mediums mit komplexem Brechungsindex $n' = n + \mathrm{i} k$ trifft (Herleitung). Berechnen Sie die Werte von $R$ für $n = 1,\!0$ und $1,\!5$ und $3,\!5$ wobei $k=0$ bzw. $10$ betragen soll.

                                      {{1}}
Wir betrachten eine einfallende ebene Welle, deren $E$-Feld in $x$-Richtung schwingt und die sich in $z$-Richtung ausbreitet:
$$E_{x,0} = E_0 \cdot \exp [\mathrm{i} (k_0 z - \omega t)]$$

                                      {{2}}
Die reflektierte Welle besitzt eine veränderte Amplitude $E_2$ und breitet sich in entgegengesetzte Richtung aus:
$$E_{x,2} = E_2 \cdot \exp [\mathrm{i} (-k_0 z - \omega t)]$$

                                      {{3}}
Die ins Medium mit dem komplexen Brechungsindex $n' = n + i \cdot k$ eindringende Welle besitzt die Amplitude $E_1$ und die gleiche Ausbreitungsrichtung wie die einfallende Welle:
$$E_{x,1} = E_1 \cdot \exp [\mathrm{i} (k_0 n' z - \omega t)]$$

                                      {{4}}
Am Ort $z = 0$ und zur Zeit $t = 0$ gilt für die Amplituden:
$$E_1 = E_0 + E_2$$

                                      {{5}}
Für die 1. Ableitung nach $z$ bei $z = 0$ und $t = 0$ gilt:
$$n' E_1 = E_0 - E_2$$

                                      {{6}}
Multiplizieren wir die erste Gleichung mit $n'$ können wir die zwei Gleichungen gleichsetzen und damit $E_1$ eliminieren:
$$n' E_0 + n' E_2 = E_0 - E_2$$

                                      {{7}}
Daraus folgt:
$$(n' - 1) E_0 = - (n' + 1) E_2$$

                                      {{8}}
Der Reflexionsfaktor $r$ für senkrechten Einfall ist damit:
$$r = \frac{E_2}{E_0} = \frac{1 - n'}{1 + n'}$$

                                      {{9}}
Der Reflexionskoeffizient $R$ für senkrechten Einfall ergibt sich entsprechend als:
$$R = r \cdot r^\ast = |r|^2 = \left| \frac{E_2}{E_0} \right|^2 = \left|\frac{1 - n - \mathrm{i} k}{1 + n + \mathrm{i} k} \right|^2 = \frac{(1 - n)^2 + k^2}{(1 + n)^2 + k^2}$$

                                      {{10}}
Ohne Absorption, also für $k = 0$, vereinfacht sich der Ausdruck zu:
$$R = \frac{(n - 1)^2}{(n + 1)^2}$$

                                      {{11}}
************************************
Gemäß der Aufgabenstellung waren folgende Reflexionswerte zu berechnen:

<!-- data-type="none" -->
|             | $k = 0$      | $k = 10$     |
|-------------|--------------|--------------|
| $n = 1$     | $R = 0,\!00$ | $R = 0,\!96$ |
| $n = 1,\!5$ | $R = 0,\!04$ | $R = 0,\!94$ |
| $n = 3,\!5$ | $R = 0,\!31$ | $R = 0,\!88$ |
************************************


## Aufgabe 2 

> Im fernen infraroten Spektralbereich erfüllen Metalle die Bedingung $\omega \tau \ll 1$, so dass ihre komplexe Dielektrizitätszahl näherungsweise durch $\varepsilon' = \mathrm{i} \sigma_0 / \varepsilon_0 \omega$ dargestellt werden kann. Dabei ist $\sigma_0$ die Gleichstromleitfähigkeit. Berechnen Sie den komplexen Brechungsindex eines Metalls und zeigen Sie, dass sich das Reflexionsvermögen im FIR durch das „Hagen-Rubens-Gesetz“ beschreiben lässt.

                                      {{1}}
Die komplexe Dielektrizitätszahl eines Metalls im Infraroten kann näherungsweise dargestellt werden durch:
$$\varepsilon' = \mathrm{i} \frac{\sigma_0}{\varepsilon_0 \omega}$$

                                      {{2}}
Der komplexe Brechungsindex ist entsprechend:
$$n' = \sqrt{\varepsilon'} = \frac{1 + \mathrm{i}}{\sqrt{2}} \sqrt{\frac{\sigma_0}{\varepsilon_0 \omega}}$$

                                      {{3}}
Da der komplexe Brechungsindex als $n' = n + \mathrm{i} k$ darstellbar ist, folgt daraus:
$$n = k = \sqrt{\frac{\sigma_0}{2 \varepsilon_0 \omega}}$$

                                      {{4}}
Die Formel für den Reflexionskoeffizienten $R$ bei senkrechtem Einfall (aus Aufgabe 1) stellen wir zunächst etwas um:
$$R = \frac{(n - 1)^2 + k^2}{(n + 1)^2 + k^2} = \frac{(n + 1)^2 + k^2 - 4n}{(n + 1)^2 + k^2} = 1 - \frac{4n}{(n + 1)^2 + k^2}$$

                                      {{5}}
Für $n = k \gg 1$ können wir die $1$ im Nenner näherungsweise weglassen und den Zusammenhang folgendermaßen vereinfachen:
$$R \approx 1 - \frac{2}{n}$$

                                      {{6}}
Setzen wir die oben erhaltene Formel für $n$ ein, ergibt sich die Hagen-Rubens-Relation:
$$R \approx 1 - \sqrt{\frac{8 \varepsilon_0 \omega}{\sigma_0}}$$


## Aufgabe 3

> Man berechne den Reflexionskoeffizient von Aluminium mit einer spezifischen Leitfähigkeit von $35 \cdot 10^6~\mathrm{\left( \Omega m \right)^{-1}}$ für die Wellenlängen von $10$ und $100~\mathrm{µm}$ nach der Hagen-Rubens-Relation.

                                      {{1}}
Zunächst rechnen wir die gegebenen Wellenlängen in Kreisfrequenzen um:
$$\omega = 2 \pi f = \frac{2 \pi c}{\lambda}$$


                                      {{2}}
Anschließend können wir direkt die Hagen-Rubens-Relation anwenden:
$$R \approx 1 - \sqrt{\frac{8 \varepsilon_0 \omega}{\sigma_0}}$$

                                      {{3}}
************************************
Für die zwei in der Aufgabenstellung genannten Wellenlängen erhalten wir:

<!-- data-type="none" -->
| Wellenlänge $\lambda$ | Kreisfrequenz $\omega$ | Reflexionskoeffizient $R$ |
|-----------------------|------------------------|---------------------------|
| $10~\mathrm{µm}$      | $1,\!88 \cdot 10^{14}~\mathrm{s^{-1}}$  | $0,\!980$ |
| $100~\mathrm{µm}$     | $1,\!88 \cdot 10^{13}~\mathrm{s^{-1}}$  | $0,\!994$ |
************************************

                                      {{4}}
Für sehr gute Leiter (z. B. Al, Cu, Ag) ist im IR-Bereich ein fast ideales Reflexionsvermögen nahe an $R=1$ zu beobachten.


## Aufgabe 4

> Für Kupfer berechne man aus den optischen Konstanten ($n = 0,\!14$, $k = 3,\!35$) die spezifische Leitfähigkeit für die Wellenlänge von $600~\mathrm{nm}$ und vergleiche sie mit Literaturwerten. Wie erklärt man die große Abweichung?

                                      {{1}}
Die verallgemeinerte Permittivität setzt sich zusammen aus:
$$\varepsilon' = \varepsilon_1 + \mathrm{i} \varepsilon_2$$

                                      {{2}}
Der imaginäre Anteil $\varepsilon_2$ hängt direkt mit der Leitfähigkeit $\sigma$ zusammen:
$$\varepsilon_2 = \frac{\sigma}{\varepsilon_0 \omega}$$

                                      {{3}}
Andererseits kann der imaginäre Anteil $\varepsilon_2$ direkt aus den optischen Konstanten ermittelt werden:
$$\varepsilon_2 = 2 n k$$

                                      {{4}}
Gleichsetzen liefert eine Formel für die Leitfähigkeit:
$$\sigma = 2 n k \varepsilon_0 \omega = 2 n k \varepsilon_0 \cdot 2 \pi \frac{c}{\lambda}$$

                                      {{5}}
Mit den gegebenen Werten erhalten wir: $\sigma = 2,\!6 \cdot 10^4~\frac{1}{\mathrm{\Omega m}}$

                                      {{6}}
Der Literaturwert für die spezifische Leitfähigkeit von Kupfer (bei $\omega = 0$) liegt allerdings bei: $\sigma_0 = 5,\!8 \cdot 10^7~\frac{1}{\mathrm{\Omega m}}$

                                      {{7}}
Es ist wichtig, sich klar zu machen, dass eine klare Unterscheidung zwischen freien und gebundenen Ladungsträgern in zeitlich oszillierenden Feldern (z. B. für die Wellenlänge von $600~\mathrm{nm}$) nicht mehr möglich ist. In beiden Fällen haben wir es mit periodischen Verschiebungen von Ladungen zu tun. Nur für $\omega = 0$ können wir das Verhalten von freien und gebundenen Ladungen klar unterscheiden und eine Trennung von Phänomenen, die $\sigma$ bzw. $\varepsilon_2$ zugeordnet werden können, ist evident. Für zeitlich und räumlich variierende Felder ist dies dagegen nicht mehr möglich.


## Aufgabe 5

> Warum kann man die Lage der Plasmafrequenz von Metallen mit Hilfe der „Energieverlustfunktion“ $-\mathrm{Im}(1/\varepsilon')$ ausfindig machen?

                                      {{1}}
Die verallgemeinerte Permittivität setzt sich zusammen aus:
$$\varepsilon' = \varepsilon_1 + \mathrm{i} \varepsilon_2$$

                                      {{2}}
Das Reziproke ist:
$$\frac{1}{\varepsilon'} = \frac{\varepsilon_1 - \mathrm{i} \varepsilon_2}{\varepsilon_1^2 + \varepsilon_2^2}$$

                                      {{3}}
Der negative Imaginärteil dieser Funktion ist:
$$-\mathrm{Im}\left(\frac{1}{\varepsilon'}\right) = \frac{\varepsilon_2}{\varepsilon_1^2 + \varepsilon_2^2}$$

                                      {{4}}
Diese sogenannte „Energieverlustfunktion“ wird also maximal für $\varepsilon_1 \rightarrow 0$. Genau bei der Plasmafrequenz wird ebenfalls $\varepsilon_1 = 0$. Damit kennzeichnet ein Maximum in der Energieverlustfunktion gerade die Lage der Plasmafrequenz.
