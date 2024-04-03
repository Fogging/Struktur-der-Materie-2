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

> Beantworten Sie mit Hilfe der nebenstehenden Grafik die folgenden Fragen:

![Bandstruktur eines indirekten Halbleiters](Bilder/Bandstruktur_Bandlücke.png)

**a) Wie groß ist die Energie der Bandlücke?**

                                      {{1}}
Der Abstand zwischen Valenzbandmaximum und Leitungsbandminimum beträgt $\mathrm{0,\!5~eV}$.

**b) Markieren Sie die niedrigste Energie eines Elektrons im Leitungsband.**

                                      {{2}}
Das Leitungsbandminimum liegt bei $k = \frac{8}{11}\,\frac{\pi}{a}$.

**c) Markieren Sie die höchste Energie eines Loches im Valenzband.**

                                      {{3}}
Das Valenzbandmaximum liegt bei $k = 0$.

**d) Ist die Energielücke direkt oder indirekt? Warum?**

                                      {{4}}
Die Energielücke ist indirekt, da Leitungsbandminimum und Valenzbandmaximum bei unterschiedlichen $k$-Werten liegen.


## Aufgabe 4 

> Wie ist die effektive Masse von Elektronen bzw. Löchern in Halbleitern definiert?

                                      {{1}}
Die effektive Masse wird als $m^*$ oder $m^\mathrm{eff}$ bezeichnet und ergibt sich aus der inversen Krümmung des Bandes $E(k)$. Die Krümmung wird über die zweite Ableitung berechnet:
$$m^\mathrm{eff} = \hbar^2 \left( \frac{\mathrm{d}^2 E}{\mathrm{d} k^2} \right)^{-1}$$

                                      {{2}}
Für Elektronen wird für $E(k)$ das Leitungsband genutzt, für Löcher das Valenzband.


## Aufgabe 5 

> Gibt es Unterschiede in der effektiven Elektronenmasse von direkten und indirekten Halbleitern?

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