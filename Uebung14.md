<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.2
language: de
narrator: Deutsch Female
comment:  Struktur der Materie 2 - Übung 14

@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md
import: https://github.com/liascript/CodeRunner
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 14

                                      {{1}}
************************************
**Frage 1: Was kann die BCS-Theorie korrekt beschreiben?**

- [[X]] Existenz einer Energielücke
- [[ ]] Hochtemperatur-Supraleiter
- [[X]] Isotopeneffekt der Sprungtemperatur
- [[X]] Magnetische Flussquantisierung
- [[X]] Meißner-Ochsenfeld-Effekt
- [[X]] Wärmekapazitätssprung bei der Sprungtemperatur
************************************

                                      {{2}}
************************************
**Frage 2: Wie berechnet sich der Ginsburg-Landau-Parameter $\kappa$ aus Eindringtiefe $\lambda$ und Kohärenzlänge $\xi$?**

- [( )] $\kappa = \lambda \cdot \xi$
- [( )] $\kappa = \sqrt{\lambda \cdot \xi}$
- [(X)] $\kappa = \frac{\lambda}{\xi}$
- [( )] $\kappa = \frac{\xi}{\lambda}$
************************************


## Aufgabe 1

> Was sagt die BCS-Theorie für die Temperaturabhängigkeit der Wärmekapazität der Elektronen für Temperaturen unterhalb $T_\mathrm{C}$ voraus?

                                      {{1}}
Die spezifische Wärmekapazität bei tiefen Temperaturen folgt im Normalzustand einer $T^3$-Abhängigkeit für den phononischen Anteil und einem linearen Anstieg für den elektronischen Anteil. Dabei ist $\gamma$ der Sommerfeld-Koeffizient:
$$c_p = A T^3 + \gamma T$$

                                      {{2}}
In klassischen Supraleitern verringert sich die Wärmekapazität im supraleitenden Zustand exponentiell mit der Temperatur, da Cooper-Paare keine Wärme aufnehmen können und so nur noch Elektronen zur Wärmekapazität beitragen, die über die Energielücke angeregt werden. Die Wärmekapazität der Phononen (Gitterschwingungen) bleibt beim Übergang in den supraleitenden Zustand unverändert. Für Supraleiter gilt daher für den elektonischen Anteil unterhalb $T_\mathrm{C}$:
$$c_p \sim \exp \left(-\frac{\Delta(0)}{k_\mathrm{B} T} \right)$$

                                      {{3}}
Direkt bei der Sprungtemperatur $T_\mathrm{C}$ sagt die BCS-Theorie eine Zunahme der Wärmekapazität um folgenden Betrag voraus:
$$\frac{\Delta c_p}{\gamma T_\mathrm{C}} = 1,\!43$$

                                      {{4}}
Durch den Übergang in den normalleitenden Zustand ergibt sich bei $T_\mathrm{C}$ ein deutlicher Sprung im Verlauf der Wärmekapazität, der bei vielen Metallen entsprechend der Vorhersage der BCS-Theorie real beobachtet werden kann.


                                      {{5}}
![Temperaturverlauf der spezifischen Wärme von supraleitendem und normalleitendem Al](Bilder/Molare-Wärmekapazität.png "Temperaturverlauf der spezifischen Wärme von supraleitendem und normalleitendem Al. Um die spezifische Wärme im normalleitenden Zustand zu messen, wurde die Supraleitung mit einem äußeren Magnetfeld von $50~\mathrm{mT}$ unterdrückt (runde Symbole). Der Gitterbeitrag zur spezifischen Wärme ist in dem gezeigten Temperaturbereich vernachlässigbar klein. *Quelle: Rudolf Gross und Achim Marx, Vorlesungsskript Festkörperphysik, 2008*")


## Aufgabe 2

> Gallium ist ein BCS-Supraleiter mit schwacher Elektron-Phonon-Kopplung. Wie groß ist die supraleitende Energielücke (in $\mathrm{meV}$) bei diesem Element, wenn der Sprung in der spezifischen Wärme beim Übergang in den supraleitenden Zustand $78,\!29~\mathrm{mJ\,mol^{-1}\,K^{-1}}$ beträgt und der Sommerfeld-Koeffizient den Wert $7,\!5~\mathrm{mJ\,mol^{-1}\,K^{-2}}$ besitzt?

                                      {{1}}
Direkt bei der Sprungtemperatur $T_\mathrm{C}$ sagt die BCS-Theorie eine Zunahme der Wärmekapazität voraus (siehe Aufgabe 1):
$$\frac{\Delta c_p}{\gamma T_\mathrm{C}} = 1,\!43$$

                                      {{2}}
Mit den gegebenen Werten $\Delta c_p = 78,\!29~\mathrm{mJ\,mol^{-1}\,K^{-1}}$ und $\gamma = 7,\!5~\mathrm{mJ\,mol^{-1}\,K^{-2}}$ erhalten wir also die Übergangstemperatur:
$$T_\mathrm{C} = \frac{\Delta c_p}{1,\!43 \cdot \gamma} = 7,\!3~\mathrm{K}$$

                                      {{3}}
Für die supraleitende Energielücke folgt aus der BCS-Theorie weiterhin:
$$\Delta = 1,\!764 \cdot k_\mathrm{B} T_\mathrm{C} = 1,\!11~\mathrm{meV}$$


## Aufgabe 3

> Berechnen Sie für $T = 0~\mathrm{K}$ das zweite kritische Feld und den Ginzburg-Landau-Parameter eines Supraleiters, dessen Energielücke $0,\!62~\mathrm{meV}$ beträgt. Bei $T = 3~\mathrm{K}$ sind die Ginzburg-Landau-Kohärenzlänge $4,\!5~\mathrm{nm}$ und die Eindringtiefe $100~\mathrm{nm}$.

                                      {{1}}
Die Übergangstemperatur ist:
$$T_\mathrm{C} = \frac{\Delta}{1,\!764 \cdot k_\mathrm{B}} = 4,\!08~\mathrm{K}$$

                                      {{2}}
Die Kohärenzlänge bei $T = 0~\mathrm{K}$ ist:
$$\xi_\mathrm{GL}(0) = \xi_\mathrm{GL}(3~\mathrm{K}) \cdot \sqrt{1 - \frac{T}{T_\mathrm{C}}} = 2,\!31~\mathrm{nm}$$

                                      {{3}}
Die Eindringtiefe bei $T = 0~\mathrm{K}$ ist:
$$\lambda_\mathrm{GL}(0) = \lambda_\mathrm{GL}(3~\mathrm{K}) \cdot \sqrt{1 - \frac{T}{T_\mathrm{C}}} = 51,\!4~\mathrm{nm}$$

                                      {{4}}
Der Ginzburg-Landau-Parameter ist:
$$\kappa_\mathrm{GL} = \frac{\lambda_\mathrm{GL}(0)}{\xi_\mathrm{GL}(0)} = \frac{\lambda_\mathrm{GL}(3~\mathrm{K})}{\xi_\mathrm{GL}(3~\mathrm{K})} = 22,\!2$$

                                      {{5}}
Das zweite kritische Feld erhalten wir mit dem magnetischen Flussquant $\Phi_0 = 2,\!068 \cdot 10^{-15}~\mathrm{Vs}$ aus:
$$B_\mathrm{C,2} = \frac{\Phi_0}{2\pi \xi_\mathrm{GL}^2(0)} = 61,\!7~\mathrm{T}$$


## Aufgabe 4

> Temperatur- und feldabhängige Messungen des elektrischen Widerstands haben gezeigt, dass Nb<sub>3</sub>Ge bei $22,\!3~\mathrm{K}$ in den supraleitenden Zustand übergeht. Das kritische Feld $B_\mathrm{C,2}$ beträgt $7,\!3~\mathrm{T}$. Die direkte Messung der Eindringtiefe ergab $\lambda_\mathrm{L} = 2250~\mathrm{\AA}$. Die Energielücke wurde aus dem Verlauf der elektronischen spezifischen Wärme zu $\Delta = 5~\mathrm{meV}$ ermittelt. Zu welchem Supraleiter-Typ gehört Nb<sub>3</sub>Ge? Kann Nb<sub>3</sub>Ge als konventioneller BCS-Supraleiter betrachtet werden?

                                      {{1}}
Die Kohärenzlänge $\xi_\mathrm{GL}$ erhalten wir aus dem Zusammenhang mit dem kritischen Feld $B_\mathrm{C,2}$:
$$B_\mathrm{C,2} = \frac{\hbar}{q_\mathrm{S} \xi_\mathrm{GL}^2} = \frac{\Phi_0}{2 \pi \xi_\mathrm{GL}^2}$$

                                      {{2}}
Dabei beträgt die Ladung $q_\mathrm{S} = 2 e$ und die Konstante $\Phi_0$ ergibt sich aus $\Phi_0 = h / q_\mathrm{S} = 2,\!07 \cdot 10^{-15}~\mathrm{Vs}$. Die Ginzburg-Landau-Kohärenzlänge ist damit:
$$\xi_\mathrm{GL} = \sqrt{\frac{\Phi_0}{2 \pi B_\mathrm{C,2}}} = 6,\!7~\mathrm{nm}$$

                                      {{3}}
Das thermodynamische kritische Feld berechnet sich zu:
$$B_\mathrm{C,th} = \frac{\Phi_0}{2 \pi \sqrt{2} \cdot \xi_\mathrm{GL} \lambda_\mathrm{L}} = 0,\!15~\mathrm{T}$$

                                      {{4}}
Der Ginzburg-Landau-Parameter ergibt sich zu:
$$\kappa_\mathrm{GL} = \frac{\lambda_\mathrm{L}}{\xi_\mathrm{GL}} = \frac{B_\mathrm{C,2}}{\sqrt{2} \cdot B_\mathrm{C,th}} = 34 \gg \frac{1}{\sqrt{2}}$$
Damit handelt es sich bei Nb<sub>3</sub>Ge um einen Supraleiter vom **Typ II**.

                                      {{5}}
Das Energielückenverhältnis ist:
$$\frac{\Delta(0)}{k_\mathrm{B} T_\mathrm{C}} = 2,\!6 > 1,\!764$$
Damit ist Nb<sub>3</sub>Ge ein **unkonventioneller Supraleiter**.