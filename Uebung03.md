<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.0.1
language: de
narrator: Deutsch Female
comment:  Struktur der Materie 2 - Übung 03

@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md
import: https://github.com/liascript/CodeRunner
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 3


## Aufgabe 1

> 	Die Wellenfunktion des atomaren Wasserstoffatoms im Grundzustand ($\mathrm{1s}$) lautet:
>
> $\Psi = (\pi a_0^3)^{-1/2} \exp \left( -\frac{r}{a_0} \right)$ mit $a_0 = \frac{4 \pi \varepsilon_0 \hbar^2}{m_\mathrm{e} e^2} = 0,\!529 \cdot 10^{-10}~\mathrm{m}$.
>
> Entsprechend der statistischen Interpretation der Wellenfunktion ist dann die Ladungsdichte $\rho(x,y,z)=-e|\Psi|^2$. Zeigen Sie, dass in diesem Zustand $\langle r^2 \rangle = 3a_0^2$ ist und berechnen Sie die molare diamagnetische Suszeptibilität von atomarem Wasserstoff.


                                      {{1}}
Der Erwartungswert $\langle r^2 \rangle$ berechnet sich aus:
$$\langle r^2 \rangle = \int_{-\infty}^{+\infty} \Psi^* r^2 \Psi \, \mathrm{d} \vec{r}$$

                                      {{2}}
Dieses Integral über das ganze Volumen wird in Kugelkoordinaten $(r, \vartheta, \varphi)$ ausgeführt. Da die Wellenfunktion $\Psi$ nur vom Radius $r$ abhängt, kann über die zwei Winkel $\vartheta$ und $\varphi$ leicht abintegriert werden. Neben der Anpassung der Integrationsgrenzen muss wegen der Koordinatentransformation $\mathrm{d} \vec{r} = r^2 \sin \vartheta \, \mathrm{d} \vartheta \, \mathrm{d} \varphi \, \mathrm{d} r$ beachtet werden:
$$\langle r^2 \rangle = \int_{0}^{+\infty} \int_{0}^{2 \pi} \int_{0}^{\pi} \Psi^* r^2 \Psi \, r^2 \sin \vartheta \, \mathrm{d} \vartheta \, \mathrm{d} \varphi \, \mathrm{d} r$$

                                      {{3}}
Mit $\int_{0}^{\pi} \sin \vartheta \, \mathrm{d} \vartheta = 2$ und $\int_{0}^{2 \pi} \mathrm{d} \varphi = 2 \pi$ erhält man:
$$\langle r^2 \rangle = \int_{0}^{\infty} \Psi^* r^2 \Psi \, 4 \pi r^2 \, \mathrm{d} r$$

                                      {{4}}
Da die gegebene Wellenfunktion $\Psi$ rein reell ist, gilt $\Psi^* = \Psi$ und Einsetzen ergibt:
$$\langle r^2 \rangle = 4 \pi \int_{0}^{\infty} \Psi^2 \, r^4 \, \mathrm{d} r = \frac{4 \pi}{\pi a_0^3} \, \int_{0}^{\infty} r^4 \, \exp \left( -\frac{2r}{a_0} \right) \, \mathrm{d} r$$

                                      {{5}}
Dieses bestimmte Integral kann mit Hilfe der allgemeinen Lösung $\int_{0}^{\infty} x^n \, \mathrm{e}^{-ax} \, \mathrm{d} x = \frac{n!}{a^{n+1}}$ berechnet werden. Im vorliegenden Fall ist $n = 4$ und $a = \frac{2}{a_0}$. Damit folgt:
$$\langle r^2 \rangle = \frac{4}{a_0^3} \cdot \frac{24}{(2/a_0)^5} = \frac{4}{a_0^3} \cdot \frac{24 \, a_0^5}{32} = 3 a_0^2$$

                                      {{6}}
Die diamagnetische Volumensuszeptibilität nach Langevin wird mit folgender Formel berechnet (in SI-Einheiten):
$$\chi_V = - \frac{\mu_0 e^2 n}{6 m_\mathrm{e}} \langle r^2 \rangle$$

                                      {{7}}
Dabei ist $n$ die Teilchendichte pro Volumen, für die $n = \frac{\varrho \cdot N_\mathrm{A}}{M}$ gilt (siehe Übung 2, Aufgabe 3). Für die molare Suszeptibilität folgt:
$$\chi_{mol} = \frac{M}{\varrho} \chi_V = - \frac{M}{\varrho} \cdot \frac{\mu_0 e^2 n}{6 m_\mathrm{e}} \langle r^2 \rangle = - \frac{\mu_0 e^2 N_\mathrm{A}}{6 m_\mathrm{e}} \langle r^2 \rangle$$

                                      {{8}}
Einsetzen des Ergebnisses für $\langle r^2 \rangle$ ergibt die molare diamagnetische Suszeptibilität von atomarem Wasserstoff (in SI-Einheiten):
$$\chi_{mol} = - \frac{\mu_0 e^2 N_\mathrm{A}}{6 m_\mathrm{e}} \cdot 3 a_0^2 = - \frac{\mu_0 e^2 N_\mathrm{A}}{2 m_\mathrm{e}} \cdot a_0^2 = -2,\!98 \cdot 10^{-11}~\mathrm{m^3/mol}$$

                                      {{9}}
Der Übergang in CGS-Einheiten erfordert die Division durch $4\pi$, d. h. $\chi_\mathrm{SI} = 4 \pi \cdot \chi_\mathrm{CGS}$. Die Einheiten $\mathrm{cm^3/mol}$ und $\mathrm{emu/mol}$ sind im CGS-System gleichbedeutend:
$$\chi_{mol} = -2,\!36 \cdot 10^{-12}~\mathrm{m^3/mol} = -2,\!36 \cdot 10^{-6}~\mathrm{cm^3/mol} = -2,\!36 \cdot 10^{-6}~\mathrm{emu/mol}$$

## Aufgabe 2 

> Berechnen Sie den Betrag des Bohrschen Magnetons (klassischer Ansatz).

                                      {{1}}
In der klassischen Betrachtung kreist das Elektron mit der Geschwindigkeit $v$ auf einer Kreisbahn mit dem Radius $r$ um den Atomkern. Der Betrag seines Drehimpulses ist dann $L = rp = r m_\mathrm{e} v$, worin $p = m_\mathrm{e} v$ der Impuls des Elektrons ist. 

                                      {{2}}
Der Elektronenspin bleibt unberücksichtigt. Wir berechnen nur das durch den Bahndrehimpuls $L$ verursachte magnetische Moment $\mu$, das man präziser auch Bahnmoment nennen kann. Es ist allgemein durch $\mu = IA$ gegeben, worin $I$ die elektrische Stromstärke und $A$ die vom Strom eingeschlossene Fläche ist. 

                                      {{3}}
Die von der Bahn umschlossene Fläche ist $A = \pi r^2$. Der Bahnumfang ist $u = 2 \pi r$. Daraus können wir auch den Strom berechnen:
$$I = \frac {q}{t} = \frac{-e}{u/v} = \frac{-e}{(2\pi r)/v} = \frac{-e v}{2\pi r}$$

                                      {{4}}
Damit folgt:
$$\mu = IA = \frac{-e v}{2} r$$

                                      {{5}}
Einsetzen von $\frac {L}{m_e} = r v$ ergibt das gesuchte magnetische Bahnmoment:
$$\mu = \frac{-e}{2 m_e} L$$

                                      {{6}}
Wenn man für den Bahndrehimpuls den festen Wert $L = 1 \hbar$ einsetzt, erhält man das sogenannte **Bohrsche Magneton** (in SI-Einheiten):
$$\mu_\mathrm{B} = \frac{e \hbar}{2 m_\mathrm{e}} = 9,\!274\cdot 10^{−24}~\mathrm{J/T} = 9,\!274\cdot 10^{−24}~\mathrm{A\,m^2}$$

                                      {{7}}
Für den Übergang in CGS-Einheiten benutzen wir den Zusammenhang $1~\mathrm{A\,m^2} = 10^3~\mathrm{emu}$. Das Bohrsche Magneton hat im CGS-System also den Wert:
$$\mu_\mathrm{B} = 9,\!274\cdot 10^{−21}~\mathrm{emu}$$


## Aufgabe 3

> Zeigen Sie, dass die magnetische Dipolwechselwirkung zwischen zwei magnetischen Momenten der Größe $\mu_\mathrm{B}$, die 3 Angström voneinander entfernt sind, erst bei Temperaturen unter $T=100~\mathrm{mK}$ wichtig wird.

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

> Ein magnetischer Dipol $\vec{\mu}$, der sich im Ursprung des Koordinatensystems befinden soll, erzeugt in seiner Umgebung die magnetische Feldstärke:
>
> $$\vec{B}(\vec{r}) = \frac{\mu_0}{4\pi} \frac{3(\vec{\mu}\vec{r})\vec{r} - r^2\vec{\mu}}{r^5}$$
>
> Berechnen Sie die Stärke des Magnetfeldes, welches ein Atom mit dem magnetischen Moment $\mu \cong \mu_\mathrm{B}$ am Ort eines Nachbar-Atoms erzeugt. Der für die Ferromagneten Fe, Ni und Co typische Abstand nächster Nachbarn $r_0$ kann aus den folgenden Angaben berechnet werden: Fe besitzt ein bcc-Gitter mit $a = 2,\!866~\mathrm{Å}$, Co ein hcp-Gitter mit $a = 2,\!507~\mathrm{Å}$ und Ni ein fcc-Gitter mit $a = 3,\!524~\mathrm{Å}$. Vergleichen Sie die maximale Energie der Dipol-Dipol-Wechselwirkung mit der thermischen Energie der Dipole bei der Curie-Temperatur, die für die genannten Materialien in der Größenordnung von $T_\mathrm{C}=1000~\mathrm{K}$ liegt.


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