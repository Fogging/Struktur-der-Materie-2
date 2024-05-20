<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.0.1
language: de
narrator: Deutsch Female
comment:  Struktur der Materie 2 - Übung 07

@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md
import: https://github.com/liascript/CodeRunner
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 7


## Aufgabe 1

> Betrachten Sie ein Wasserstoffatom in einem äußeren elektrischen Feld, das senkrecht zur Bahnebene steht (semiklassische Betrachtungsweise). Zeigen Sie, dass in diesem Fall für die elektronische Polarisierbarkeit des Wasserstoffatoms $\alpha_\mathrm{el} = 4 \pi \varepsilon_0 a_0^3$ gilt, wobei $a_0$ der Radius der ungestörten Bahn ist. Nehmen Sie an, dass das angelegte Feld in $x$-Richtung zeigt und die Bahnebene in der $yz$-Ebene liegt. Die Auslenkung $x$ soll außerdem klein gegenüber $a_0$ sein. Hinweis: Die $x$-Komponente des Kernfeldes an der ausgelenkten Position der Elektronenbahn muss gleich dem angelegten Feld sein.

                                      {{1}}
************************************
Das äußere Feld $\vec{E}_\mathrm{a}$ bewirkt eine elektrische Kraft $\vec{F}_\mathrm{el} = q \vec{E}_\mathrm{a}$ auf das Proton (des Wasserstoffatoms) in $x$-Richtung. Dadurch neigt sich die klassische Kreisbahn des Elektrons um das Proton leicht aus der $yz$-Ebene heraus. Der Verkippungswinkel der Kreisbahn sei $\vartheta$. Der Betrag der elektrischen Kraft in $x$-Richtung ist:
$$F_{\mathrm{el}, x} = e E_\mathrm{a}$$

![Wasserstoffatom in einem äußeren elektrischen Feld, das senkrecht zur Bahnebene steht](Bilder/Feld_lokal.png "Wasserstoffatom in einem äußeren elektrischen Feld, das senkrecht zur Bahnebene steht *Quelle: Hartmut Stöcker, [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/)*")<!-- style = "width: 250px;" -->
************************************

                                      {{2}}
Wir betrachten nun die Coulomb-Kraft $\vec{F}_\mathrm{C}$ zwischen Proton und Elektron: 
$$\vec{F}_\mathrm{C} = \frac{1}{4 \pi \varepsilon_0} \frac{q_1 q_2}{r^2} \vec{e}_r$$

                                      {{3}}
Die Coulomb-Kraft zeigt entlang des Einheitsvektors $\vec{e}_r$ parallel zum Radius-Vektor $\vec{r}$ zwischen Proton und Elektron. Wir interessieren uns für die $x$-Komponente der Kraft, die senkrecht auf der Bahnebene ($yz$-Ebene) steht. Für den Verkippungswinkel gilt dabei $\sin \vartheta = \frac{x}{r}$. Wir erhalten:
$$F_{\mathrm{C}, x} = \frac{1}{4 \pi \varepsilon_0} \frac{e^2}{r^2} \sin \vartheta = \frac{1}{4 \pi \varepsilon_0} \frac{e^2}{r^2} \frac{x}{r}$$

                                      {{4}}
Die $x$-Komponente der Coulomb-Kraft an der ausgelenkten Position der Elektronenbahn muss gleich der elektrischen Kraft durch das angelegte Feld sein:
$$F_{\mathrm{el}, x} = e E_\mathrm{a} = \frac{1}{4 \pi \varepsilon_0} \frac{e^2 x}{r^3} = F_{\mathrm{C}, x}$$

                                      {{5}}
Da das elektrische Dipolmoment einfach als $p_x = e x$ definiert ist, können wir die vorherige Formel nach dieser Größe umstellen und erhalten:
$$p_x = e x = 4 \pi \varepsilon_0 r^3 E_\mathrm{a}$$

                                      {{6}}
Das induzierte Dipolmoment ergibt sich außerdem aus der Polarisierbarkeit $\alpha$ multipliziert mit dem lokalen elektrischen Feld. Dieser Zusammenhang definiert die Polarisierbarkeit:
$$\vec{p}_\mathrm{ind} = \alpha \vec{E}_\mathrm{lokal}$$

                                      {{7}}
Das Dipolmoment liegt in unserem Fall in $x$-Richtung und wir können uns auf diese Richtung beschränken. Da wir nur ein einzelnes Wasserstoffatom betrachten, können wir das lokale gleich dem äußeren elektrischen Feld setzen:
$$p_\mathrm{ind} = p_x = \alpha E_\mathrm{a}$$

                                      {{8}}
Vergleichen wir die zwei Formeln für das Dipolmoment $p_x$, ergibt sich für die Polarisierbarkeit:
$$\alpha = 4 \pi \varepsilon_0 r^3$$

                                      {{9}}
Da $x \ll r$ (oder auch $x \ll a_0$), können wir $x$ in der Formel für den Radius der Kreisbahn näherungsweise vernachlässigen:
$$r = \sqrt{x^2 + y^2 + z^2} \approx \sqrt{y^2 + z^2} = a_0$$

                                      {{10}}
Damit haben wir den gesuchten Zusammenhang zwischen der elektronischen Polarisierbarkeit und dem ungestörten Bahnradius:
$$\alpha_\mathrm{el} = 4 \pi \varepsilon_0 a_0^3$$


## Aufgabe 2 

> Betrachten Sie eine isolierende Kugel mit der Dielektrizitätskonstante $\varepsilon$ in einem äußeren homogenen elektrischen Feld $E_\mathrm{a}$. Welchen Wert hat das über das gesamte Volumen der Kugel gemittelte elektrische Feld $E$ innerhalb der Kugel (Entelektrisierungsfaktor $N = 1/3$)? Welchen Wert hat die Polarisation $P$ in der Kugel? Berechnen Sie das Verhältnis $E/E_\mathrm{a}$, wenn die Kugel aus Polyethylen ($\varepsilon = 2,\!3$) besteht.

                                      {{1}}
Analog zum magnetischen Feld setzt sich das elektrische Feld $E$ im Inneren eines Körpers aus dem äußeren Feld $E_\mathrm{a}$ und dem Entelektrisierfeld $E_N$ zusammen:
$$E = E_\mathrm{a} - E_N$$

                                      {{2}}
Der Grund für die Entelektrisierung liegt in der elektrischen Polarisation $P$, also der Erzeugung bzw. Ausrichtung mikroskopischer Dipole, die zur Ausbildung von Oberflächenladungen führt. Diese Oberflächenladungen erzeugen das entelektrisierende Feld, das dem äußeren Feld entgegenwirkt. Das Entelektrisierfeld beträgt $E_N = N P / \varepsilon_0$, das heißt:
$$E = E_\mathrm{a} - \frac{N P}{\varepsilon_0}$$

                                      {{3}}
Die Polarisation $P$ hängt über die elektrische Suszeptibilität $\chi$ des Mediums direkt mit der lokalen elektrischen Feldstärke $E$ zusammen: $P = \chi \varepsilon_0 E$. Daraus folgt:
$$E = E_\mathrm{a} - N \chi E$$

                                      {{4}}
Für das elektrische Feld im Inneren des Dielektrikums erhalten wir also:
$$E = \frac{1}{1 + N \chi} E_\mathrm{a}$$

$\varepsilon$ oder $\varepsilon_\mathrm{r}$?

Für die dielektrische Verschiebung gilt:
D = ε0E + P = ε0E + χε0E = (1 + χ) ε0E und damit
D = \frac{1+\chi}{1+N\chi} ε0Ea
Für die Polarisation einer Kugel mit Entelektrisierungsfaktor N = 1/3 
und ε = 2,3 folgt:
χ = ε – 1 = 1,3
E = \frac{1}{1+1,3/3} Ea = 0,698 Ea und
P = \frac{1,3}{1+1,3/3} ε0Ea = 0,907 ε0Ea



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

> Berechnen Sie für die Metalle Silber ($m^\mathrm{op} = 1,\!03$, $n = 5,\!86 \cdot {10}^{22}~\mathrm{cm}^{-3}$) und Aluminium ($m^\mathrm{op} = 0,\!50$, $n = 6,\!02 \cdot {10}^{22}~\mathrm{cm}^{-3}$) jeweils die Plasmafrequenz und Plasmonenenergie, sowie die entsprechende Wellenlänge, ab welcher das Reflexionsvermögen deutlich ansteigt. Zum Vergleich berechne man die entsprechenden Werte für Silizium, das mit Phosphor dotiert wurde ($m^\mathrm{op} = 0,\!26$, $n = 5,\!0 \cdot {10}^{18}~\mathrm{cm}^{-3}$, $\varepsilon=11,\!7$).

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