<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.0.1
language: de
narrator: Deutsch Female
comment:  Struktur der Materie 2 - Übung 05

@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md
import: https://github.com/liascript/CodeRunner
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 5


## Aufgabe 1

> Wir betrachten ein freies Elektronengas mit einer Dichte von $n=2,\!54 \cdot 10^{22}~\mathrm{cm}^{-3}$ (Natrium) und einem Volumen von $V = L_x L_y L_z = 1\cdot1\cdot1~\mathrm{cm}^3$.
>
> a) Berechnen Sie aus der Anzahl $N$ der Elektronen die Anzahl $Z_\mathrm{F}$ der im $k$-Raum besetzten Zustände, den Radius der Fermi-Kugel und die Anzahl $Z_0$ der in der Ebene $k_z=0$ von Elektronen besetzten Zustände.
>
> b) Wir legen nun ein Magnetfeld $B=1~\mathrm{T}$ in die $z$-Richtung an. Berechnen Sie die Anzahl der Kreise konstanter Energie $E(n, k_z=0)$, die sich innerhalb der ursprünglichen Grenzen der Fermi-Kugel befinden.
>
> c) Bestimmen Sie die Flussdichte $B_0$, bei welcher der innerste Landau-Zylinder $n=0$ die ursprüngliche Fermi-Kugel verlässt. Vergleichen Sie den Wert von $B_0$ mit technisch realisierbaren Magnetfeldern.

                                      {{1}}
**a)** Dichte der Zustände im $k$-Raum: $z(k) = V/(2 \pi)^3$

                                      {{2}}
Zahl der Elektronen: $N = n \cdot V = 2,\!54 \cdot 10^{22}$

                                      {{3}}
Zahl der besetzten Zustände in der Fermi-Kugel (jeweils 2 Spinzustände): $Z_\mathrm{F} = N/2 = 1,\!27 \cdot 10^{22}$

                                      {{4}}
Die Zahl der Zustände in der Fermi-Kugel ergibt sich aber auch aus der Zustandsdichte im $k$-Raum multipliziert mit dem Volumen der Fermi-Kugel mit dem Radius $k_\mathrm{F}$:
$$Z_\mathrm{F} = z(k) \cdot \frac{4}{3} \pi k_\mathrm{F}^3 = \frac{V}{(2 \pi)^3} \cdot \frac{4}{3} \pi k_\mathrm{F}^3 = \frac{V}{6 \pi^2} \cdot k_\mathrm{F}^3 = \frac{N}{2} = \frac{n V}{2}$$

                                      {{5}}
Für die Fermi-Wellenzahl folgt: $k_\mathrm{F} = (3 \pi^2 n)^{1/3} = 9,\!1 \cdot 10^7~\mathrm{cm^{-1}}$

                                      {{6}}
$Z_0$ ist die Anzahl der Zustände in der Ebene $k_z=0$, d. h. in einem dünnen Kreiszylinder mit der Dicke $2 \pi/L_z$:
$$Z_0 = z(k) \cdot \pi k_\mathrm{F}^2 \cdot \frac{2 \pi}{L_z} = \frac{V}{(2 \pi)^3} \cdot \pi k_\mathrm{F}^2 \cdot \frac{2 \pi}{L_z} = \frac{L_x L_y}{4 \pi} \cdot k_\mathrm{F}^2 = 6,\!58 \cdot 10^{14}$$

                                      {{7}}
**b)** Während nach den Gesetzen der klassischen Physik ein Teilchen jede beliebige transversale Energie annehmen kann, ist dies in der Quantenmechanik nicht möglich, sondern die Energie ist quantisiert, das heißt, die transversale Energie kann nur diskrete, durch eine natürliche Zahl $n$ charakterisierte Werte annehmen. Die Landau-Niveaus (nach Lew Dawidowitsch Landau) sind in der Quantenmechanik die Niveaus der transversalen Energie eines geladenen Teilchens, das sich in einem homogenen Magnetfeld $B$ bewegt. Diese Aufspaltung in Landau-Niveaus lässt sich zum Beispiel durch den De-Haas-van-Alphen-Effekt messen. In Bezug auf die longitudinale Bewegung in Richtung des Magnetfeldes $B$ ist die Energie auch nach der quantenmechanischen Behandlung nicht quantisiert und identisch zur klassischen Herangehensweise. 

                                      {{8}}
Im zweidimensionalen, transversalen Impulsraum bilden die Landau-Niveaus Kreise; im dreidimensionalen Impulsraum die Landau-Zylinder. Sie besitzen folgende Energiewerte:
$$E_n = \hbar \omega_c \left(n + \frac{1}{2} \right)$$

                                      {{9}}
Dabei ist $\omega_c = \frac{eB}{m_e}$ die Zyklotronfrequenz, also die Winkelgeschwindigkeit beim Umlauf des Elektrons im Magnetfeld.

                                      {{10}}
In einem Festkörper sind die transversalen Impulse $k_\perp$ zusätzlich aufgrund des Kristallgitters gequantelt:
$$E_n = \frac{\hbar^2 k_\perp^2}{2 m_e}$$

                                      {{11}}
Der maximal mögliche transversale Impuls innerhalb der Fermi-Kugel ist durch die Fermi-Wellenzahl $k_\mathrm{F}$ gegeben. Gleichsetzen der Energie-Formeln und Umstellen nach $n$ ergibt die Anzahl der Kreise:
$$n = \frac{\hbar k_\mathrm{F}^2}{2 e B} - \frac{1}{2} = 27196$$

                                      {{12}}
**c)** Damit bereits bei $n=0$ der transversale Impuls $k_\perp$ die Fermi-Kugel berührt, muss das Magnetfeld deutlich größer als zuvor sein. Den erforderlichen Wert für $B$ erhält man durch Einsetzen von $n=0$ in die letzte Formel:
$$0 = \frac{\hbar k_\mathrm{F}^2}{2 e B} - \frac{1}{2} \ \Rightarrow \ B = \frac{\hbar k_\mathrm{F}^2}{e} = 54400~\mathrm{T}$$

                                      {{13}}
***********************************
Zum Vergleich:

| Quelle des Magnetfeldes      | Magnetfeld                      |
|---------------|---------------------------------|
| Erdmagnetfeld | $30...60~\mathrm{µ T}$          |
| Kühlschrankmagnet | $1...10~\mathrm{m T}$          |
| Lautsprechermagnet | $1...2~\mathrm{T}$          |
| NMR-Gerät in der Medizin | $2...12~\mathrm{T}$          |
| Supraleitende Magnete in Messgeräten | $7...32~\mathrm{T}$          |
| Rekord für kontinuierliches Magnetfeld | $45,\!5~\mathrm{T}$          |
| Rekord für gepulstes Magnetfeld | $2800~\mathrm{T}$          |
************************************


## Aufgabe 2 

> Beschreiben Sie quantitativ den paramagnetischen Anteil der magnetischen Suszeptibilität eines freien Elektronengases in einem Metall. Wie groß ist dieser Anteil an der gesamten magnetischen Suszeptibilität?

                                      {{1}}
**Einfache Überlegung:** Zur Suszeptibilität tragen nicht alle Elektronen bei, sondern nur der Anteil in der Nähe der Fermie-Energie, der mit $T/T_\mathrm{F}$ abgeschätzt wird ($k_\mathrm{B} T_\mathrm{F} = E_\mathrm{F}$). Wir nutzen das Ergebnis von Übung 4, Aufgabe 4 und multiplizieren mit $T/T_\mathrm{F}$:
$$\chi = \mu_0 \frac{M}{B_0} \approx \frac{\mu_0 n \mu_\mathrm{eff}^2}{k_\mathrm{B} T} \cdot \frac{T}{T_\mathrm{F}}$$

                                      {{2}}
Für Elektronen mit $L = 0$ und $S = ½$ ist $\mu_\mathrm{eff} = ½ g_S \mu_\mathrm{B} \cong \mu_\mathrm{B}$, da $g_S \cong 2$. Damit erhalten wir:
$$\chi \approx \frac{n \mu_0 \mu_\mathrm{B}^2}{k_\mathrm{B} T_\mathrm{F}} = \frac{n \mu_0 \mu_\mathrm{B}^2}{E_\mathrm{F}}$$

                                      {{3}}
************************************
** Genauere Betrachtung:** Das äußere Magnetfeld bewirkt, dass sich die Zustandsdichtefunktionen der Elektronen mit Spin parallel bzw. antiparallel zum Magnetfeld um jeweils den Betrag $\mu_\mathrm{B} B$ gegenüber ihrer ursprünglichen Lage verschieben.

![Verschiebung der Zustandsdichtefunktionen der Elektronen mit Spin parallel bzw. antiparallel zum Magnetfeld](Bilder/Spin-Niveaus.png "Verschiebung der Zustandsdichtefunktionen der Elektronen mit Spin parallel bzw. antiparallel zum Magnetfeld *Quelle: Hartmut Stöcker, [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/)*")<!-- style = "width: 300px;" -->
************************************

                                      {{4}}
Für die jeweilige Anzahl der Zustände erhalten wir:
$$N^+ = \frac{1}{2} \int_{-\mu_\mathrm{B}}^{E_\mathrm{F}} f(E) \cdot D(E + \mu_\mathrm{B} B) \, \mathrm{d}E \approx \frac{1}{2} \int_0^{E_\mathrm{F}} f(E) \cdot D(E) \, \mathrm{d}E + \frac{1}{2} \mu_\mathrm{B} B D(E_\mathrm{F})$$
$$N^- = \frac{1}{2} \int_{+\mu_\mathrm{B}}^{E_\mathrm{F}} f(E) \cdot D(E - \mu_\mathrm{B} B) \, \mathrm{d}E \approx \frac{1}{2} \int_0^{E_\mathrm{F}} f(E) \cdot D(E) \, \mathrm{d}E - \frac{1}{2} \mu_\mathrm{B} B D(E_\mathrm{F})$$

                                      {{5}}
Daraus folgt die Magnetisierung:
$$M = \mu_\mathrm{B} \cdot (N^+ - N^-) = \mu_\mathrm{B} \cdot \mu_\mathrm{B} B D(E_\mathrm{F})$$

                                      {{6}}
Für die Zustandsdichte bei der Fermi-Energie nutzen wir die Formel $D(E_\mathrm{F}) = \frac{3 n}{2 E_\mathrm{F}}$, die aus *Struktur der Materie 1* bekannt ist. Damit folgt:
$$M = \mu_\mathrm{B}^2 B \frac{3 n}{2 E_\mathrm{F}}$$

                                      {{7}}
Der paramagnetische Anteil der magnetischen Suszeptibilität eines freien Elektronengases (Pauli-Spinsuszeptibilität) ist also:
$$\chi_\mathrm{para} = \mu_0 \frac{M}{B} = \frac{3}{2} \mu_0 \mu_\mathrm{B}^2 \frac{n}{E_\mathrm{F}}$$

                                      {{8}}
Ohne Herleitung: Der zusätzliche diamagnetische Beitrag durch die Elektronenbewegung (Landau-Spinsuszeptibilität) beträgt:
$$\chi_\mathrm{dia} = - \frac{1}{3} \chi_\mathrm{para} = - \frac{1}{2} \mu_0 \mu_\mathrm{B}^2 \frac{n}{E_\mathrm{F}}$$

                                      {{9}}
Für die gesamte magnetische Suszeptibilität erhalten wir:
$$\chi = \mu_0 \mu_\mathrm{B}^2 \frac{n}{E_\mathrm{F}}$$


## Aufgabe 3

> Die Fermi-Energie von Kupfer beträgt $E_\mathrm{F} = 7,\!00~\mathrm{eV}$. Berechnen Sie den Beitrag des Elektronengases zur molaren magnetischen Suszeptibilität von Kupfer in der Näherung freier Elektronen. Außer diesem Beitrag trägt auch noch der diamagnetische Anteil der abgeschlossenen Elektronenschalen der Ionenrümpfe (Cu^+^) von $-15 \cdot {10}^{-11}~\mathrm{m^3/mol}$ zum Gesamtwert bei. Vergleichen Sie das Ergebnis mit dem experimentell bestimmten Messwert von $\chi_\mathrm{mol} = -6,\!9\cdot{10}^{-11}~\mathrm{m^3/mol}$.

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

> Wandeln Sie den experimentellen Messwert von Kupfer auch in die entsprechenden Werte für die Massensuszeptibilität und Volumensuszeptibilität um (Dichte $\varrho = 8,\!93~\mathrm{g/cm^3}$, molare Masse $M = 63,\!5~\mathrm{g/mol}$).

                                      {{1}}
Der Messwert beträgt $\chi_\mathrm{mol} = -6,\!9\cdot{10}^{-11}~\mathrm{m^3/mol}$ und rechnet sich wie folgt in eine Volumensuszeptibilität (ohne Einheit) um:
$$\chi_V = \frac{\varrho}{M} \chi_\mathrm{mol} = -9,\!71 \cdot 10^{-6}$$

                                      {{2}}
Die Massensuszeptibilität $\chi_\mathrm{g}$ ergibt sich folgendermaßen:
$$\chi_\mathrm{g} = \frac{1}{\varrho} \chi_V = \frac{1}{M} \chi_\mathrm{mol} = -1,\!09 \cdot 10^{-6}~\mathrm{cm^3/g}$$



## Aufgabe 5 

> Berechnen Sie für die Übergangsmetallionen Ti^2+^, Cr^3+^, Fe^3+^ und Cu^2+^ den Landéfaktor und das effektive magnetische Moment und vergleichen Sie diese Werte mit dem Experiment. Wie fällt der Vergleich aus, wenn reiner Spinmagnetismus ($g=2$) angenommen wird?

                                      {{1}}
***********************************
Alle genannten Elemente gehören zu den Übergangsmetallen der 4. Periode und haben damit eine abgeschlossene Argon-Konfiguration, zwei Elektronen im Zustand $\mathrm{4s}$ sowie unterschiedlich viele $\mathrm{3d}$-Elektronen. 

![Periodensystem der Elemente](Bilder/Periodensystem-der-elemente_1280x720.png "Periodensystem der Elemente. *Quelle: https://www.joqora.de/blog/das-periodensystem-der-elemente *") <!-- style = "width: 600px;" -->
************************************

                                      {{2}}
************************************
Bei den $\mathrm{3d}$-Übergangsmetallen werden durch Ionisation zunächst die $\mathrm{4s}$-Elektronen entfernt. Wir bestimmen nun die Quantenzahlen und gehen dabei wie in Übung 4, Aufgabe 2 vor:

<!-- data-type="none" -->
| Ion    | Konfiguration                      | Kästchenschema | $S$ | $L$ | $J$ | Termsymbol |
|--------|------------------------------------|----------------|-----|-----|-----|------------|
| Ti^2+^ | $\mathrm{[Ar] \, 3d^2}$    | $\fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{\phantom{↑↓}} \fbox{\phantom{↑↓}} \fbox{\phantom{↑↓}}$ | $1$ | $3$ | $2$ | $\mathrm{^3F_2}$ |
| Cr^3+^ | $\mathrm{[Ar] \, 3d^3}$    | $\fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{\phantom{↑↓}} \fbox{\phantom{↑↓}}$ | $\frac{3}{2}$ | $3$ | $\frac{3}{2}$ | $\mathrm{^4F_{3/2}}$ |
| Fe^3+^ | $\mathrm{[Ar] \, 3d^5}$    | $\fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}}$ | $\frac{5}{2}$ | $0$ | $\frac{5}{2}$ | $\mathrm{^6S_{5/2}}$ |
| Cu^2+^ | $\mathrm{[Ar] \, 3d^9}$    | $\fbox{↑↓} \fbox{↑↓} \fbox{↑↓} \fbox{↑↓} \fbox{↑\phantom{↓}}$ | $\frac{1}{2}$ | $2$ | $\frac{5}{2}$ | $\mathrm{^2D_{5/2}}$ |
************************************

                                      {{3}}
Der Landé-Faktor $g$ folgt aus:
$$g = 1+\frac{J(J+1)+S(S+1)-L(L+1)}{2J(J+1)}$$

                                      {{4}}
Das effektive magnetische Moment ist dann:
$$\mu_\mathrm{eff} = g \cdot \sqrt{J(J+1)} \cdot \mu_\mathrm{B}$$

                                      {{5}}
Für ein reines Spinsystem ($g=2$) gilt:
$$\mu_{\mathrm{eff},S} = 2 \cdot \sqrt{S(S+1)} \cdot \mu_\mathrm{B}$$

                                      {{6}}
************************************
Übersicht der berechneten Werte und Vergleich mit experimentellen Werten (*Quelle: Rudolf Gross und Achim Marx, Vorlesungsskript Festkörperphysik, 2008*):

<!-- data-type="none" -->
| Ion    | Landé-Faktor  | $\mu_\mathrm{eff}/\mu_\mathrm{B}$ (Theorie) | $\mu_{\mathrm{eff},S}/\mu_\mathrm{B}$ (Theorie) | $\mu_\mathrm{eff}/\mu_\mathrm{B}$ (Experiment)  |
|--------|---------------|----------|----------|---------|
| Ti^2+^ | $\frac{2}{3}$ | $1,\!63$ | $2,\!83$ | $2,\!8$ |
| Cr^3+^ | $\frac{2}{5}$ | $0,\!77$ | $3,\!87$ | $3,\!8$ |
| Fe^3+^ | $2$           | $5,\!92$ | $5,\!92$ | $5,\!9$ |
| Cu^2+^ | $\frac{6}{5}$ | $3,\!55$ | $1,\!73$ | $1,\!9$ |
************************************