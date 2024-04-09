<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.0.1
language: de
narrator: Deutsch Female
comment:  Struktur der Materie 2 - Übung 02

@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md
import: https://github.com/liascript/CodeRunner
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 2


## Aufgabe 1

> Zeigen Sie, dass das Produkt aus Majoritäts- und Minoritätsladungsträgerdichte für einen gegebenen Halbleiter und eine vorgegebene Temperatur konstant ist.

                                      {{1}}
Für die Herleitung beginnen wir mit den Formeln für die Elektronenkonzentration $n$ und die Löcherkonzentration $p$:
$$n = N_\mathrm{L} \cdot \exp \left( - \frac{E_\mathrm{L} - E_\mathrm{F}}{k_\mathrm{B} T} \right)$$
$$p = N_\mathrm{V} \cdot \exp \left( \frac{E_\mathrm{V} - E_\mathrm{F}}{k_\mathrm{B} T} \right)$$

                                      {{2}}
Die gesuchte Größe ist das Produkt $n \cdot p$, für das folgt:
$$n \cdot p = N_\mathrm{L} \cdot N_\mathrm{V} \cdot \exp \left( - \frac{E_\mathrm{L} - E_\mathrm{F}}{k_\mathrm{B} T} \right) \cdot \exp \left( \frac{E_\mathrm{V} - E_\mathrm{F}}{k_\mathrm{B} T} \right)$$
$$n \cdot p = N_\mathrm{L} N_\mathrm{V} \cdot \exp \left( - \frac{E_\mathrm{L} - E_\mathrm{F} - E_\mathrm{V} + E_\mathrm{F}}{k_\mathrm{B} T} \right)$$

                                      {{3}}
Da $E_\mathrm{L} - E_\mathrm{V} = E_\mathrm{g}$ gerade die Bandlücke ergibt, erhält man:
$$n \cdot p = N_\mathrm{L} N_\mathrm{V} \cdot \exp \left( - \frac{E_\mathrm{g}}{k_\mathrm{B} T} \right)$$

                                      {{4}}
Schreibt man die effektiven Zustandsdichten $N_\mathrm{L}$ und $N_\mathrm{V}$ aus, erkennt man die vollständige Temperaturabhängigkeit:
$$n \cdot p = 4 \left( \frac{k_\mathrm{B} T}{2 \pi \hbar^2} \right)^3 \left( m_\mathrm{e}^\mathrm{eff} m_\mathrm{h}^\mathrm{eff} \right)^{3/2} \cdot \exp \left( - \frac{E_\mathrm{g}}{k_\mathrm{B} T} \right)$$

                                      {{5}}
Damit ist das Produkt $n \cdot p$ nur von der Temperatur $T$, den effektiven Massen $m_\mathrm{e}^\mathrm{eff}$ und $m_\mathrm{h}^\mathrm{eff}$ sowie der Bandlücke $E_\mathrm{g}$ des betrachteten Halbleiters abhängig. Dieser Zusammenhang gilt für intrinsische und dotierte Halbleiter (aber nicht für entartete Halbleiter) und wird als **Massenwirkungsgesetz** bezeichnet.

                                      {{6}}
Für einen intrinsischen Halbleiter ist $n_i = p_i$ und es gilt:
$$n \cdot p = n_i \cdot p_i = n_i^2 = N_\mathrm{L} N_\mathrm{V} \cdot \exp \left( - \frac{E_\mathrm{g}}{k_\mathrm{B} T} \right)$$

                                      {{7}}
Daraus folgt:
$$n_i = p_i = \sqrt{N_\mathrm{L} N_\mathrm{V}} \cdot \exp \left( - \frac{E_\mathrm{g}}{2 k_\mathrm{B} T} \right)$$


## Aufgabe 2 

> Die Temperatur eigenleitenden Siliziums wird von -20 °C auf 200 °C erhöht. Wie ändert sich die Elektronenkonzentration (Quotient beider Konzentrationen)?

                                      {{1}}
Gemäß Aufgabe 1 gilt:
$$n_i = \sqrt{N_\mathrm{L} N_\mathrm{V}} \cdot \exp \left( - \frac{E_\mathrm{g}}{2 k_\mathrm{B} T} \right) = 2 \left( \frac{k_\mathrm{B} T}{2 \pi \hbar^2} \right)^{3/2} \left( m_\mathrm{e}^\mathrm{eff} m_\mathrm{h}^\mathrm{eff} \right)^{3/4} \cdot \exp \left( - \frac{E_\mathrm{g}}{2 k_\mathrm{B} T} \right)$$

                                      {{2}}
Zu vergleichen sind die Temperaturen $T_1 = 253~\mathrm{K}$ und $T_2 = 473~\mathrm{K}$. Bildet man das Verhältnis der zwei Elektronenkonzentrationen bei diesen Temperaturen, erhält man:
$$\frac{n_2}{n_1} = \left( \frac{T_2}{T_1} \right)^{3/2} \cdot \frac{\exp \left( - \frac{E_\mathrm{g}}{2 k_\mathrm{B} T_2} \right)}{\exp \left( - \frac{E_\mathrm{g}}{2 k_\mathrm{B} T_1} \right)} = \left( \frac{T_2}{T_1} \right)^{3/2} \cdot \exp \left[ - \frac{E_\mathrm{g}}{2 k_\mathrm{B}} \left( \frac{1}{T_2} - \frac{1}{T_1} \right) \right]$$

                                      {{3}}
Wir nehmen an, dass die Bandlückenenergie ungefähr konstant bleibt. (Eigentlich gibt es eine leichte Temperaturabhängigkeit.) Der Wert für Silizium bei Raumtemperatur ist $E_\mathrm{g} = 1,\!12~\mathrm{eV}$. Damit ergibt sich:
$$\frac{n_2}{n_1} = 3,\!95 \cdot 10^5$$

                                      {{4}}
Die Elektronenkonzentration nimmt also zwischen -20 °C und 200 °C um mehr als fünf Größenordnungen zu.


## Aufgabe 3

> Bestimmen Sie die Dotierstoffkonzentration in Silizium, wenn eins von einer Million Si-Atome durch ein Bor-Atom ersetzt wird (molare Masse von Si: 28 g/mol, Dichte: 2,3 g/cm³).

                                      {{1}}
Die Stoffmenge $n$ (*Bitte nicht mit einer Elektronenkonzentration verwechseln!*) erhalten wir entweder aus der Anzahl der Teilchen $N$ geteilt durch die Avogadro-Konstante $N_\mathrm{A}$ oder aus der Masse $m$ geteilt durch die molare Masse $M$:
$$n = \frac{N}{N_\mathrm{A}} = \frac{m}{M}$$

                                      {{2}}
Die Konzentration der Silizium-Atome ist die Anzahl der Atome $N$ pro Volumen $V$. Wir bezeichnen sie mit $n_\mathrm{Si}$. Aus der vorherigen Formel folgt:
$$n_\mathrm{Si} = \frac{N}{V} = \frac{m \cdot N_\mathrm{A}}{M \cdot V}$$

                                      {{3}}
In dieser Formel können wir $\frac{m}{V}$ durch die Dichte $\varrho$ ersetzen:
$$n_\mathrm{Si} = \frac{\varrho \cdot N_\mathrm{A}}{M}$$

                                      {{4}}
Da Bor in Silizium ein Akzeptor ist, bezeichnen wir die gesuchte Dotierstoffkonzentration mit $n_\mathrm{A}$. Wenn eins von einer Million Si-Atome durch ein Bor-Atom ersetzt wird, folgt aus der vorherigen Formel:
$$n_\mathrm{A} = 10^{-6} \cdot n_\mathrm{Si} = 10^{-6} \cdot \frac{\varrho \cdot N_\mathrm{A}}{M}$$

                                      {{5}}
Einsetzen der gegebenen Werte liefert:
$$n_\mathrm{A} = 4,\!9 \cdot 10^{16}~\mathrm{cm^{-3}}$$


## Aufgabe 4 

> Ein Halbleiter hat eine Donator-Konzentration von $n_\mathrm{D} = 3,\!5 \cdot 10^{16}~\mathrm{cm^{-3}}$ und eine Akzeptor-Konzentration von $n_\mathrm{A} = 1,\!0 \cdot 10^{16}~\mathrm{cm^{-3}}$. Man berechne die Konzentration der Elektronen und Löcher ($n_i = 5,\!0 \cdot 10^{9}~\mathrm{cm^{-3}}$).

                                      {{1}}
Für den gegebenen Halbleiter überwiegt die Donator-Konzentration und wir betrachten zunächst die Elektronen.

                                      {{2}}
Bei Raumtemperatur sind in der Regel alle Donatoren ionisiert, d. h. die Elektronen der Donatoren wurden bereits komplett thermisch angeregt.

                                      {{3}}
Der größte Teil dieser Elektronen befindet sich nun im Leitungsband und bildet die frei beweglichen Elektronen.

                                      {{4}}
Der zweite Teil der über die Donatoren eingebrachten Elektronen besetzt aber die zusätzlich vorhandenen Akzeptor-Zustände. Für die Elektronenkonzentration folgt daraus:
$$n = n_\mathrm{D} - n_\mathrm{A} = 2,\!5 \cdot 10^{16}~\mathrm{cm^{-3}}$$

                                      {{5}}
Die Löcherkonzentration lässt sich aus dem Massenwirkungsgesetz bestimmen:
$$p = \frac{n_i^2}{n} = 1,\!0 \cdot 10^{3}~\mathrm{cm^{-3}}$$

                                      {{6}}
Demzufolge ist die Löcherkonzentration $p$ um 13 Größenordnungen geringer als die Elektronenkonzentration $n$.


## Aufgabe 5 

> Für Indiumantimonid ist die Bandlücke $E_\mathrm{g} = 0,\!23~\mathrm{eV}$, die Dielektrizitätskonstante $\varepsilon_r = 18$, die effektive Masse der Elektronen $m_\mathrm{e}^\mathrm{eff} = 0,\!015\,m_0$. Berechnen Sie:
>
> a) die Ionisierungsenergie der Donatoren!
>
> b) den Bahnradius für den Grundzustand!
>
> c) Ab welcher Donatorkonzentration treten deutliche Überlappungseffekte zwischen den Bahnen benachbarter Fremdatome auf? Diese Überlappung kann ein Störstellenband erzeugen. Dies ist ein Energieband, das die elektrische Leitung durch den Sprung-mechanismus (*Hopping*) ermöglicht, bei dem Elektronen von einem Fremdatom auf ein benachbartes, ionisiertes Fremdatom springen.


                                      {{1}}
**Direkte Halbleiter** (z. B. GaAs, GaN, InP) haben ein Leitungsbandminimum bei $k = 0$. Dort ist die effektive Masse isotrop, d. h. in allen Richtungen gleich:
$$m^\mathrm{eff} = m_x^\mathrm{eff} = m_y^\mathrm{eff} = m_z^\mathrm{eff}$$

                                      {{2}}
An diesem Punkt kann die Energie $E(k)$ durch eine isotrope Parabel mit nur einer Masse $m^\mathrm{eff}$ angenähert werden:
$$E(k) = \frac{\hbar^2 k^2}{2 m^\mathrm{eff}}$$

                                      {{3}}
************************************
**Indirekte Halbleiter** (z. B. Si, Ge, GaP) haben ein Leitungsbandminimum bei $k \neq 0$. Dort ist die effektive Masse richtungsabhängig. Man unterscheidet zwei effektive Massen:

- die longitudinale $m_l^\mathrm{eff}$ (entlang der $k$-Richtung)
- die transversale $m_t^\mathrm{eff}$ (senkrecht zu $k$)
************************************

                                      {{4}}
Die Energieparabel $E(k)$ hängt dann von zwei Massen ab, zum Beispiel:
$$E(k) = \frac{\hbar^2}{2} \left( \frac{k_x^2}{m_t^\mathrm{eff}} + \frac{k_y^2}{m_t^\mathrm{eff}} + \frac{k_z^2}{m_l^\mathrm{eff}} \right)$$


## Aufgabe 6 

> Wie lassen sich durch Messung der Temperaturabhängigkeit des Hall-Koeffizienten die Energielücke $E_\mathrm{g}$ eines Halbleiters sowie bei einem n-Typ-Halbleiter der Abstand $E_\mathrm{d}$ des Donatorniveaus von der Leitungsbandkante bzw. bei einem p-Typ-Halbleiter der Abstand $E_\mathrm{a}$ des Akzeptorniveaus von der Valenzbandkante bestimmen?

                                      {{1}}
![Qualitativer Verlauf der Bandstruktur von Si und Ge in der Nähe des Γ-Punktes](Bilder/Massen_Löcher.png "Qualitativer Verlauf der Bandstruktur von Si und Ge in der Nähe des Γ-Punktes. ∆ ist die Spin-Bahn-Aufspaltung. *Quelle: Rudolf Gross und Achim Marx, Vorlesungsskript Festkörperphysik, 2008*")

                                      {{2}}
Das Valenzband entsteht aus einem $p^3$-Orbital, d. h. die Drehimpulsquantenzahl beträgt $l=1$. Die Spin-Bahn-Kopplung $j = l \pm s$ (mit $s = \frac{1}{2}$) verursacht eine Energieaufspaltung um $\Delta$. 

                                      {{3}}
Die energetisch nach unten abgespaltenen Löcher besitzen den Gesamtdrehimpuls $j = l - s = \frac{1}{2}$ und die Masse $m_\mathrm{soh}^*$ (*split-off holes*).

                                      {{4}}
************************************
Die energetisch höher liegenden Löcher besitzen den Gesamtdrehimpuls $j = l + s = \frac{3}{2}$. Dieser Gesamtdrehimpuls ermöglich zwei unterschiedliche magnetische Quantenzahlen $m_j$:

- $m_j = \frac{3}{2}$ => schwere Löcher mit $m_\mathrm{hh}^*$ (*heavy holes*)
- $m_j = \frac{1}{2}$ => leichte Löcher mit $m_\mathrm{lh}^*$ (*light holes*)
************************************


## Aufgabe 7

> Lässt sich durch Messung des Hall-Effekts die Dichte $n_\mathrm{D}$ der Donatoren in einem n-Typ-Halbleiter bzw. die Dichte $n_\mathrm{A}$ der Akzeptoren in einem p-Typ-Halbleiter bestimmen? Wenn ja, in welchem Temperaturbereich muss die Messung stattfinden?

                                      {{1}}
Bei nicht zu hohen Temperaturen, also z. B. bei Raumtemperatur, sind das chemische Potential und die Fermi-Energie ungefähr gleich: $\mu \approx E_\mathrm{F}$.

                                      {{2}}
Für die Herleitung beginnen wir mit den Formeln für die Elektronenkonzentration $n$ und die Löcherkonzentration $p$:
$$n = 2 \left( \frac{m_\mathrm{e}^\mathrm{eff} k_\mathrm{B} T}{2 \pi \hbar^2} \right)^{3/2} \exp \left( - \frac{E_\mathrm{L} - E_\mathrm{F}}{k_\mathrm{B} T} \right)$$
$$p = 2 \left( \frac{m_\mathrm{h}^\mathrm{eff} k_\mathrm{B} T}{2 \pi \hbar^2} \right)^{3/2} \exp \left( \frac{E_\mathrm{V} - E_\mathrm{F}}{k_\mathrm{B} T} \right)$$

                                      {{3}}
Bei intrinsischen Halbleitern stammen alle Leitungselektronen aus dem Valenzband, so dass $n = p$ gilt:
$$2 \left( \frac{m_\mathrm{e}^\mathrm{eff} k_\mathrm{B} T}{2 \pi \hbar^2} \right)^{3/2} \exp \left( - \frac{E_\mathrm{L} - E_\mathrm{F}}{k_\mathrm{B} T} \right) = 2 \left( \frac{m_\mathrm{h}^\mathrm{eff} k_\mathrm{B} T}{2 \pi \hbar^2} \right)^{3/2} \exp \left( \frac{E_\mathrm{V} - E_\mathrm{F}}{k_\mathrm{B} T} \right)$$

                                      {{4}}
Kürzen und umstellen führt zu:
$$\left( m_\mathrm{e}^\mathrm{eff} \right)^{3/2} \exp \left( - \frac{E_\mathrm{L} - E_\mathrm{F}}{k_\mathrm{B} T} \right) = \left( m_\mathrm{h}^\mathrm{eff} \right)^{3/2} \exp \left( \frac{E_\mathrm{V} - E_\mathrm{F}}{k_\mathrm{B} T} \right)$$
$$\exp \left( \frac{-E_\mathrm{L} + 2 E_\mathrm{F} - E_\mathrm{V}}{k_\mathrm{B} T} \right) = \left( \frac{m_\mathrm{h}^\mathrm{eff}}{m_\mathrm{e}^\mathrm{eff}} \right)^{3/2}$$

                                      {{5}}
Weiter umformen:
$$\frac{-E_\mathrm{L} + 2 E_\mathrm{F} - E_\mathrm{V}}{k_\mathrm{B} T} = \ln \left[ \left( \frac{m_\mathrm{h}^\mathrm{eff}}{m_\mathrm{e}^\mathrm{eff}} \right)^{3/2} \right]$$
$$-E_\mathrm{L} + 2 E_\mathrm{F} - E_\mathrm{V} = \frac{3}{2} k_\mathrm{B} T \cdot \ln \left( \frac{m_\mathrm{h}^\mathrm{eff}}{m_\mathrm{e}^\mathrm{eff}} \right)$$

                                      {{6}}
Daraus folgt der gesuchte Zusammenhang (wobei $E_\mathrm{g} = E_\mathrm{L} + E_\mathrm{V}$):
$$E_\mathrm{F} = \frac{E_\mathrm{L} + E_\mathrm{V}}{2} + \frac{3}{4} k_\mathrm{B} T \cdot \ln \left( \frac{m_\mathrm{h}^\mathrm{eff}}{m_\mathrm{e}^\mathrm{eff}} \right)$$

                                      {{7}}
************************************
Das bedeutet:

- Bei $T = 0~\mathrm{K}$ liegt die Fermi-Energie genau in der Mitte der Bandlücke: $E_\mathrm{F} = \frac{E_\mathrm{g}}{2}$.
- Bei höheren Temperaturen verschiebt sich die Fermi-Energie leicht nach oben oder unten (je nach dem Verhältnis der effektiven Massen).
- Ist $m_\mathrm{h}^\mathrm{eff} > m_\mathrm{e}^\mathrm{eff}$ (z. B. GaAs), steigt die Fermi-Energie mit der Temperatur an.
- Ist $m_\mathrm{h}^\mathrm{eff} < m_\mathrm{e}^\mathrm{eff}$ (z. B. Si), nimmt die Fermi-Energie mit der Temperatur ab.
************************************

                                      {{8}}
************************************
**Beispiel für $m_\mathrm{h}^\mathrm{eff} < m_\mathrm{e}^\mathrm{eff}$:**

![Unterschiedliche effektive Massen von Elektronen und Löchern bedeuten verschiedene Bandkrümmungen von Leitungs- und Valenzband](Bilder/Fermienergie_Löchermassen.png "Unterschiedliche effektive Massen von Elektronen und Löchern bedeuten verschiedene Bandkrümmungen von Leitungs- und Valenzband. *Quelle: Hartmut Stöcker, [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/)*")
************************************

                                      {{9}}
Für $m_\mathrm{h}^\mathrm{eff} < m_\mathrm{e}^\mathrm{eff}$ ist das Valenzband stärker gekrümmt als das Leitungsband. Bei gleicher Ladungsträgerdichte ($n=p$) im intrinsischen Halbleiter muss sich die Fermi-Energie $E_\mathrm{F}$ leicht nach unten verschieben. Dies ist notwendig um die ungleiche Besetzung der Zustände richtig zu beschreiben. Diese Verschiebung steigt mit der Temperatur, da immer mehr Elektronen und Löcher entstehen und damit die Besetzung der Bänder zunimmt.