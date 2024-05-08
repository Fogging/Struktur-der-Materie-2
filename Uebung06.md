<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.0.1
language: de
narrator: Deutsch Female
comment:  Struktur der Materie 2 - Übung 06

@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md
import: https://github.com/liascript/CodeRunner
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 6


## Aufgabe 1

> Die magnetische Suszeptibilität einer ferro- bzw. antiferromagnetischen Substanz wird durch das Curie-Weiss-Gesetz $\chi = C/(T-\theta)$ beschrieben. Erklären Sie die Bedeutung der Parameter, welche in dieser Formel auftreten. Welches Vorzeichen besitzt die Größe $\theta$, wenn zwischen den magnetischen Momenten der Substanz eine ferromagnetische bzw. antiferromagnetische Wechselwirkung herrscht? Skizzieren Sie die entsprechenden Graphen in Abhängigkeit von der Temperatur.

                                      {{1}}
Das erweiterte Curie-Weiss-Gesetz hat die Form:
$$\chi = \chi_0 + \frac{C}{T - \theta}$$
Dabei ist $\chi_0$ ein temperaturunabhängiger Anteil (z. B. der diamagnetische Anteil abgeschlossener Elektronenschalen, van Vleck-Paramagnetismus, Paramagnetismus eines Elektronengases u. a.) und soll hier nicht weiter betrachtet werden.

                                      {{2}}
Das Curie-Weiss-Gesetz hat dann die Form:
$$\chi = \frac{C}{T-\theta}$$
Hierbei sind $C$ die Curie-Konstante und $\theta$ die paramagnetische Curie-Temperatur (bzw. der Ordnungsparameter).

                                      {{3}}
**Für $\theta = 0$** liegen keine magnetischen Kooperativ-Effekte vor (d. h. idealer Spin-Paramagnetismus, siehe Übung 4, Aufgabe 4) und man erhält das Curie-Gesetz:
$$\chi = \frac{C}{T}$$

                                      {{4}}
**Für $\theta > 0$** existiert eine ferromagnetische Wechselwirkung (parallele Ausrichtung der Spins):
$$\chi = \frac{C}{T - \theta} \approx \frac{C}{T - T_\mathrm{C}}$$
Das Curie-Weiss-Gesetz beschreibt hier die Temperaturabhängigkeit der magnetischen Suszeptibilität eines Ferromagneten in der Hochtemperaturphase, d. h. oberhalb der Curie-Temperatur $T_\mathrm{C}$. Experimentell findet man, dass im paramagnetischen Bereich für $T \gg T_\mathrm{C}$ die gemessene Suszeptibilität sehr gut durch ein Curie-Weiss-Gesetz beschrieben werden kann, allerdings mit der paramagnetischen Curie-Temperatur $\theta$, die stets höher ist als die ferromagnetische Curie-Temperatur $T_\mathrm{C}$, oberhalb der die spontane Magnetisierung verschwindet. Die Gleichung besagt, dass die magnetische Suszeptibilität in der paramagnetischen Phase bei Annäherung der Temperatur $T$ von oben an die Curie-Temperatur $\theta$ divergiert.

                                      {{5}}
![Temperaturabhängigkeit der Suszeptibilität (durchgezogen) und der inversen Suszeptibilität (gestrichelt) eines Paramagneten (a) und eines Ferromagneten (b)](Bilder/Ferromagnetismus_chi.png "Temperaturabhängigkeit der Suszeptibilität (durchgezogen) und der inversen Suszeptibilität (gestrichelt) eines Paramagneten (a) und eines Ferromagneten (b). Das Curie-Weiss-Gesetz (gestrichelte Linie in (b)) ist nur weit oberhalb von $T_\mathrm{C}$ eine gute Näherung. Die Extrapolation von $\chi^{-1}(T)$ auf $\chi^{-1} = 0$ ergibt die paramagnetische Curie-Temperatur $\theta$. Diese ist immer größer als $T_\mathrm{C}$. *Quelle: Rudolf Gross und Achim Marx, Vorlesungsskript Festkörperphysik, 2008*")<!-- style = "width: 400px;" -->

                                      {{6}}
**Für $\theta < 0$** existiert eine antiferromagnetische Wechselwirkung (antiparallele Ausrichtung der Spins):
$$\chi = \frac{C}{T - \theta} \approx \frac{C}{T + T_\mathrm{N}}$$
In diesem Fall „divergiert“ die Suszeptibilität der Hochtemperaturphase scheinbar gegen eine negative Temperatur $\theta$. Die Gleichung beschreibt aber nur die Temperaturabhängigkeit der magnetischen Suszeptibilität in der Hochtemperaturphase oberhalb der Néel-Temperatur $T_\mathrm{N}$, wobei $T_\mathrm{N} < | \theta |$. Unterhalb von $T_\mathrm{N}$ ist $\chi$ richtungsabhängig (also ein Tensor).

                                      {{7}}
![Temperaturabhängigkeit der Suszeptibilität (durchgezogen) und der inversen Suszeptibilität (gestrichelt) eines Paramagneten (a) und eines Antiferromagneten (b)](Bilder/Antiferromagnetismus_chi.png "Temperaturabhängigkeit der Suszeptibilität (durchgezogen) und der inversen Suszeptibilität (gestrichelt) eines Paramagneten (a) und eines Antiferromagneten (b). Das Curie-Weiss-Gesetz (gepunktete Linie in (b)) ist nur weit oberhalb von $T_\mathrm{N}$ eine gute Näherung. Die Extrapolation von $\chi^{-1}(T)$ auf $\chi^{-1} = 0$ ergibt die paramagnetische Néel-Temperatur $\theta$. Der Betrag von $\theta$ ist meist größer als $T_\mathrm{N}$. *Quelle: Rudolf Gross und Achim Marx, Vorlesungsskript Festkörperphysik, 2008*")<!-- style = "width: 400px;" -->


## Aufgabe 2 

> Das makroskopische magnetische Feld $H$ im Inneren einer Probe, deren Entmagnetisierungsfaktor den Wert $N$ besitzt, ergibt sich zu $H = H_\mathrm{a} - N \cdot M$, wobei $H_\mathrm{a}$ das äußere Magnetfeld und $M$ die in der Probe vorhandene Magnetisierung bedeuten. Berechnen Sie für den Fall einer linearen Magnetisierungskurve ($M = \chi \cdot H$) die Stärke des makroskopischen Feldes $H$ sowie der magnetischen Induktion $B$ im Probeninneren in Abhängigkeit von der Stärke des äußeren Feldes $H_\mathrm{a}$. Ergibt sich ein merklicher Fehler, wenn der Unterschied zwischen $H$ und $H_\mathrm{a}$ bei der Untersuchung dia- und paramagnetischer Proben vernachlässigt wird?

                                      {{1}}
Der Zusammenhang zwischen dem externen angelegten Magnetfeld $H_\mathrm{a}$ und dem Magnetfeld $H$ im Inneren einer Probe mit Entmagnetisierungsfaktor $N$ lautet gemäß Aufgabenstellung:
$$H = H_\mathrm{a} - N \cdot M = H_\mathrm{a} - N \cdot \chi \cdot H$$

                                      {{2}}
Durch Umstellen erhalten wir:
$$H_\mathrm{a} = H + N \cdot \chi \cdot H = H \cdot (1 + N \cdot \chi)$$

                                      {{3}}
Für das Magnetfeld im Probeninneren ergibt sich:
$$H = \frac{H_\mathrm{a}}{1 + N \cdot \chi}$$

                                      {{4}}
Für die magnetische Induktion folgt:
$$B = \mu_0 (H + M) = \mu_0 H \cdot (1 + \chi) = \mu_0 H_\mathrm{a} \frac{1 + \chi}{1 + N \cdot \chi}$$

                                      {{5}}
Da nur $H_\mathrm{a}$ messbar ist, bezieht man üblicherweise die Suszeptibilität auf das externe Feld $H_\mathrm{a}$ anstatt auf $H$ im Probeninneren:
$$\chi ' = \frac{M}{H_\mathrm{a}} = \frac{\chi \cdot H}{H_\mathrm{a}} = \frac{1}{1 + N \cdot \chi} \chi$$

                                      {{6}}
Typische Werte für $\chi$ für dia- und paramagnetische Proben liegen im Bereich von $-10^{-6}$ bis $+10^{-2}$ und für $N = \frac{1}{3}$ (Kugel)
folgt:
$$N \cdot \chi \ll 1 \ \Rightarrow \ \chi ' \approx \chi$$


## Aufgabe 3

> Aus welchem Grund weisen ferromagnetische Stoffe nichtlineare Magnetisierungskurven auf? Welche Unterschiede bestehen zwischen der gemessenen Magnetisierungskurve $M(H_\mathrm{a})$ und der auf das innere Magnetfeld bezogenen Magnetisierungskurve $M(H)$ einer ferromagnetischen Substanz?

                                      {{1}}
Gemäß Aufgabe 2 besteht der Beitrag des Elektronengases zur magnetischen Suszeptibilität aus einem paramagnetischen Anteil (Pauli-Spinsuszeptibilität) und einem diamagnetischen Anteil (Landau-Spinsuszeptibilität). Für die gesamte magnetische Suszeptibilität hatten wir erhalten:
$$\chi_\mathrm{el} = \mu_0 \mu_\mathrm{B}^2 \frac{n}{E_\mathrm{F}}$$

                                      {{2}}
Hierbei handelt es sich um eine Volumensuszeptibilität. Gesucht ist aber die molare Suszeptibilität, die wir aus $\chi_\mathrm{mol} = \frac{M}{\varrho} \chi_V$ erhalten. Für die Elektronendichte pro Volumen setzen wir noch $n = \frac{\varrho \cdot N_\mathrm{A}}{M}$ ein (siehe Übung 3, Aufgabe 1). Für die molare Suszeptibilität folgt:
$$\chi_\mathrm{el,mol} = \frac{M}{\varrho} \chi_\mathrm{el} = \frac{M}{\varrho} \cdot \mu_0 \mu_\mathrm{B}^2 \frac{\varrho \cdot N_\mathrm{A}}{M \cdot E_\mathrm{F}} = \mu_0 \mu_\mathrm{B}^2 \frac{N_\mathrm{A}}{E_\mathrm{F}} = 5,\!8 \cdot 10^{-11}~\mathrm{m^3/mol}$$

                                      {{3}}
Zusammen mit dem diamagnetischen Anteil der abgeschlossenen Elektronenschalen der Ionenrümpfe (Cu^+^) von $\chi_\mathrm{dia,mol} = -15 \cdot {10}^{-11}~\mathrm{m^3/mol}$ ergibt sich:
$$\chi_\mathrm{mol} = \chi_\mathrm{el,mol} + \chi_\mathrm{dia,mol} = -9,\!2 \cdot 10^{-11}~\mathrm{m^3/mol}$$

                                      {{4}}
Insgesamt liegt also diamagnetisches Verhalten vor. Der Messwert von $\chi_\mathrm{mol} = -6,\!9\cdot{10}^{-11}~\mathrm{m^3/mol}$ wird ungefähr bestätigt.


## Aufgabe 4 

> Berechnen Sie aus der im paramagnetischen Temperaturbereich ermittelten Curie-Konstanten $C$, der Sättigungsmagnetisierung $M_\mathrm{m}$ und der Atomdichte (Gitterparameter) das effektive magnetische Moment $\mu_\mathrm{eff}$ und das maximale magnetische Moment $\mu_\mathrm{m}$ für die Elemente:
>
> a) Eisen: bcc, $a = 2,\!867~\mathrm{Å}$, $C = 2,\!22~\mathrm{K}$, $M_\mathrm{m} = 1,\!746 \cdot 10^6~\mathrm{A/m}$
> 
> b) Gadolinium: hcp, $a = 3,\!636~\mathrm{Å}$, $c = 5,\!783~\mathrm{Å}$, $C = 5~\mathrm{K}$, $M_\mathrm{m} = 2,\!06 \cdot 10^6~\mathrm{A/m}$


                                      {{1}}
Der Messwert beträgt $\chi_\mathrm{mol} = -6,\!9\cdot{10}^{-11}~\mathrm{m^3/mol}$ und rechnet sich wie folgt in eine Volumensuszeptibilität (ohne Einheit) um:
$$\chi_V = \frac{\varrho}{M} \chi_\mathrm{mol} = -9,\!71 \cdot 10^{-6}$$

                                      {{2}}
Die Massensuszeptibilität $\chi_\mathrm{g}$ ergibt sich folgendermaßen:
$$\chi_\mathrm{g} = \frac{1}{\varrho} \chi_V = \frac{1}{M} \chi_\mathrm{mol} = -1,\!09 \cdot 10^{-6}~\mathrm{cm^3/g}$$