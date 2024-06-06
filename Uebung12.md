<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.0.1
language: de
narrator: Deutsch Female
comment:  Struktur der Materie 2 - Übung 12

@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md
import: https://github.com/liascript/CodeRunner
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 12


## Aufgabe 1

> Ein Supraleiter hat eine kritische Temperatur von $T_\mathrm{C} = 20~\mathrm{K}$. Bei $4,\!2~\mathrm{K}$ beträgt das kritische Feld $B_\mathrm{C} = 30~\mathrm{T}$. Bei welcher maximalen Arbeitstemperatur kann der Supraleiter für einen supraleitenden Magneten von $10~\mathrm{T}$ eingesetzt werden?

                                      {{1}}
Der Realteil der dielektrischen Funktion eines Ionenkristalls ist bei Vernachlässigung der Dämpfung:
$$\varepsilon_\mathrm{r}(\omega) = \varepsilon_\mathrm{stat} \cdot \frac{\omega_\mathrm{LO}^2 - \omega^2}{\omega_\mathrm{TO}^2 - \omega^2}$$

                                      {{2}}
Außerdem gilt die **Lyddane-Sachs-Teller-Relation**, die das Verhältnis der Eigenfrequenzen der longitudinalen und transversalen optischen Schwingungen mit der Dielektrizitätskonstante $\varepsilon_\mathrm{r}(0)$ bei $\omega = 0$ und der Dielektrizitätskonstante $\varepsilon_\mathrm{stat}$ für sehr hohe Frequenzen $\omega \gg \omega_\mathrm{LO}$ in Beziehung setzt:
$$\frac{\omega_\mathrm{LO}^2}{\omega_\mathrm{TO}^2} = \frac{\varepsilon_\mathrm{r}(0)}{\varepsilon_\mathrm{stat}}$$

                                      {{3}}
Die Dielektrizitätskonstante $\varepsilon_\mathrm{stat}$ können wir aus dem Brechungsindex im Sichtbaren berechnen:
$$\varepsilon_\mathrm{stat} = n_\mathrm{S}^2 = 2,\!25$$

                                      {{4}}
Dann erhalten wir die LO-Phononenfrequenz $\omega_\mathrm{LO}$ aus der Lyddane-Sachs-Teller-Relation:
$$\omega_\mathrm{LO} = \omega_\mathrm{TO} \cdot \sqrt{\frac{\varepsilon_\mathrm{r}(0)}{\varepsilon_\mathrm{stat}}} = 5,\!02 \cdot {10}^{13}~\mathrm{s^{-1}}$$

                                      {{5}}
Die zwei Phononenfrequenzen liegen also im FIR-Bereich. Die entsprechenden Wellenlängen sind:
$$\lambda_\mathrm{LO} = 2 \pi c / \omega_\mathrm{LO} = 37,\!5~\mathrm{µm}$$
$$\lambda_\mathrm{TO} = 2 \pi c / \omega_\mathrm{TO} = 60,\!8~\mathrm{µm}$$

                                      {{6}}
![Dielektrische Funktion eines Ionenkristalls](Bilder/Dielektrische-Funktion-Ionenkristall.png "Dielektrische Funktion eines Ionenkristalls für $\omega_\mathrm{LO} = 1,\!5 \cdot \omega_\mathrm{TO}$ und $\varepsilon_\mathrm{stat} = 1,\!5$ mit einer endlichen Dämpfung, welche die Singularität bei $\omega = \omega_\mathrm{TO}$ beseitigt. *Quelle: Rudolf Gross und Achim Marx, Vorlesungsskript Festkörperphysik, 2008*")
![Veranschaulichung der ionischen Polarisation](Bilder/Reflexionsvermögen-Ionenkristall.png "Reflexionsvermögen eines Ionenkristalls bei Vernachlässigung der Dämpfung für $\omega_\mathrm{LO} = 1,\!5 \cdot \omega_\mathrm{TO}$ und $\varepsilon_\mathrm{stat} = 1,\!5$. *Quelle: Rudolf Gross und Achim Marx, Vorlesungsskript Festkörperphysik, 2008*")


## Aufgabe 2 

> In einem Draht aus Blei mit dem Radius von $3~\mathrm{mm}$ fließt im supraleitenden Zustand ein Strom von $100~\mathrm{A}$. Angenommen die Zahl der Cooper-Paare beträgt $5 \cdot 10^{27}~\mathrm{m^{-3}}$, wie groß ist dann die mittlere Geschwindigkeit der Paare? Vergleichen Sie das Ergebnis mit der Fermi-Geschwindigkeit der Elektronen in Blei ($E_\mathrm{F} = 9,\!37~\mathrm{eV}$).

                                      {{1}}
Für den elektrostatischen Fall ($\omega = 0$) benutzen wir die **Clausius-Mossotti-Gleichung**:
$$\frac{\varepsilon_\mathrm{r} - 1}{\varepsilon_\mathrm{r} + 2} = \frac{\alpha_0 n}{3 \varepsilon_0} = \frac{\alpha_0}{3 \varepsilon_0} \cdot \frac{\varrho N_\mathrm{A}}{M}$$

                                      {{2}}
Umstellen nach der gesuchten Polarisation $\alpha_0$ und Einsetzen der gegebenen Werte liefert:
$$\alpha_0 = 3 \cdot \frac{\varepsilon_\mathrm{r}(0) - 1}{\varepsilon_\mathrm{r}(0) + 2} \cdot \frac{M \varepsilon_0}{\varrho N_\mathrm{A}} = 1,\!2 \cdot 10^{-39}~\mathrm{\frac{C m^2}{V}}$$

                                      {{3}}
Für die Lösung im sichtbaren Bereich setzen wir $n_\mathrm{S}^2 = \varepsilon_\mathrm{r}$ in die Clausius-Mossotti-Gleichung ein und erhalten die **Lorentz-Lorenz-Gleichung**:
$$\frac{n_\mathrm{S}^2 - 1}{n_\mathrm{S}^2 + 2} = \frac{\alpha_\mathrm{S} n}{3 \varepsilon_0} = \frac{\alpha_\mathrm{S}}{3 \varepsilon_0} \cdot \frac{\varrho N_\mathrm{A}}{M}$$

                                      {{4}}
Umgestellt nach $\alpha_\mathrm{S}$ erhalten wir:
$$\alpha_\mathrm{S} = 3 \cdot \frac{n_\mathrm{S}^2 - 1}{n_\mathrm{S}^2 + 2} \cdot \frac{M \varepsilon_0}{\varrho N_\mathrm{A}} = 5,\!9 \cdot 10^{-40}~\mathrm{\frac{C m^2}{V}}$$

                                      {{5}}
Wenn ein statisches elektrisches Feld angelegt wird, ergibt sich eine Polarisation von:
$$P_0 = (\varepsilon_\mathrm{r} - 1) \varepsilon_0 E = 4,\!4 \cdot 10^{-5}~\mathrm{C/m^2}$$

                                      {{6}}
Das elektrische Dipolmoment beträgt:
$$p = \frac{P_0}{n} = \frac{P_0 M}{\varrho N_\mathrm{A}} = 3,\!2 \cdot 10^{-33}~\mathrm{Cm}$$

                                      {{7}}
Die entsprechende Dipollänge ist:
$$r = \frac{p}{e} = 2,\!0 \cdot 10^{-14}~\mathrm{m} = 2,\!0 \cdot 10^{-4}~\mathrm{\AA}$$
Dies ist also weniger als ein Tausendstel der Gitterkonstante!


## Aufgabe 3

> Temperatur- und feldabhängige Messungen des elektrischen Widerstands haben gezeigt, dass Nb<sub>3</sub>Ge bei $22,\!3~\mathrm{K}$ in den supraleitenden Zustand übergeht. Das kritische Feld $B_\mathrm{C,2}$ beträgt $7,\!3~\mathrm{T}$. Die direkte Messung der Eindringtiefe ergab $\lambda = 2250~\mathrm{\AA}$. Die Energielücke wurde aus dem Verlauf der elektronischen spezifischen Wärme zu $\Delta = 5~\mathrm{meV}$ ermittelt. Zu welchem Supraleiter-Typ gehört Nb<sub>3</sub>Ge? Kann Nb<sub>3</sub>Ge als konventioneller BCS-Supraleiter betrachtet werden?

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

> Bis zu welcher maximalen Stromdichte bleibt ein Blei-Draht von $4~\mathrm{mm}$ Durchmesser bei $4,\!2~\mathrm{K}$ supraleitend? Die kritische Temperatur für Blei liegt bei $7,\!2~\mathrm{K}$ und das kritische Feld $B_\mathrm{C}$ beträgt $8,\!0 \cdot 10^{-2}~\mathrm{T}$.

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

> Die Sprungtemperaturen für die Quecksilber-Isotope ^200^Hg und ^204^Hg betragen $4,\!185~\mathrm{K}$ und $4,\!146~\mathrm{K}$. Für den funktionellen Zusammenhang zwischen der Sprungtemperatur und der Isotopenmasse gilt: $T_\mathrm{C} = c \cdot M^{-\alpha}$ mit den Konstanten $c$ und $\alpha$. Bestimmen Sie den Wert der Konstante $\alpha$. Vergleichen Sie das Ergebnis mit der Masseabhängigkeit der Frequenz eines harmonischen Oszillators.

                                      {{1}}
Gemäß des gegebenen Zusammenhangs zwischen der Sprungtemperatur und der Isotopenmasse gilt für die zwei zu betrachtenden Isotope:
$$T_\mathrm{C,1} = c \cdot M_1^{-\alpha}$$
$$T_\mathrm{C,2} = c \cdot M_2^{-\alpha}$$

                                      {{2}}
Für das Verhältnis der zwei Sprungtemperaturen folgt: 
$$\frac{T_\mathrm{C,1}}{T_\mathrm{C,2}} = \frac{M_1^{-\alpha}}{M_2^{-\alpha}} = \left( \frac{M_1}{M_2} \right)^{-\alpha}$$

                                      {{3}}
Um den Exponenten zu erhalten, nutzen wir den Logarithmus:
$$\alpha = - \frac{\ln ( T_\mathrm{C,1} / T_\mathrm{C,2} )}{\ln (M_1 / M_2)} = 0,\!473$$

                                      {{4}}
Wir erhalten also $\alpha \approx \frac{1}{2}$, d. h. die Isotopenmasse beeinflusst nur die Phononenfrequenz und nicht das gesamte Phononenspektrum. Es gilt näherungsweise:
$$T_\mathrm{C} \approx \frac{c}{\sqrt{M}}$$

                                      {{5}}
Dies entspricht der Masseabhängigkeit der Kreisfrequenz eines harmonischen Oszillators mit der Federkonstante $k$ und der Masse $M$:
$$\omega = \sqrt{\frac{k}{M}}$$


## Aufgabe 6

> Ein Magnet mit einer Masse von $5~\mathrm{g}$ und einem magnetischen Moment $\mu$ von $0,\!3~\mathrm{J/T}$ schwebt über einer Scheibe aus einem Supraleiter vom Typ I (Meißner-Effekt). In welcher Höhe $h$ schwebt der Magnet, wenn sich die potentielle magnetische Energie des Magneten wie folgt berechnet:
> $$E_\mathrm{mag} = \frac{\mu_0 \mu^2}{32 \pi h^3}$$


                                      {{1}}
Wir setzen die potentielle Lage-Energie gleich der magnetischen Energie:
$$E_\mathrm{pot} = m g h = \frac{\mu_0 \mu^2}{32 \pi h^3} = E_\mathrm{mag}$$

                                      {{2}}
Umstellen nach der Höhe $h$ liefert: 
$$h = \left( \frac{\mu_0 \mu^2}{32 \pi m g} \right)^\frac{1}{4} = 1,\!23~\mathrm{cm}$$