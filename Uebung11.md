<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.0.1
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


## Aufgabe 1

> Gegeben sei eine Kugel aus einem Supraleiter erster Art mit einem kritischen Feld $H_\mathrm{C}$. Zeigen Sie, dass im Bereich des Meißner-Effekts die effektive Magnetisierung innerhalb der Kugel durch $M = -\frac{3}{2} H_\mathrm{a}$ gegeben ist und dass das Magnetfeld an der Oberfläche der Kugel in der Äquatorebene $\frac{3}{2} B_\mathrm{a}$ ist.

                                      {{1}}
In Übung 6, Aufgabe 2 hatten wir gezeigt, dass für das Magnetfeld $H$ und die magnetische Induktion $B$ im Probeninneren gilt:
$$H = \frac{1}{1 + N \cdot \chi} \cdot H_\mathrm{a}$$
$$B = \frac{1 + \chi}{1 + N \cdot \chi} \cdot B_\mathrm{a}$$

                                      {{2}}
Dabei ist $B_\mathrm{a} = \mu_0 H_\mathrm{a}$. Für eine Kugel ist der Entmagnetisierungsfaktor $N = \frac{1}{3}$. Weiterhin ist für einen Supraleiter erster Art $\chi = -1$. Damit erhalten wir:
$$H = \frac{3}{2} H_\mathrm{a}$$
$$B = 0$$

                                      {{3}}
Die Magnetisierung erhalten wir aus $M = \chi H$ und es ergibt sich:
$$M = -H = - \frac{3}{2} H_\mathrm{a}$$

                                      {{4}}
Das obige Ergebnis $B = 0$ gilt tatsächlich nur im Inneren der Kugel. Da die Tangentialkomponente von $\vec{H}$ stetig sein muss, folgt für $B$ an der Oberfläche der Kugel in der Äquatorebene:
$$B_\mathrm{Äquator} = \frac{3}{2} B_\mathrm{a}$$

                                      {{5}}
Da die Normalkomponente von $\vec{B}$ stetig sein muss, folgt für die Pole auf der Kugeloberfläche:
$$B_\mathrm{Pole} = 0$$


## Aufgabe 2 

> Berechnen Sie die Ortsabhängigkeit der magnetischen Flussdichte im Inneren eines Supraleiters für den Fall:
>
> a) dass ein homogenes magnetisches Feld $\vec{B}_0 = B_0 \vec{e}_z$ in einen den Halbraum $x \geq 0$ ausfüllenden Supraleiter eindringt.
>
> b) dass ein homogenes magnetisches Feld $\vec{B}_0 = B_0 \vec{e}_z$ parallel zur Oberfläche einer dünnen supraleitenden Platte, welche den Raum $–\frac{d}{2} \leq x \leq+\frac{d}{2}$ ausfüllt, angelegt wird.


                                      {{1}}
Die **2. London-Gleichung** können wir mit dem Laplace-Operator $\Delta$ allgemein schreiben als:
$$\Delta \vec{B} - \frac{1}{\lambda_\mathrm{L}^2} \vec{B} = 0$$

                                      {{2}}
Für ein homogenes magnetisches Feld $\vec{B}_0 = B_0 \vec{e}_z$, das ausschließlich in $z$-Richtung zeigt, und einen Supraleiter, der in $y$- und $z$-Richtung unendlich ausgedeht ist, ergibt sich:
$$\frac{\mathrm{d}^2 B}{\mathrm{d} x^2} - \frac{1}{\lambda_\mathrm{L}^2} B = 0$$

                                      {{3}}
Da sich das Material (und damit das Magnetfeld $B$) nur in $x$-Richtung ändert, muss nur die Ableitung nach $x$ berücksichtigt werden. Die allgemeine Lösung dieser Differentialgleichung 2. Ordnung ist:
$$B(x) = C_1 \exp \left( -\frac{x}{\lambda_\mathrm{L}} \right) + C_2 \exp \left( \frac{x}{\lambda_\mathrm{L}} \right)$$

                                      {{4}}
**a)** Für einen den Halbraum $x \geq 0$ ausfüllenden Supraleiter gelten die Randbedingungen $B(0) = B_0$ und $B(\infty) = 0$. Einsetzen der Randbedingung $B(\infty) = 0$ in die allgemeine Lösung liefert $C_2 = 0$. Aus $B(0) = B_0$ folgt dann noch $C_1 = B_0$. Damit ergibt sich für diesen Fall die Lösung:
$$B(x) = B_0 \exp \left( -\frac{x}{\lambda_\mathrm{L}} \right)$$

                                      {{5}}
**b)** Für eine dünne supraleitende Platte, welche den Raum $–\frac{d}{2} \leq x \leq+\frac{d}{2}$ ausfüllt, gelten die Randbedingungen $B(-x) = B(+x)$ und $B(\frac{d}{2}) = B_0$. Einsetzen der ersten Randbedingung $B(-x) = B(+x)$ in die allgemeine Lösung liefert $C_1 = C_2$. Die zweite Randbedingung $B(\frac{d}{2}) = B_0$ führt dann auf:
$$B_0 = C_1 \exp \left( -\frac{d}{2 \lambda_\mathrm{L}} \right) + C_1 \exp \left( \frac{d}{2 \lambda_\mathrm{L}} \right) = 2 C_1 \cosh \left( \frac{d}{2 \lambda_\mathrm{L}} \right)$$

                                      {{6}}
Für den Parameter $C_1$ gilt also:
$$C_1 = \frac{B_0}{2 \cosh \left( \frac{d}{2 \lambda_\mathrm{L}} \right)}$$

                                      {{7}}
Da $C_1 = C_2$ gilt, können wir den Zusammenhang $2 \cosh(z) = \exp(z) + \exp(-z)$ auch auf die allgemeine Lösung anwenden und erhalten für den Fall der supraleitenden Platte:
$$B(x) = B_0 \frac{\cosh(\frac{x}{\lambda_\mathrm{L}})}{\cosh(\frac{d}{2 \lambda_\mathrm{L}})}$$

                                      {{8}}
![Dielektrische Funktion eines Ionenkristalls](Bilder/Magnetfeld_Halbraum.png "Exponentieller Abfall der magnetischen Flussdichte $B(x)$ als Funktion des Abstandes $x$ von der Oberfläche eines massiven Supraleiter. Das externe Feld ist in $z$-Richtung angelegt, der Supraleiter erstreckt sich im Halbraum $x \geq 0$. *Quelle: Rudolf Gross und Achim Marx, Vorlesungsskript Festkörperphysik, 2008*")
![Schematische Darstellung des Verlaufs der magnetischen Flussdichte in einer dünnen supraleitenden Platte in der Größenordnung der Londonschen Eindringtiefe](Bilder/Magnetfeld_Platte.png "Schematische Darstellung des Verlaufs der magnetischen Flussdichte in einer dünnen supraleitenden Platte der Dicke $d$ in der Größenordnung der Londonschen Eindringtiefe $\lambda_\mathrm{L}$. Die Platte liegt in der $yz$-Ebene, das äußere Magnetfeld ist parallel zur $z$-Achse angelegt. Die Flussdichte nimmt im Zentrum der Schicht nicht auf Null ab. *Quelle: Rudolf Gross und Achim Marx, Vorlesungsskript Festkörperphysik, 2008*")


## Aufgabe 3

> In einem Dauerstromexperiment wird das Abklingen des durch den Suprastrom $I_\mathrm{s}$ in einem geschlossenen supraleitenden Ring (Radius $r_0 = 1~\mathrm{mm}$ und Drahtradius $r_1 = 0,\!1~\mathrm{mm}$) erzeugten magnetischen Moments benutzt, um den Widerstand des Supraleiters abzuschätzen.
>
> a) Schätzen Sie den Strom $I_\mathrm{s}$ für ein Feld von $1~\mathrm{mT}$ im Zentrum des Rings ab.
>
> b) Nach einem Jahr wird eine Abnahme des magnetischen Moments um $5~\%$ gemessen. Welcher maximale Widerstand des Supraleiters kann daraus abgeschätzt werden?


                                      {{1}}
Exzitonen sind Wasserstoff-artige Energieniveaus unterhalb der Leitungsbandkante. Mit der Bandlückenenergie $E_\mathrm{g}$ und der reduzierten Masse $\mu^\ast$ gilt:
$$E_n = E_\mathrm{g} - \frac{\mu^\ast e^4}{2 (4 \pi \varepsilon_0 \varepsilon_\mathrm{r} \hbar)^2} \cdot \frac{1}{n^2}$$

                                      {{2}}
Für die ersten beiden Exzitonen mit $n=1$ und $n=2$ gilt also:
$$E_1 = E_\mathrm{g} - \frac{\mu^\ast e^4}{2 (4 \pi \varepsilon_0 \varepsilon_\mathrm{r} \hbar)^2} \cdot \frac{1}{1} = E_\mathrm{g} - \Delta E$$
$$E_2 = E_\mathrm{g} - \frac{\mu^\ast e^4}{2 (4 \pi \varepsilon_0 \varepsilon_\mathrm{r} \hbar)^2} \cdot \frac{1}{4} = E_\mathrm{g} - \frac{\Delta E}{4}$$

                                      {{3}}
Da $E_1$ und $E_2$ gegeben sind, können wir nach der Bandlückenenergie $E_\mathrm{g}$ und der Bindungsenergie $\Delta E$ des ersten Exzitons ($n=1$) auflösen:
$$E_\mathrm{g} = \frac{1}{3} \cdot (4 E_2 - E_1) = 1,\!519~\mathrm{eV}$$
$$\Delta E = \frac{4}{3} \cdot (E_2 - E_1) = 0,\!0034~\mathrm{eV}$$

                                      {{4}}
Den Exzitonenradius (für das erste Exziton mit $n=1$) erhalten wir folgendermaßen:
$$a_\mathrm{ex} = \frac{e^2}{8 \pi \varepsilon_0 \varepsilon_\mathrm{r} \Delta E} = 20~\mathrm{nm}$$


## Aufgabe 4

> Worin besteht der Unterschied zwischen einem Supraleiter vom Typ I und einem Supraleiter vom Typ II? Was versteht man unter einer Shubnikov-Phase?

                                      {{1}}
Das elektrische Feld in der Umgebung eines Dipols $\vec{p}$ ist:
$$\vec{E} (\vec{r}) = \frac{1}{4 \pi \varepsilon_0} \left( 3 \, \frac{\vec{p} \cdot \vec{r}}{r^5} \, \vec{r} - \frac{1}{r^3} \, \vec{p} \right)$$

                                      {{2}}
Wir betrachten die zwei Atome als zwei parallele Dipolmomente $\vec{p}_1$ und $\vec{p}_2$ mit dem Abstand $r=a$. Für die Feldstärke des ersten Dipolmoments gilt entlang der Verbindungslinie (entlang der Dipolachse):
$$E_1(a) = \frac{1}{4 \pi \varepsilon_0} \cdot \frac{3 p_1 - p_1}{a^3} = \frac{1}{4 \pi \varepsilon_0} \cdot \frac{2 p_1}{a^3}$$

                                      {{3}}
Nutzen wir die Definition der Polarisierbarkeit $\alpha$, erhalten wir für die Größe des zweiten Dipolmoments:
$$p_2 = \alpha \cdot E_1(a) = \frac{\alpha \cdot p_1}{2 \pi \varepsilon_0 a^3}$$

                                      {{4}}
Da es sich um zwei gleiche Atome handelt, müssen auch die Dipolmomente gleich sein, d. h. $p_1 = p_2$. Daraus folgt:
$$\alpha = 2 \pi \varepsilon_0 a^3$$


## Aufgabe 5

> Erklären Sie, warum die BCS-Theorie für die Temperaturabhängigkeit der Wärmekapazität der Elektronen für Temperaturen unterhalb $T_\mathrm{C}$ eine exponentielle Abhängigkeit anstelle der üblichen linearen Abhängigkeit voraussagt.

                                      {{1}}
************************************
In einer Elementarzelle der Perowskit-Struktur von BaTiO<sub>3</sub> befinden sich folgende Ionen:

- 1 Kation Ba^2+^
- 1 Kation Ti^4+^
- 3 Anionen O^2−^
************************************

                                      {{2}}
Es gibt also 6 positive und 6 negative Ladungen. In einer Stoffmenge von $1~\mathrm{mol}$ befindet sich also die Ladung: 
$$Q = 6 N_\mathrm{A} e$$

                                      {{3}}
Das molare Dipolmoment ist damit:
$$p_\mathrm{m} = Q \cdot \Delta x$$

                                      {{4}}
Das molare Dipolmoment ergibt sich andererseits über das molare Volumen $V_\mathrm{m}$ und die Sättigungspolarisation $P_\mathrm{S}$ gemäß:
$$p_\mathrm{m} = V_\mathrm{m} \cdot P_\mathrm{S}$$

                                      {{5}}
Für die Gitterverschiebung $\Delta x$ folgt also:
$$\Delta x = \frac{V_\mathrm{m} \cdot P_\mathrm{S}}{Q} = \frac{V_\mathrm{m} \cdot P_\mathrm{S}}{6 N_\mathrm{A} e} = 1,\!7 \cdot 10^{-11}~\mathrm{m} = 0,\!17~\mathrm{\AA}$$