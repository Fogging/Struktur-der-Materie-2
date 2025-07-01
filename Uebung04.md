<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.1
language: de
narrator: Deutsch Female
comment:  Struktur der Materie 2 - Übung 04

@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md
import: https://github.com/liascript/CodeRunner
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 4

                                      {{1}}
************************************
**Frage 1: Welche Zusammenhänge zwischen dielektrischer Verschiebung $D$ und elektrischem Feld $E$ sind korrekt?**

- [[X]] $D = \varepsilon_0 \varepsilon_r E$
- [[ ]] $D = \varepsilon_0 \chi E$
- [[ ]] $D = \varepsilon_0 \varepsilon_r E + P$
- [[X]] $D = \varepsilon_0 E + P$
************************************

                                      {{2}}
************************************
**Frage 2: Wie lautet die korrekte Definition der Polarisierbarkeit $\alpha$?**

- [(X)] $p = \alpha \cdot E$
- [( )] $p = \alpha \cdot D$
- [( )] $p = \alpha \cdot P$
- [( )] $p = \alpha \cdot \chi$
************************************


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

> Betrachten Sie eine isolierende Kugel mit der Dielektrizitätskonstante $\varepsilon_\mathrm{r}$ in einem äußeren homogenen elektrischen Feld $E_\mathrm{a}$. Welchen Wert hat das über das gesamte Volumen der Kugel gemittelte elektrische Feld $E$ innerhalb der Kugel (Entelektrisierungsfaktor $N = 1/3$)? Welchen Wert hat die Polarisation $P$ in der Kugel? Berechnen Sie das Verhältnis $E/E_\mathrm{a}$, wenn die Kugel aus Polyethylen ($\varepsilon_\mathrm{r} = 2,\!3$) besteht.

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

> Berechnen Sie für die Metalle Silber ($m^\ast = 1,\!03\,m_\mathrm{e}$, $n = 5,\!86 \cdot {10}^{22}~\mathrm{cm}^{-3}$) und Aluminium ($m^\ast = 0,\!50\,m_\mathrm{e}$, $n = 6,\!02 \cdot {10}^{22}~\mathrm{cm}^{-3}$) jeweils die Plasmafrequenz und Plasmonenenergie sowie die entsprechende Wellenlänge, ab welcher das Reflexionsvermögen deutlich ansteigt. Zum Vergleich berechne man die entsprechenden Werte für Silizium, das mit Phosphor dotiert wurde ($m^\ast = 0,\!26\,m_\mathrm{e}$, $n = 5,\!0 \cdot {10}^{18}~\mathrm{cm}^{-3}$, $\varepsilon_\mathrm{r} = 11,\!7$).

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

> Aus optischen Messungen bestimmt sich die Plasmafrequenz eines organischen Leiters zu $2 \cdot {10}^{15}~\mathrm{s}^{-1}$. Die Relaxationszeit der Elektronen beträgt bei Raumtemperatur $3 \cdot {10}^{-15}~\mathrm{s}$. Berechnen Sie daraus die elektrische Leitfähigkeit des Materials ($\varepsilon_\mathrm{r} \approx 1$).

                                      {{1}}
Die Gleichstromleitfähigkeit nach Drude erhalten wir aus:
$$\sigma(0) = \frac{e^2 n \tau}{m^\ast} = \varepsilon_0 \varepsilon_\mathrm{r} \tau \omega_\mathrm{p}^2$$

                                      {{2}}
Aus den gegebenen Werten ergibt sich:
$$\sigma(0) = 1,\!06 \cdot 10^5~\mathrm{\frac{1}{\Omega m}}$$

                                      {{3}}
Das Reziproke der Leitfähigkeit ist der spezifische Widerstand:
$$\rho(0) = \frac{1}{\sigma(0)} = 9,\!4 \cdot 10^{-6}~\mathrm{\Omega m}$$
