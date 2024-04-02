<!--
author:   Hartmut Stöcker

email:    hartmut.stoecker@physik.tu-freiberg.de

version:  0.0.1

language: de

narrator: Deutsch Female

comment:  Struktur der Materie 2 - Übung 01
@style
.lia-toc__bottom {
    display: none;
}
@end



import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md

import: https://github.com/liascript/CodeRunner

import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 1


## Aufgabe 1

> Die Energielücke zwischen Valenz- und Leitungsband liegt in der Größenordnung von $\mathrm{1~eV}$. Wie stark muss ein von außen angelegtes elektrisches Feld sein, um einen Elektronenübergang vom Valenz- zum Leitungsband zu erzeugen? Nehmen Sie eine mittlere Elektronengeschwindigkeit von $\mathrm{10^6~m/s}$ und eine Relaxationszeit von $\mathrm{10^{-14}~s}$ an.

                                      {{1}}
Ein elektrisches Feld führt zur Verkippung der Bänder (allgemein gültig, nicht nur bei Halbleitern).

                                      {{2}}
Kann das Elektron ausreichend weit springen, kann es die Bandlücke $E_\mathrm{g}$ zwischen Valenzband und Leitungsband überwinden.

                                      {{3}}
![Energieschema eines Halbleiters über dem Ort mit angelegtem elektrischen Feld](Bilder/Elektrisches_Feld_Valenzband_Leitungsband.png "Energieschema eines Halbleiters über dem Ort mit angelegtem elektrischen Feld. Das Elektron (blauer Kreis) bewegt sich vom Valenzband zum Leitungsband. *Quelle: Hartmut Stöcker, [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/)*")

                                      {{4}}
Die Sprungweite $s$ ergibt sich aus Geschwindigkeit $v$ und Relaxationszeit $t$ (Lebensdauer):
$$s = v \cdot t = \mathrm{10^6~\frac{m}{s}} \cdot \mathrm{10^{-14}~s} = \mathrm{10^{-8}~m}$$

                                      {{5}}
Die Bandlücke $E_\mathrm{g} = \mathrm{1~eV}$ entspricht für das Elektron einer Potentialbarriere von $U = \mathrm{1~V}$.

                                      {{6}}
Für das elektrische Feld $E$ folgt:
$$E = \frac{U}{s} = \frac{\mathrm{1~V}}{\mathrm{10^{-8}~m}} = \mathrm{10^8~\frac{V}{m}} = \mathrm{10^5~\frac{V}{mm}} = \mathrm{100~\frac{kV}{mm}}$$

## Aufgabe 2 

> Zeichnen Sie schematisch die Bandstruktur $E(k)$ für einen direkten und einen indirekten Halbleiter. Wo befindet sich das Fermi-Niveau $E_\mathrm{F}$ bei Raumtemperatur für einen intrinsischen, Donator- oder Akzeptor-dotierten Halbleiter?

                                      {{1}}
**Bandstruktur direkter Halbleiter:**
![Bandstrukturen für zwei direkte Halbleiter](Bilder/Bandschema_direkte_Halbleiter.png "Bandstrukturen $E(k)$ für zwei direkte Halbleiter. Das Valenzbandmaximum und das Leitungsbandminimum liegen genau beim gleichen $k$-Wert. *Quelle: Helmut Föll, [Matwiss II](https://www.tf.uni-kiel.de/matwis/amat/mw2_ge/kap_4/backbone/r4_3_2.html)*")

                                      {{2}}
**Bandstruktur indirekter Halbleiter:**
![Bandstrukturen für zwei indirekte Halbleiter](Bilder/Bandschema_indirekte_Halbleiter.png "Bandstrukturen $E(k)$ für zwei indirekte Halbleiter. Das Valenzbandmaximum und das Leitungsbandminimum befinden sich bei unterschiedlichen $k$-Werten. *Quelle: Helmut Föll, [Matwiss II](https://www.tf.uni-kiel.de/matwis/amat/mw2_ge/kap_4/backbone/r4_3_2.html)*")

                                      {{3}}
**Fermi-Niveau intrinsischer Halbleiter:**
![Fermi-Niveau für einen intrinsischen Halbleiter](Bilder/Ferminiveau_Raumtemperatur_intrinsisch.png "Das Fermi-Niveau $E_\mathrm{F}$ für einen intrinsischen Halbleiter liegt ungefähr in der Mitte der Bandlücke. *Quelle: Hartmut Stöcker, [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/)*") 

                                      {{4}}
**Fermi-Niveau Donator-dotierter Halbleiter:**
![Fermi-Niveau für einen Donator-dotierten Halbleiter](Bilder/Ferminiveau_Raumtemperatur_Donator.png "Das Fermi-Niveau $E_\mathrm{F}$ für einen Donator-dotierten Halbleiter liegt ungefähr beim Donator-Niveau $E_\mathrm{D}$. *Quelle: Hartmut Stöcker, [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/)*") 

                                      {{5}}
**Fermi-Niveau Akzeptor-dotierter Halbleiter:**
![Fermi-Niveau für einen Akzeptor-dotierten Halbleiter](Bilder/Ferminiveau_Raumtemperatur_Akzeptor.png "Das Fermi-Niveau $E_\mathrm{F}$ für einen Akzeptor-dotierten Halbleiter liegt ungefähr beim Akzeptor-Niveau $E_\mathrm{A}$. *Quelle: Hartmut Stöcker, [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/)*")


## Aufgabe 3
                                      {{0}}
> __3.__ Wie groß ist die Zustandsdichte eines dreidimensionalen freien Elektronengases im reziproken Raum ($D(k)$) und  im realen Raum ($D(E)$)?


                                      {{1}}



**Lösung Aufgabe 3:**

                                      {{2}}
Es gilt wieder:
$$\int_{k(E)}^{k(E+\Delta E)} D(k)dk^3=\int_{E}^{E+\Delta E}D(E)dE$$

                                      {{3}}
Die periodischen Randbedingungen für die ebenen Wellen (Knotenpunkte am Kristallrand) bedingen wieder (wie bei den Phononen) eine Quantelung der erlaubten Zustände (Wellenvektoren). Das Volumen pro Zustand im 3D-Impulsraum ist $\frac{(2\pi)^3}{V}$. Da jeder $k$-Wellenvektor von 2 Elektronen mit entgegengesetztem Spin besetzt werden kann, ist die Zustandsdichte im Impulsraum damit 

                                      {{4}}
$$D(k)=2\cdot \frac{V}{(2\pi)^3}$$

                                      {{5}}
Damit kann die linke Seite der obigen Gleichung umgestellt werden:
$$\int_{k(E)}^{k(E+\Delta E)} D(k)dk^3=\int_{k(E)}^{k(E+\Delta E)} 2\cdot \frac{V}{(2\pi)^3}dk^3=2\cdot \frac{V}{(2\pi)^3}\int_{k(E)}^{k(E+\Delta E)} dk^3$$

                                      {{6}}
Die Flächen konstanter Energie im $k$-Raum sind wegen der Dispersionsrelation $E(k)=\frac{\hbar^2 k^2}{2m}$ Kugeloberflächen. $\Delta k$ sei die zu $\Delta E$ gehörige Änderung des Wellenvektors.  
Für einen dreidimensionalen Festkörper erhalten wir für den Ausruck 

                                      {{7}}
$$2\cdot \frac{V}{(2\pi)^3}\int_{k(E)}^{k(E+\Delta E)} dk^3=2\cdot \frac{V}{(2\pi)^3} \cdot \overbrace{4\pi k^2 \Delta k}^\text{Volumen von Kugelschale im k-Raum}$$

                                      {{8}}
Damit ergibt sich mit für $\Delta k$ insgesamt: 
$$2\cdot \frac{V}{(2\pi)^3} \cdot 4\pi k^2 \Delta k=D(E)\Delta E$$

                                      {{9}}
Und damit 
$$D(E)=2\cdot \frac{V}{(2\pi)^3} \cdot 4\pi k^2\frac{ \Delta k}{\Delta E}$$
Aus der bekannten Dispersionsrelation $E=\frac{\hbar^2 k^2}{2m}$ für freie Elektonen ergibt sich:

                                      {{10}}
$$k=\sqrt{\frac{2mE}{\hbar^2}}$$

                                      {{11}}
Für die Ableitung gilt damit:
$$\frac{dk}{dE}=\sqrt{\frac{2m}{\hbar^2}}\cdot \frac{1}{2}\cdot E^{-\frac{1}{2}}$$

                                      {{12}}
Damit gilt für $D(E)$:
$$\begin{align*}D(E)&=2\cdot \frac{V}{(2\pi)^3} \cdot 4\pi k^2\sqrt{\frac{2m}{\hbar^2}}\cdot \frac{1}{2}\cdot E^{-\frac{1}{2}}\\
&=2\cdot \frac{V}{(2\pi)^3} \cdot 4\pi \frac{2mE}{\hbar^2}\sqrt{\frac{2m}{\hbar^2}}\cdot \frac{1}{2}\cdot E^{-\frac{1}{2}}\\
&=\frac{V}{2\pi^2} \bigg(\frac{2m}{\hbar^2}\bigg)^{\frac{3}{2}}E^{\frac{1}{2}}\end{align*}$$





## Aufgabe 4 
                                      {{0}}
> __4.__ Zeigen Sie, dass die mittlere (kinetische) Energie von freien Elektronen in einem dreidimensionalen Elektronengas aus $N$ Elektronen bei $T=0\,\mathrm{K}$ gleich $\overline{E}=\frac{3}{5}E_\mathrm{F}$ ist.



                                      {{1}}
**Lösung Aufgabe 4:**

                                      {{2}}

Die Elektronen befolgen auf Grund ihres halbzahligen Spins die Fermi-Dirac-Statistic mit der Verteilungsfunktion

                                      {{2}}
$$f(E,T)=\frac{1}{e^{(E-E_\mathrm{F})/k_\mathrm{B}T}+1}$$



                                      {{3}}
Die Gesamtenergie der Elektronen ist gegeben durch
$$E_\mathrm{ges}=\int_0^{\infin}E\cdot D(E)\cdot f(E,T)\cdot dE $$

                                      {{4}}
Die mittlere Energie pro Elekron läßt sich berechnen zu:
$$\begin{align*}\overline{E}&=\frac{E_\mathrm{ges}}{N}\\
&=\frac{\int_0^{\infin}E\cdot D(E)\cdot f(E,T)\cdot dE}{\int_0^{\infin} D(E)\cdot f(E,T)\cdot dE}\\
\end{align*}$$

                                      {{5}}
Jetzt können die Zustandsdichte $D(E)$ (siehe Aufgabe 3) und die Verteilungsfunktion $f(E,T)$ eingesetzt werden:

                                      {{6}}
$$\begin{align*}\overline{E}
&=\frac{\int_0^{\infin}E\cdot \frac{V}{2\pi^2} \bigg(\frac{2m}{\hbar^2}\bigg)^{\frac{3}{2}}E^{\frac{1}{2}}\cdot \frac{1}{e^{(E-E_\mathrm{F})/k_\mathrm{B}T}+1}\cdot dE}{\int_0^{\infin} \frac{V}{2\pi^2} \bigg(\frac{2m}{\hbar^2}\bigg)^{\frac{3}{2}}E^{\frac{1}{2}}\cdot \frac{1}{e^{(E-E_\mathrm{F})/k_\mathrm{B}T}+1}\cdot dE}\\
\end{align*}$$

{{7}}       
Für $T=0\,\mathrm{K}$ ist die Verteilungsfunktion eine Stufenfunktion mit Sprung bei $E_\mathrm{F}$, unterhalb von $E_\mathrm{F}$ ist der Wert 1, oberhalb Null.
$$\begin{align*}
\overline{E}
&=\frac{\int_0^{E_\mathrm{F}}E^{\frac{3}{2}}dE}{\int_0^{E_\mathrm{F}}E^{\frac{1}{2}}dE}\\
&=\frac{\frac{2}{5}E_\mathrm{F}^{\frac{5}{2}}}{\frac{2}{3}E_\mathrm{F}^{\frac{3}{2}}}\\
&=\frac{3}{5}E_\mathrm{F}
\end{align*}$$

## Aufgabe 5 

                                      {{0}}
> __5.__ Zeigen Sie, dass ein Fermi-Gas mit der Fermi-Energie $E_\mathrm{F}$ auch am Temperaturnullpunkt einen Fermi-Druck besitzt. Vergleichen Sie das Ergebnis mit dem eines klassischen idealen Gases.

                                      {{1}}
**Lösung Aufgabe 5:**

                                      {{2}}
Die innere Energie $U$ eines Fermigases bei $T=0\, \mathrm{K}$ ist (siehe Aufgabe 4)
$$U=N\cdot \overline{E}=N\cdot \frac{3}{5}E_\mathrm{F}$$

                                       {{3}}
Mit der Fermienergie $E_\mathrm{F}=\frac{\hbar^2}{2m_\mathrm{e}}\big(3\pi^2\frac{N}{V}\big)^{\frac{2}{3}}$ ergibt sich:

                                      {{4}}
$$U=N\cdot \frac{3}{5}E_\mathrm{F}=N\cdot \frac{3}{5}\frac{\hbar^2}{2m_\mathrm{e}}\bigg(3\pi^2 \frac{N}{V}\bigg)^{\frac{2}{3}}$$

                                      {{5}}
Der Druck ist definiert als $p=-\frac{\partial U}{\partial V}$, also gilt

                                      {{6}}
$$\begin{align*}
p&=-\frac{\partial U}{\partial V}\\
&=-\frac{\partial }{\partial V}\bigg(N\cdot \frac{3}{5}\frac{\hbar^2}{2m_\mathrm{e}}\bigg(3\pi^2 \frac{N}{V}\bigg)^{\frac{2}{3}}\bigg)\\
&=N\cdot \frac{3}{5}\frac{\hbar^2(3\pi^2N)^{\frac{2}{3}}}{2m_\mathrm{e}}\cdot (-\frac{2}{3})V^{-\frac{5}{3}}\\
&=N\cdot V^{-1}\cdot \frac{2}{5}\frac{\hbar^2}{2m_\mathrm{e}}\cdot (\frac{3\pi^2N}{V})^{\frac{2}{3}}\\
&=\frac{2}{5}\frac{N}{V}\cdot E_\mathrm{F}
\end{align*}$$

                                      {{7}}
Der Fermi-Druck ist nicht von der Temperatur abhängig und auch bei $T=0\, \mathrm{K}$ vorhanden. Ein klassisches ideales Gas mit $N$ Teilchen hat den Druck 

                                      {{8}}
$$p_\mathrm{Gas}=N\cdot k_\mathrm{B} \frac{T}{V}$$
## Aufgabe 6 

                                      {{0}}
> __6.__ Konstruieren Sie die ersten drei Brillouin-Zonen eines ebenen quadratischen Gitters.

![quadratisches Gitter](media/quadratisches_Gitter.png)

                                      {{1}}
**Lösung Aufgabe 6:**
![Abbildung der erste, zweiten und dritten Brioullin-Zone eines ebenen quadratischen Gitters](media/quadratisches_Gitter_BZ.png "*Erste (gelb), zweite (grün) und dritte (rot) Brillouinzone eines ebenen quadratischen Gitters; Quelle:  Claudia Funke licensed under [CC BY-NC-SA ](https://creativecommons.org/licenses/by-nc-sa/4.0/)*")


## Aufgabe 7

                                      {{0}}
>__7.__ Betrachten Sie ein einfaches ebenes quadratisches Gitter in zwei Dimensionen. Zeigen Sie, dass die kinetische Energie eines freien Elektrons an einer Ecke der ersten Brillouin-Zone doppelt so groß ist wie die eines Elektrons im Mittelpunkt einer Seitenfläche der Zone.

                                      {{1}}
**Lösung Aufgabe 7:**

                                      {{2}}
Die Energie eines freien Elektrons ist 
$$E(K)=\frac{\hbar^2k^2}{2m}$$

                                      {{2}}
![Abbildung reziprokes quadratisches Gitter](media/quadr_Gitter_beschriftet.png "*Wellenvektoren in der ersten Brillouinzone eines ebenen quadratischen Gitters; Quelle:  Claudia Funke licensed under [CC BY-NC-SA ](https://creativecommons.org/licenses/by-nc-sa/4.0/)*" )

                                      {{3}}
Für die Wellenvektoren in der Ecke der ersten Brillouinzone gilt:
$$k_\mathrm{Ecke}=\sqrt{2}k_\mathrm{Mitte}$$

                                      {{4}}
$$\Rightarrow E_\mathrm{Ecke}=2\cdot E_\mathrm{Mitte}$$

## Aufgabe 8

                                      {{0}}
>__8.__ Wie groß ist das Verhältnis  der kinetischen Energien eines freien Elektrons an einer Ecke der ersten Brillouin-Zone zu der eines Elektrons im Mittelpunkt einer Seitenfläche der Zone im einfachen dreidimensionalen kubischen Gitter?

                                      {{1}}
**Lösung Aufgabe 8**

                                      {{2}}
Die 1. Brillouin- Zone eines sc-Gitters im 3D mit Gitterkonstante $a$ ist ein Würfel mit der Kantenlänge $\frac{2\pi}{a}$

                                      {{3}}
Die [Raumdiagonale vom Würfel](https://www.matheretter.de/wiki/wurfel-raumdiagonale) errechnet sich mit Hilfe vom Satz des Pythagoras, wobei die Raumdiagonale durch eine Flächendiagonale und eine Kantenlänge aufgespannt wird. 
Die Raumdiagonale im Impulsraum hat damit die Länge

                                      {{4}}
$$\sqrt{3}\cdot \frac{\pi}{a}$$

                                      {{5}}
Damit gilt für die Energie in der Ecke des 3D-Würfels ([111]-Richtung) im Verhältnis fur Energie in [100]-Richtung:

                                      {{6}}
$$E_{[111]} = 3 \cdot E_{[100]}$$

## Aufgabe 9

                                      {{0}}
>__9.__ Warum tragen nicht alle Leitungselektronen im Metall mit $\frac{1}{2}k_\mathrm{B}$ pro Freiheitsgrad zur spezifischen Wärme bei?

                                      {{1}}
**Lösung Aufgabe 9**

                                      {{2}}
![freie Elektronen: Zustandsdichte mal Fermiverteilung](https://www.tf.uni-kiel.de/matwis/amat/mw2_ge/kap_2/illustr/waermekapazitaet1.png "*Freie Elektronen: Zustandsdichte mal Fermiverteilung (rot); Quelle [H. Föll (MaWi 2 Skript), Uni Kiel](https://www.tf.uni-kiel.de/matwis/amat/mw2_ge/kap_2/backbone/r2_4_1.html)*")

                                      {{3}}
Im Modell des freien Elektronengases sitzen die meisten der Elektronen auf vollbesetzten Zuständen oder anders ausgedrückt, auf Plätzen im $k$-Raum, bei denen alle Nachbarplätze besetzt sind.  Wegen des Pauli-Prinzips können nur solche Elektronen thermisch angeregt werden, die sich in einem Energiebereich von der Größenordnung $\frac{1}{2}k_\mathrm{B}\cdot T$ in der Nähe der Fermienergie $E_\mathrm{F}$ befinden, denn nur dort sind leere Zustände in der Nähe, in die sie angeregt werden können. Nur Elektronen in dem oben gelb markierten Gebiet (Breite ca. $\frac{1}{2}k_\mathrm{B}\cdot T$ ) können also angeregt werden 


## Aufgabe 10

                                      {{0}}
>__10.__ Was beschreiben die Sommerfeld- Parameter?


                                      {{1}}
**Lösung Aufgabe 10**

                                      {{2}}
Für die spezifische Wärme von Metallen gilt bei tiefen Temperaturen:
$$C_p = \underbrace{\gamma \cdot T}_\text{elektronischer Anteil} + \underbrace{A\cdot T^3}_\text{Phononenanteil}$$

                                      {{3}}
In der Darstellung $\frac{C}{T}$ über $T^2$ ergibt sich dann eine Gerade. Der Schnittpunkt dieser Gerade mit der $y$-Achse ist der Sommerfeld-Koeffizient $\gamma$.

{{4}}
![Spezifische Wärme von Kalium bei tiefen Temperaturen](media/spezifische_Wärme_Kalium.png "*Spezifische Wärme von Kalium bei tiefen Temperaturen. Geplottet ist $C_p(T)$ gegen $T^2$ (Daten aus W.H. Lien, N.E. Phillips, Phys. Rev. 133, A1370 (1964)); Bildquelle: Vorlesungsskript zur Vorlesung Festkörperphysik WS 1998/1999 und SS 1999, Prof. Dr. Rudolf Gross und Dr. Achim Marx, Walther-Meissner-Institut *")




## Aufgabe 11

                                      {{0}}
>__11.__ Welche Gründe kann es für Abweichungen der theoretischen Sommerfeld-Koeffizienten $\gamma_\mathrm{theo}$ und dem dazugehörigen gemessenen Koeffizienten $\gamma_\mathrm{exp}$ geben?

                                      {{1}}
**Lösung Aufgabe 11**

                                      {{2}}
Der theoretische Sommerfeld-Koeffizent $\gamma_\mathrm{theo}$ ergibt sich aus der aus der inneren Energie $U$ eines Elektonengases abgeleiteten spezifischen Wärmekapazität des Elektronengases:

                                      {{3}}
$$C_V=\frac{\pi^2}{3}k_\mathrm{B}^2 T D(E_\mathrm{F})=\frac{\pi^2}{2}Nk_\mathrm{B}\frac{T}{T_\mathrm{F}}=\gamma_\mathrm{theo}\cdot T$$

                                      {{3}}
mit dem Sommerfeld Koeffizienten 
$$\gamma_\mathrm{theo}=\frac{\pi^2}{3}k_\mathrm{B}^2  D(E_\mathrm{F})=\frac{\pi^2Nk_\mathrm{B}}{2T_\mathrm{F}}$$

                                      {{4}}
Die beobachteten Abweichungen zwischen $\gamma_\mathrm{theo}$ und $\gamma_\mathrm{exp}$ können folgende Ursachen haben:

                                      {{5}}
- Wechselwirkung der Elektronen mit dem Kristallpotential. Das Elektron ist also nicht richtig "frei".
- Wechselwirkung der Elektronen mit Phononen. Anschaulich gesprochen verformen die Elektronen bei ihrer Bewegung durch das Kristallgitter das Kristallgitter und müssen bei ihrer Bewegung diese Verformung mitschleppen. Dadurch werden sie gebremst (höhere effektive Masse).
- Die Wechselwirkung von Elektronen untereinander führt ebenfalls zu einer höheren effektiven Masse.

                                      {{6}}
Insbesondere die 3d-Übergangsmetalle liefern große Abweichungen, weil die 3d-Elektronen zwar wesentlich zur Zustandsdichte an der Fermi-Kante beitragen, aber stark lokalisiert sind und schlecht durch freie Elektronen beschrieben werden.


## Aufgabe 12

                                      {{0}}
>__12.__ Welcher Sachverhalt wird mit der Matthiesenschen Regel beschrieben?

                                      {{1}}
**Lösung Aufgabe 12**

                                      {{2}}
Die mittlere Stoßzeit $\tau$ der Elektronen ergibt sich aus der Stoßzeit für Stöße mit Phononen $\tau_\text{P}$ und der Stoßzeit für Stöße mit Gitterfehlern $\tau_\text{i}$ zu:

                                      {{3}}
$$\frac{1}{\tau }=\frac{1}{{ \tau}_\text{P}} +{\frac{1}{\tau_\text{i}}}$$

                                      {{4}}
(Hinweis: bei der Addition der reziproken Terme "übernimmt der keinste Term das Kommando")

                                      {{5}}
Für die spezifischen Widerstände von Metallen folgt dann:
$$\rho\ = \rho_\text{P} + \rho_\text{i}$$

                                      {{6}}
Dabei ist $\rho_\text{i}$ der Restwiderstand (unabhängig von $T$) und $\rho_\text{P}$ der  durch Gitterschwingungen verursachte Widerstand (für höhere Temperaturen       proportional zu T)

                                      {{7}}
Die verschiedenen Stoßprozesse 1, 2, 3, ... können näherungsweise als von- einander unabhängig betrachtet werden. Es gilt allgemein:

                                      {{8}}
$$\frac{1}{\tau} =\frac{1}{\tau_1} +\frac{1}{\tau}_2+\frac{1}{\ \tau_3}\ +\ ....$$



## Aufgabe 13

                                      {{0}}
>__13.__ Geben Sie eine anschauliche Erklärung dafür, dass Umklapp-Streuungen von Elektronen durch Phononen bei niedrigeren Temperaturen unwahrscheinlicher werden.

                                      {{1}}
**Lösung Aufgabe 13**

                                      {{2}}
Umklapp-Streuung: Elektron-Phonon-Streuung

                                      {{3}}
Es gilt der Impulserhaltungssatz, wobei $G$ ein reziproker Gittervektor ist, $k$ und $k'$ Wellenvektoren des Elektrons und $K$ der Wellenvektor des Phonons:
$$k' = k + K+ G  $$

                                      {{4}}
![Elektron-Phonon-Streung: Umklappprozess](media/Umklappstreuung_Elektronen.png "Elektron-Phonon-Streung: Umklappprozess ($q=K$); Bildquelle: Vorlesungsskript zur Vorlesung Festkörperphysik WS 1998/1999 und SS 1999, Prof. Dr. Rudolf Gross und Dr. Achim Marx, Walther-Meissner-Institut ")

                                      {{5}}
Nur Elektronen nahe der Fermikante $E_\mathrm{F}$ können (in freie Zustände) gestreut werden. Für eine Umpkappstreuung eines Elektrons an einen Phonon wird aber eine minimales $K_0=q_\text{min}$ benötigt. Bei tiefen Temperaturen wird diese Anregung unwahrscheinlicher.


