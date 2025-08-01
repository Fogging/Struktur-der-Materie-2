<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.2
language: de
narrator: Deutsch Female
comment:  Struktur der Materie 2 - Übung 11

@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md
import: https://github.com/liascript/CodeRunner
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 11

                                      {{1}}
Zur [[ (Minimierung) | Maximierung ]] der magnetischen Feldenergie zerfällt ein Ferromagnet in Domänen.

                                      {{2}}
Oberhalb der Curie-Temperatur [[ verstärkt sich | (verschwindet) | dreht sich ]] die magnetische Ordnung in einem Ferromagneten.

                                      {{3}}
Die spontane Magnetisierung eines ferromagnetischen Materials [[ verschwindet | (verbleibt) | verstärkt sich ]] ohne äußeres Magnetfeld.


## Aufgabe 1 

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
$$B = \mu_0 (H + M) = \mu_0 H \cdot (1 + \chi) = \mu_0 H_\mathrm{a} \cdot \frac{1 + \chi}{1 + N \cdot \chi}$$

                                      {{5}}
Da nur $H_\mathrm{a}$ messbar ist, bezieht man üblicherweise die Suszeptibilität auf das externe Feld $H_\mathrm{a}$ anstatt auf $H$ im Probeninneren:
$$\chi ' = \frac{M}{H_\mathrm{a}} = \frac{\chi \cdot H}{H_\mathrm{a}} = \frac{\chi}{1 + N \cdot \chi}$$

                                      {{6}}
Typische Werte für $\chi$ für dia- und paramagnetische Proben liegen im Bereich von $-10^{-6}$ bis $+10^{-2}$ und für $N = \frac{1}{3}$ (Kugel) folgt:
$$N \cdot \chi \ll 1$$

                                      {{7}}
Es ist also $\chi ' \approx \chi$, d. h. der Unterschied zwischen $H$ und $H_\mathrm{a}$ kann bei der Untersuchung dia- und paramagnetischer Proben vernachlässigt werden.


## Aufgabe 2

> Aus welchem Grund weisen ferromagnetische Stoffe nichtlineare Magnetisierungskurven auf? Welche Unterschiede bestehen zwischen der gemessenen Magnetisierungskurve $M(H_\mathrm{a})$ und der auf das innere Magnetfeld bezogenen Magnetisierungskurve $M(H)$ einer ferromagnetischen Substanz?

                                      {{1}}
- Ferromagnetische Substanzen bestehen aus kleinen Bereichen homogener spontaner Magnetisierung („Domänen“).
- Bei kleinen Feldstärken kommt es zu Wandverschiebungen zwischen benachbarten Domänen, die zur Volumenzunahme der Domänen mit zum äußeren Feld günstiger Magnetisierungsrichtung führen.
- Bei höheren Feldstärken erfolgt zudem eine Drehung der Magnetisierungsrichtung von Domänen in Richtung des äußeren Feldes.

                                      {{2}}
************************************
Gegenüber der Magnetisierungskurve $M(H)$ weist eine auf das äußere Magnetfeld bezogene Magnetisierungskurve $M(H_\mathrm{a})$ eine von der Probengeometrie abhängige „Scherung“ (gedrückte Kurve) auf.

![Magnetisierungskurve für eine ferromagnetische Substanz: auf das äußere Magnetfeld $H_\mathrm{a}$ bezogen (links) bzw. auf das innere Magnetfeld $H$ bezogen (rechts)](Bilder/Magnetisierungskurve_ferromagnetisch.png "Magnetisierungskurve für eine ferromagnetische Substanz: auf das äußere Magnetfeld $H_\mathrm{a}$ bezogen (links) bzw. auf das innere Magnetfeld $H$ bezogen (rechts) *Quelle: Hartmut Stöcker, [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/)*")<!-- style = "width: 500px;" -->
************************************

                                      {{3}}
- Die Koerzitivfeldstärke $H_\mathrm{K}$ (für $M = 0$) bleibt für beide Kurven erhalten.
- Die wirkliche Remanenz $M_\mathrm{R}$ (für $H = 0$) lässt sich nur aus $M(H)$ bestimmen!
- Die Fläche innerhalb der Hysteresekurve entspricht der Magnetisierungsenergie: $\oint M \, \mathrm{d}H = E_\mathrm{mag}$


## Aufgabe 3

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
**Für $\theta = 0$** liegen keine magnetischen Kooperativ-Effekte vor (d. h. idealer Spin-Paramagnetismus, siehe Übung 9, Aufgabe 4) und man erhält das Curie-Gesetz:
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


## Aufgabe 4 

> Berechnen Sie aus der im paramagnetischen Temperaturbereich ermittelten Curie-Konstanten $C$, der Sättigungsmagnetisierung $M_\mathrm{m}$ und der Atomdichte (Gitterparameter) das effektive magnetische Moment $\mu_\mathrm{eff}$ und das maximale magnetische Moment $\mu_\mathrm{m}$ für die Elemente:
>
> a) Eisen: bcc, $a = 2,\!867~\mathrm{Å}$, $C = 2,\!22~\mathrm{K}$, $M_\mathrm{m} = 1,\!75 \cdot 10^6~\mathrm{A/m}$
> 
> b) Gadolinium: hcp, $a = 3,\!636~\mathrm{Å}$, $c = 5,\!783~\mathrm{Å}$, $C = 5,\!00~\mathrm{K}$, $M_\mathrm{m} = 2,\!06 \cdot 10^6~\mathrm{A/m}$


                                      {{1}}
************************************
**a) Eisen**

Die Teilchendichte $n$ erhalten wir aus der Anzahl der Atome pro Elementarzellvolumen:
$$n = \frac{2}{a^3} = 8,\!49 \cdot 10^{22}~\mathrm{cm^{-3}}$$
************************************

                                      {{2}}
Für das effektive magnetische Moment gilt:
$$\mu_\mathrm{eff} = \sqrt{\frac{3 k_\mathrm{B} C}{\mu_0 n}} = 3,\!17 \, \mu_\mathrm{B}$$

                                      {{3}}
Aus der gegebenen Sättigungsmagnetisierung erhalten wir:
$$\mu_\mathrm{m} = \frac{M_\mathrm{m}}{n} = 2,\!22 \, \mu_\mathrm{B}$$

                                      {{4}}
Das Ion Fe^3+^ besitzt die Konfiguration $\mathrm{[Ar] \, 3d^5}$ und durch Anwenden der Hundschen Regeln erhalten wir: $S = 5/2$, $L = 0$ und $J = 5/2$ (siehe Übung 10, Aufgabe 5). Daraus folgt $g=2$ und:
$$\mu_\mathrm{eff} = g \cdot \sqrt{J(J+1)} \cdot \mu_\mathrm{B} = 5,\!92 \, \mu_\mathrm{B} ~~ \text{und} ~~ \mu_\mathrm{m} = g \cdot J \cdot \mu_\mathrm{B} = 5 \, \mu_\mathrm{B}$$

                                      {{5}}
Wir erhalten für Eisen also keine Übereinstimmung zwischen dem theoretischen Wert für Fe^3+^ und den in der Aufgabenstellung gegebenen experimentellen Werten. Ursache ist der vorliegende **Bandferromagnetismus**! Ursache des Ferromagnetismus sind hier keine lokalisierten Elektronen, sondern die Leitungselektronen.

                                      {{6}}
************************************
**b) Gadolinium**

Die Teilchendichte $n$ erhalten wir aus der Anzahl der Atome pro Elementarzellvolumen:
$$n = \frac{2}{\frac{\sqrt{3}}{2} a^2 c} = 3,\!02 \cdot 10^{22}~\mathrm{cm^{-3}}$$
************************************

                                      {{7}}
Für das effektive magnetische Moment gilt:
$$\mu_\mathrm{eff} = \sqrt{\frac{3 k_\mathrm{B} C}{\mu_0 n}} = 7,\!96 \, \mu_\mathrm{B}$$

                                      {{8}}
Aus der gegebenen Sättigungsmagnetisierung erhalten wir:
$$\mu_\mathrm{m} = \frac{M_\mathrm{m}}{n} = 7,\!35 \, \mu_\mathrm{B}$$

                                      {{9}}
Das Ion Gd^3+^ besitzt die Konfiguration $\mathrm{[Xe]\,4f^7}$ und durch Anwenden der Hundschen Regeln erhalten wir: $S = 7/2$, $L = 0$ und $J = 7/2$. Daraus folgt $g=2$ und:
$$\mu_\mathrm{eff} = g \cdot \sqrt{J(J+1)} \cdot \mu_\mathrm{B} = 7,\!94 \, \mu_\mathrm{B} ~~ \text{und} ~~ \mu_\mathrm{m} = g \cdot J \cdot \mu_\mathrm{B} = 7 \, \mu_\mathrm{B}$$

                                      {{10}}
Wir erhalten für Gadolinium also eine gute Übereinstimmung zwischen Theorie und Experiment. Es liegt reiner **Spin-Magnetismus** vor (weil Bahndrehimpuls $L=0$), der von lokalisierten Elektronen ausgeht.