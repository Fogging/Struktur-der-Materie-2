<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.0.1
language: de
narrator: Deutsch Female
comment:  Struktur der Materie 2 - Übung 13

@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md
import: https://github.com/liascript/CodeRunner
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 13

## Aufgabe 1

> a) Erklären Sie, wie ein NMR-Spektrum zustande kommt. 
>
> b) Welche Eigenschaften eines Atomkerns führen zu einer großen NMR-Empfindlichkeit?
>
> c) In welcher Einheit wird die $x$-Achse im NMR-Spektrum angegeben und wie ist sie definiert?
>
> d) Welchen Vorteil bietet in der NMR-Spektrometrie ein möglichst starkes Magnetfeld?


                                      {{1}}
************************************
**a)** NMR-Signale entstehen durch die Wechselwirkung der Kernspins mit einem externen Magnetfeld, die Anregung durch HF-Pulse und die anschließende Relaxation, die ein messbares elektrisches Signal in einer Spule erzeugt. Die Analyse dieses Signals durch Fourier-Transformation liefert ein Spektrum, das Informationen über die chemische Struktur und Umgebung der Atome in der Probe enthält.
![Signalentstehung bei der NMR-Spektroskopie](Bilder/NMR_Signalentstehung.png "Signalentstehung bei der NMR-Spektroskopie. *Quelle: Thomas Köhler, [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/)*")
************************************

                                      {{2}}
************************************
**b)** Ein Isotop eines Elements wird empfindlich genannt, wenn es zu einem starken Signal im NMR-Spektrum führt. Dazu muss das Isotop:

- im natürlichen Isotopengemisch mit großer Häufigkeit vorkommen,
- ein großes magnetogyrisches Verhältnis besitzen,
- eine Kernspinquantenzahl von ungleich Null haben, da die Atomkerne dieses Isotops sonst kein magnetisches Moment besitzen.
************************************

                                      {{3}}
**c)** Die Energieeinheit im NMR-Spektrum ist die chemische Verschiebung $\delta$. Die chemische Verschiebung ist der Unterschied der Resonanzfrequenz der Atome einer Probe zu der der Atome des Standards TMS (Tetramethylsilan), also bezogen auf die TMS-Frequenz (bzw. $f_0$). Da die Unterschiede der Resonanzfrequenzen sehr klein sind, wird $\delta$ in $\mathrm{ppm}$ angegeben. Die chemische Verschiebung ist ein Relativmaß und daher unabhängig von der Magnetfeldstärke $B_0$.

                                      {{4}}
************************************
**d)** Je stärker das Magnetfeld ist, desto größer ist der Energieunterschied der verschiedenen Orientierungen eines atomaren magnetischen Moments im Magnetfeld. Je stärker das Magnetfeld ist, desto:

- mehr unterscheiden sich die Resonanzenergien verschiedener Atomkerne,
- intensiver werden die Absorptionen, weil weniger Atomkerne thermisch angeregt sind,
- einfacher interpretierbar werden die NMR-Spektren.
************************************


## Aufgabe 2

> a) Was ist die Kopplungskonstante $J$ in der NMR-Spektroskopie und welche Informationen lassen sich aus der Feinstruktur eines NMR-Signals ableiten?
>
> b) Sie sehen nebenstehend ein Triplett aus einem $\mathrm{250~MHz}$-Spektrum, in dem die Bandenmaxima in $\mathrm{ppm}$ beschriftet sind. Geben Sie die Kopplungskonstante $J$ in $\mathrm{Hz}$ an.
>
> ![Triplett aus einem 250 MHz-Spektrum, in dem die Bandenmaxima in ppm beschriftet sind](Bilder/NMR_Triplett.png)


                                      {{1}}
Der Zusammenhang zwischen kritischer Feldstärke $B_\mathrm{C}(T)$ und kritischer Temperatur $T_\mathrm{C}$ lautet:
$$B_\mathrm{C}(T) = B_\mathrm{C}(0) \cdot \left[1 - \left( \frac{T}{T_\mathrm{C}} \right)^2 \right]$$

                                      {{2}}
Umstellen liefert $B_\mathrm{C}(0)$, also die kritische Feldstärke bei $T = 0~\mathrm{K}$:
$$B_\mathrm{C}(0) = \frac{B_\mathrm{C}(T)}{1 - \left( \frac{T}{T_\mathrm{C}} \right)^2} = 31,\!4~\mathrm{T}$$

                                      {{3}}
Damit können wir nun die gleiche Formel nach der Temperatur $T$ umstellen, bei der $B_\mathrm{C}$ gerade den Wert $10~\mathrm{T}$ erreicht:
$$T = T_\mathrm{C} \cdot \sqrt{1 - \frac{B_\mathrm{C}(T)}{B_\mathrm{C}(0)}} = 16,\!5~\mathrm{K}$$


## Aufgabe 3 

> Was besagt die Multiplizität in der NMR-Spektroskopie? Bestimmen Sie die Multiplizität der abgebildeten ^1^H-Signale der gegebenen Molekülfragmente. Hinweis: Das betrachtete Proton ist blau markiert. Die Unterscheidung von H<sub>A</sub> und H<sub>B</sub> meint ungleiche Bindungspartner.
>
> ![1H-Signale verschiedener Molekülfragmente](Bilder/NMR_Molekülfragmente.png)

                                      {{1}}
Für den elektrischen Strom gilt:
$$I = \frac{Q}{t} = e n_\mathrm{S} A v_\mathrm{S}$$

                                      {{2}}
Umstellen nach der gesuchten Geschwindigkeit $v_\mathrm{S}$ der Cooper-Paare liefert:
$$v_\mathrm{S} = \frac{I}{e A n_\mathrm{S}}$$


                                      {{3}}
Würde die gesamte Querschnittsfläche $A$ des Blei-Drahts vom Strom durchflossen, wäre $A = \pi r^2 = 2,\!83 \cdot 10^{-5}~\mathrm{m^2}$ und die Rechnung ergäbe:
$$v_\mathrm{S} = 0,\!0044~\mathrm{\frac{m}{s}}$$

                                      {{4}}
Aufgrund des Meißner-Effekts darf das Magnetfeld aber nicht ins Innere des Supraleiters 1. Art eindringen. Daher kann auch der supraleitende Strom nur direkt an der Oberfläche des Supraleiters fließen. Er klingt mit der London’schen Eindringtiefe $\lambda_\mathrm{L}$ exponentiell von der Mantelfläche des Drahtes her ab. Die stromdurchflossene Fläche ist also viel kleiner und kann aus dem Umfang des Drahtes mit $A = 2 \pi r \cdot \lambda_\mathrm{L} = 6,\!97 \cdot 10^{-10}~\mathrm{m^2}$ abgeschätzt werden. Daraus folgt für die Geschwindigkeit der Cooper-Paare:
$$v_\mathrm{S} = 179~\mathrm{\frac{m}{s}}$$

                                      {{5}}
Die Fermi-Geschwindigkeit $v_\mathrm{F}$ der Elektronen in Blei erhalten wir aus dem Zusammenhang $E_\mathrm{F} = \frac{m}{2} v_\mathrm{F}^2$ als:
$$v_\mathrm{F} = \sqrt{\frac{2 E_\mathrm{F}}{m}} = 1,\!82 \cdot 10^6~\mathrm{\frac{m}{s}}$$

                                      {{6}}
Die mittlere Geschwindigkeit der Cooper-Paare ist also viel kleiner als die Fermi-Geschwindigkeit der Elektronen.


## Aufgabe 4

> a) Welche Multipletts ergeben sich für (i) die Methylengruppe und (ii) die Methylgruppe von Chlorethan (CH<sub>3</sub>–CH<sub>2</sub>–Cl)?
>
>b) Welche Multipletts sind für (i) die Methylengruppe und (ii) die Methingruppe von 1,1,2-Trichlorethan (Cl–CH<sub>2</sub>–CH–Cl<sub>2</sub>) zu erwarten?


                                      {{1}}
Die Kohärenzlänge $\xi_\mathrm{GL}$ erhalten wir aus dem Zusammenhang mit dem kritischen Feld $B_\mathrm{C2}$:
$$B_\mathrm{C2} = \frac{\hbar}{q_\mathrm{S} \xi_\mathrm{GL}^2} = \frac{\Phi_0}{2 \pi \xi_\mathrm{GL}^2}$$

                                      {{2}}
Dabei beträgt die Ladung $q_\mathrm{S} = 2 e$ und die Konstante $\Phi_0$ ergibt sich aus $\Phi_0 = h / q_\mathrm{S} = 2,\!07 \cdot 10^{-15}~\mathrm{Vs}$. Die Ginzburg-Landau-Kohärenzlänge ist damit:
$$\xi_\mathrm{GL} = \sqrt{\frac{\Phi_0}{2 \pi B_\mathrm{C2}}} = 6,\!7~\mathrm{nm}$$

                                      {{3}}
Das thermodynamische kritische Feld berechnet sich zu:
$$B_\mathrm{C,th} = \frac{\Phi_0}{2 \pi \sqrt{2} \xi_\mathrm{GL} \lambda_\mathrm{L}} = 0,\!15~\mathrm{T}$$

                                      {{4}}
Der Ginzburg-Landau-Parameter ergibt sich zu:
$$\kappa_\mathrm{GL} = \frac{\lambda_\mathrm{L}}{\xi_\mathrm{GL}} = \frac{B_\mathrm{C2}}{\sqrt{2} \cdot B_\mathrm{C,th}} = 34 \gg \frac{1}{\sqrt{2}}$$
Damit handelt es sich bei Nb<sub>3</sub>Ge um einen Supraleiter vom **Typ II**.

                                      {{5}}
Das Energielückenverhältnis ist:
$$\frac{\Delta(0)}{k_\mathrm{B} T_\mathrm{C}} = 2,\!6 > 1,\!764$$
Damit ist Nb<sub>3</sub>Ge ein **unkonventioneller Supraleiter**.


## Aufgabe 5

> a) Wie groß ist die Resonanzfrequenz eines Protons in einem Magnetfeld von $B = 14,\!1~\mathrm{T}$? Der Landé-Faktor für das Proton ist mit $g = 5,\!5857$ gegeben und sein magnetisches Moment entspricht einem Kernmagneton $\mu_\mathrm{N} = 5,\!0508 \cdot {10}^{-27}~\mathrm{J/T}$.
>
> b) In welchem der folgenden Systeme ist die Aufspaltung der Energieniveaus größer: (i) in einem Proton in einem $\mathrm{600~MHz}$-Spektrometer oder (ii) in einem Deuteron in demselben Spektrometer ($g_I = 0,\!8575$)?


                                      {{1}}
Fließt durch einen geraden, langen Leiter ein elektrischer Strom $I$, dann bilden die magnetischen Feldlinien Kreise um den Leiterquerschnitt. Der Betrag der magnetischen Flussdichte $B$ im Abstand $r$ ist:
$$B = \frac{\mu_0 I}{2 \pi r}$$

                                      {{2}}
Wird der Strom so stark, dass das dadurch erzeugte Magnetfeld $B$ die kritische Feldstärke $B_\mathrm{C}$ übersteigt, bricht die Supraleitung zusammen. Dann ist der kritische Strom $I_\mathrm{C}$ erreicht:
$$I_\mathrm{C} = \frac{2 \pi r B_\mathrm{C}}{\mu_0}$$

                                      {{3}}
Nun benötigen wir noch die kritische Feldstärke $B_\mathrm{C}(T)$ für $T = 4,\!2~\mathrm{K}$. Dazu nutzen wir die gleiche Formel wie in Aufgabe 1:
$$B_\mathrm{C}(T) = B_\mathrm{C}(0) \cdot \left[1 - \left( \frac{T}{T_\mathrm{C}} \right)^2 \right] = 5,\!28 \cdot 10^{-2}~\mathrm{T}$$

                                      {{4}}
Anhand der vorherigen Formel können wir nun den kritischen Strom $I_\mathrm{C}$ berechnen. Wenn wir noch den Durchmesser $d = 2r$ einsetzen, erhalten wir:
$$I_\mathrm{C} = \frac{\pi d B_\mathrm{C}}{\mu_0} = 528~\mathrm{A}$$

                                      {{5}}
Die Stromdichte $j$ ergibt sich aus dem Strom $I$ geteilt durch die Querschnittsfläche $A$. Nähme man an, dass die gesamte Querschnittsfläche des Blei-Drahts vom Strom durchflossen wird, würde sich ergeben:
$$j_\mathrm{C} = \frac{I_\mathrm{C}}{A} = \frac{I_\mathrm{C}}{\frac{\pi}{4} d^2} = 4,\!2 \cdot 10^7~\mathrm{\frac{A}{m^2}}$$

                                      {{6}}
Aufgrund des Meißner-Effekts darf das Magnetfeld aber nicht ins Innere des Supraleiters 1. Art eindringen. Daher kann auch der supraleitende Strom nur direkt an der Oberfläche des Supraleiters fließen. Er klingt mit der London’schen Eindringtiefe $\lambda_\mathrm{L}$ exponentiell von der Mantelfläche des Drahtes her ab. Für Blei ist $\lambda_\mathrm{L} = 37~\mathrm{nm}$. Die stromdurchflossene Fläche ist also viel kleiner und kann mit $A = \pi d \cdot \lambda_\mathrm{L}$ abgeschätzt werden. Dann folgt für die kritische Stromdichte:
$$j_\mathrm{C} = \frac{I_\mathrm{C}}{A} = \frac{I_\mathrm{C}}{\pi d \lambda_\mathrm{L}} = 1,\!1 \cdot 10^{12}~\mathrm{\frac{A}{m^2}}$$


## Aufgabe 6

> a) Die chemische Verschiebung der CH<sub>3</sub>-Protonen in Acetaldehyd (Ethanal) ist $\delta = 2,\!20~\mathrm{ppm}$, die des Aldehydprotons (−CHO) ist $\delta = 9,\!80~\mathrm{ppm}$. Wie groß ist die Differenz der lokalen Feldstärken für diese beiden Protonen bei einem äußeren Feld von (i) $\mathrm{1,\!5~T}$ und (ii) $\mathrm{15~T}$?
>
> b) Skizieren Sie das Aussehen des ^1^H-NMR-Spektrums von Acetaldehyd (i) in einem $\mathrm{250~MHz}$ und (ii) $\mathrm{500~MHz}$-Spektrometer. Verwenden Sie dazu $J = 2,\!9~\mathrm{Hz}$ sowie die Daten aus Teilaufgabe (a).


                                      {{1}}
Fließt durch einen geraden, langen Leiter ein elektrischer Strom $I$, dann bilden die magnetischen Feldlinien Kreise um den Leiterquerschnitt. Der Betrag der magnetischen Flussdichte $B$ im Abstand $r$ ist:
$$B = \frac{\mu_0 I}{2 \pi r}$$


## Aufgabe 7

> Die Abbildung zeigt das ^1^H-NMR-Spektrum von Ethanol (CH<sub>3</sub>CH<sub>2</sub>OH). Die stufenartigen Kurven zeigen das integrierte Signal.
>
> a) Ordnen Sie die Signale der H-Gruppen von Ethanol den Signalen im Spektrum zu.
>
> b) Erklären Sie die Feinstruktur der C-H-Protonen im Spektrum.
>
> ![1H-NMR-Spektrum von Ethanol](Bilder/NMR_Ethanol.png)



                                      {{1}}
Fließt durch einen geraden, langen Leiter ein elektrischer Strom $I$, dann bilden die magnetischen Feldlinien Kreise um den Leiterquerschnitt. Der Betrag der magnetischen Flussdichte $B$ im Abstand $r$ ist:
$$B = \frac{\mu_0 I}{2 \pi r}$$


## Aufgabe 8

> Gegeben ist ein ^1^H-NMR-Spektrum von 4-Methyl-Benzoesäureethylester (C<sub>10</sub>H<sub>12</sub>O<sub>2</sub>). Ermitteln Sie die chemischen Verschiebungen, alle vicinalen Kopplungen $^3J$ und ordnen Sie die Protongruppen im Spektrum der Molekülstruktur zu.
>
> ![1H-NMR-Spektrum von 4-Methyl-Benzoesäureethylester](Bilder/NMR_4-Methyl-Benzoesäureethylester.png)<!-- style = "width: 500px;" -->


                                      {{1}}
Fließt durch einen geraden, langen Leiter ein elektrischer Strom $I$, dann bilden die magnetischen Feldlinien Kreise um den Leiterquerschnitt. Der Betrag der magnetischen Flussdichte $B$ im Abstand $r$ ist:
$$B = \frac{\mu_0 I}{2 \pi r}$$