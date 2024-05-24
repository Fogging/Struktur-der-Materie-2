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
$$E_x = E_0 \cdot \exp [\mathrm{i} (k_0 z - \omega t)]$$

                                      {{2}}
Die reflektierte Welle besitzt eine veränderte Amplitude $E_2$ und breitet sich in entgegengesetzte Richtung aus:
$$E_x = E_2 \cdot \exp [\mathrm{i} (-k_0 z - \omega t)]$$

                                      {{3}}
Die ins Medium mit dem komplexen Brechungsindex $n' = n + i \cdot k$ eindringende Welle besitzt die Amplitude $E_1$ und die gleiche Ausbreitungsrichtung wie die einfallende Welle:
$$E_x = E_1 \cdot \exp [\mathrm{i} (k_0 n' z - \omega t)]$$

                                      {{4}}
Am Ort $z = 0$ und zur Zeit $t = 0$ gilt für die Amplituden:
$$E_1 = E_0 + E_2$$

                                      {{5}}
Für die 1. Ableitung bei $z = 0$ und $t = 0$ gilt:
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

> Im fernen infraroten Spektralbereich erfüllen Metalle die Bedingung $\omega \tau \ll 1$, so dass ihre komplexe Dielektrizitätszahl näherungsweise durch $\varepsilon' = \mathrm{i} \sigma / \varepsilon_0 \omega$ dargestellt werden kann. Dabei ist $\sigma$ die Gleichstromleitfähigkeit. Berechnen Sie den komplexen Brechungsindex eines Metalls und zeigen Sie, dass sich das Reflexionsvermögen im FIR durch das „Hagen-Rubens-Gesetz“ beschreiben lässt.

                                      {{1}}
Analog zum magnetischen Feld setzt sich das elektrische Feld $E$ im Inneren eines Körpers aus dem äußeren Feld $E_\mathrm{a}$ und dem Entelektrisierfeld $E_N$ zusammen:
$$E = E_\mathrm{a} - E_N$$

                                      {{2}}
Der Grund für die Entelektrisierung liegt in der elektrischen Polarisation $P$, also der Erzeugung bzw. Ausrichtung mikroskopischer Dipole, die zur Ausbildung von Oberflächenladungen führt. Diese Oberflächenladungen erzeugen das entelektrisierende Feld, das dem äußeren Feld entgegenwirkt. Das Entelektrisierfeld beträgt $E_N = N P / \varepsilon_0$, das heißt:
$$E = E_\mathrm{a} - \frac{N P}{\varepsilon_0}$$

                                      {{3}}
Die Polarisation hängt gemäß $P = \chi \varepsilon_0 E$ über die elektrische Suszeptibilität $\chi$ des Mediums direkt mit der lokalen elektrischen Feldstärke $E$ zusammen. Daraus folgt:
$$E = E_\mathrm{a} - N \chi E$$

                                      {{4}}
Für das elektrische Feld im Inneren des Dielektrikums erhalten wir also:
$$E = \frac{1}{1 + N \chi} E_\mathrm{a}$$

                                      {{5}}
Für die dielektrische Verschiebung gilt:
$$D = \varepsilon_0 E + P = \varepsilon_0 E + \chi \varepsilon_0 E = (1 + \chi) \varepsilon_0 E$$

                                      {{6}}
Der Zusammenhang mit der äußeren Feldstärke $E_\mathrm{a}$ lautet:
$$D = \frac{1 + \chi}{1 + N \chi} \varepsilon_0 E_\mathrm{a}$$

                                      {{7}}
Für eine dielektrische Kugel mit Entelektrisierungsfaktor $N = 1/3$ und $\varepsilon_\mathrm{r} = 2,\!3$ folgt:
$$\chi = \varepsilon_\mathrm{r} - 1 = 1,\!3$$
$$E = \frac{1}{1 + 1,\!3/3} E_\mathrm{a} = 0,\!698 \cdot E_\mathrm{a}$$
$$P = \frac{1,\!3}{1 + 1,\!3/3} \varepsilon_0 E_\mathrm{a} = 0,\!907 \cdot \varepsilon_0 E_\mathrm{a}$$


## Aufgabe 3

> Man berechne den Reflexionskoeffizient von Aluminium mit einer spezifischen Leitfähigkeit von $35 \cdot 10^6~\mathrm{\left( \Omega m \right)^{-1}}$ für die Wellenlängen von $10$ und $100~\mathrm{µm}$ nach der Hagen-Rubens-Relation.

                                      {{1}}
Die Plasmafrequenz berechnet sich gemäß:
$$\omega_\mathrm{p} = \sqrt{\frac{e^2 n}{\varepsilon_0 \varepsilon_\mathrm{r} m^\ast}}$$

                                      {{2}}
Für Metalle können wir $\varepsilon_\mathrm{r} \approx 1$ benutzen.

                                      {{3}}
Für die Plasmonenenergie gilt entsprechend:
$$E_\mathrm{p} = \hbar \omega_\mathrm{p}$$

                                      {{4}}
Da $c = \lambda f$ und $\omega = 2 \pi f$, folgt für die entsprechende Wellenlänge:
$$\lambda_\mathrm{p} = \frac{2 \pi c}{\omega_\mathrm{p}}$$

                                      {{5}}
************************************
Für die drei in der Aufgabenstellung genannten Materialien erhalten wir:

<!-- data-type="none" -->
| Material  | $\omega_\mathrm{p}$                    | $E_\mathrm{p}$       | $\lambda_\mathrm{p}$ |
|-----------|----------------------------------------|----------------------|----------------------|
| Silber    | $1,\!35 \cdot 10^{16}~\mathrm{s^{-1}}$ | $8,\!86~\mathrm{eV}$ | $140~\mathrm{nm}$    |
| Aluminium | $1,\!96 \cdot 10^{16}~\mathrm{s^{-1}}$ | $12,\!9~\mathrm{eV}$ | $96~\mathrm{nm}$    |
| Silizium  | $7,\!23 \cdot 10^{13}~\mathrm{s^{-1}}$ | $0,\!048~\mathrm{eV}$ | $26~\mathrm{µm}$    |
************************************

                                      {{6}}
Die Wellenlänge, ab welcher das Reflexionsvermögen deutlich ansteigt, liegt für Metalle also im UV-Bereich und für Halbleiter im fernen Infrarot.


## Aufgabe 4

> Für Kupfer berechne man aus den optischen Konstanten ($n = 0,\!14$, $k = 3,\!35$) die spezifische Leitfähigkeit für die Wellenlänge von $600~\mathrm{nm}$ und vergleiche sie mit Literaturwerten. Wie erklärt man die große Abweichung?

                                      {{1}}
Die Gleichstromleitfähigkeit nach Drude erhalten wir aus:
$$\sigma(0) = \frac{e^2 n \tau}{m^\ast} = \varepsilon_0 \varepsilon_\mathrm{r} \tau \omega_\mathrm{p}^2$$

                                      {{2}}
Aus den gegebenen Werten ergibt sich:
$$\sigma(0) = 1,\!06 \cdot 10^5~\mathrm{\frac{1}{\Omega m}}$$

                                      {{3}}
Das Reziproke der Leitfähigkeit ist der spezifische Widerstand:
$$\rho(0) = \frac{1}{\sigma(0)} = 9,\!4 \cdot 10^{-6}~\mathrm{\Omega m}$$


## Aufgabe 5

> Warum kann man die Lage der Plasmafrequenz von Metallen mit Hilfe der „Energieverlustfunktion“ $-\mathrm{Im}(1/\varepsilon')$ ausfindig machen?

                                      {{1}}
Die Gleichstromleitfähigkeit nach Drude erhalten wir aus:
$$\sigma(0) = \frac{e^2 n \tau}{m^\ast} = \varepsilon_0 \varepsilon_\mathrm{r} \tau \omega_\mathrm{p}^2$$

                                      {{2}}
Aus den gegebenen Werten ergibt sich:
$$\sigma(0) = 1,\!06 \cdot 10^5~\mathrm{\frac{1}{\Omega m}}$$

                                      {{3}}
Das Reziproke der Leitfähigkeit ist der spezifische Widerstand:
$$\rho(0) = \frac{1}{\sigma(0)} = 9,\!4 \cdot 10^{-6}~\mathrm{\Omega m}$$