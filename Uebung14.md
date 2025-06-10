<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.1
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