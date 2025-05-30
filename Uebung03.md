<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.1
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

                                      {{1}}
Donatoren erzeugen einen [[ (n-Typ) | p-Typ ]] Halbleiter, bei dem die Fermi-Energie [[ (nahe des Leitungsbandes) | etwa mittig in der Bandlücke | nahe des Valenzbandes ]] liegt.

                                      {{2}}
Akzeptoren erzeugen einen [[ n-Typ | (p-Typ) ]] Halbleiter, bei dem die Fermi-Energie [[ nahe des Leitungsbandes | etwa mittig in der Bandlücke | (nahe des Valenzbandes) ]] liegt.

                                      {{3}}
Intrinsische Halbleiter enthalten [[ viele | (wenige) ]] Dotieratome, sodass die Fermi-Energie [[ nahe des Leitungsbandes | (etwa mittig in der Bandlücke) | nahe des Valenzbandes ]] liegt.


## Aufgabe 1 

> Für Indiumantimonid ist die Bandlücke $E_\mathrm{g} = 0,\!23~\mathrm{eV}$, die Dielektrizitätskonstante $\varepsilon_r = 18$, die effektive Masse der Elektronen $m_\mathrm{e}^\mathrm{eff} = 0,\!015\,m_0$. Berechnen Sie:
>
> a) die Ionisierungsenergie der Donatoren!
>
> b) den Bahnradius für den Grundzustand!
>
> c) Ab welcher Donatorkonzentration treten deutliche Überlappungseffekte zwischen den Bahnen benachbarter Fremdatome auf? Diese Überlappung kann ein Störstellenband erzeugen. Dies ist ein Energieband, das die elektrische Leitung durch den Sprung-mechanismus (*Hopping*) ermöglicht, bei dem Elektronen von einem Fremdatom auf ein benachbartes, ionisiertes Fremdatom springen.


                                      {{1}}
**a)** Aus dem Wasserstoffmodell eines Dotieratoms erhält man:
$$E_n = -\frac{1}{2} \frac{m^\mathrm{eff} e^4}{(4 \pi \varepsilon_0 \varepsilon_r \hbar)^2} \frac{1}{n^2}$$

                                      {{2}}
Für die Hauptquantenzahl wird $n=1$ eingesetzt. Die Ionisierungsenergie $E_\mathrm{D}$ entspricht der negativen Bindungsenergie, sodass man mit den gegebenen Werten erhält:
$$E_\mathrm{D} = -E_1 = 0,\!63~\mathrm{meV}$$

                                      {{3}}
**b)** Das Wasserstoffmodell ergibt weiterhin einen skalierten Bohrradius:
$$a_\mathrm{D} = \frac{4 \pi \varepsilon_0 \varepsilon_r \hbar^2}{m^\mathrm{eff} e^2}$$

                                      {{4}}
Mit den gegebenen Werten erhält man:
$$a_\mathrm{D} = 63,\!5~\mathrm{nm}$$

                                      {{5}}
**c)** Nimmt man kugelförmige Orbitale der Elektronen um die Donatoren an, erhält man die maximal mögliche Konzentration aus:
$$n_\mathrm{D} = \frac{1}{V} = \frac{1}{\frac{4}{3} \pi a_\mathrm{D}^3}$$

                                      {{6}}
Mit dem vorherigen Ergebnis erhält man:
$$n_\mathrm{D} = 9,\!3 \cdot 10^{14}~\mathrm{cm^{-3}}$$


## Aufgabe 2

> Lässt sich durch Messung des Hall-Effekts die Dichte $n_\mathrm{D}$ der Donatoren in einem n-Typ-Halbleiter bzw. die Dichte $n_\mathrm{A}$ der Akzeptoren in einem p-Typ-Halbleiter bestimmen? Wenn ja, in welchem Temperaturbereich muss die Messung stattfinden?

                                      {{1}}
Wenn die elektrische Leitfähigkeit nur von einer Ladungsträgerart bestimmt wird, also z. B. von Elektronen in einem n-dotierten Halbleiter, so kann der Hall-Koeffizient $R_\mathrm{H}$ aus der Ladungsträgerdichte $n$ und der Ladung $q$ berechnet werden:
$$R_\mathrm{H} = \frac{1}{q n}$$

                                      {{2}}
Für einen n-Typ-Halbleiter ist $q=-e$; für einen p-Typ-Halbleiter gilt $q = +e$. Aus der Messung des Hall-Koeffizienten $R_\mathrm{H}$ folgt also direkt die Ladungsträgerdichte $n$ gemäß:
$$n = \frac{1}{q R_\mathrm{H}}$$

                                      {{3}}
Aus einer temperaturabhängigen Messung von $R_\mathrm{H}$ erhält man somit den Temperaturverlauf von $n$. Dieser ist schematisch in der nachfolgenden Abbildung gezeigt:
![Temperaturverlauf der Ladungsträgerdichte $n$ und des chemischen Potenzials $\mu$ in einem dotierten n-Typ-Halbleiter](Bilder/Fermienergie_n-Typ_Temperatur.png "Temperaturverlauf der Ladungsträgerdichte $n$ und des chemischen Potenzials $\mu$ in einem dotierten n-Typ-Halbleiter. *Quelle: Rudolf Gross und Achim Marx, Vorlesungsskript Festkörperphysik, 2008*")

                                      {{4}}
Um die Dichte $n_\mathrm{D}$ der Donatoren in einem n-Typ-Halbleiter zu bestimmen, muss also die Ladungsträgerdichte $n$ im Bereich mittlerer Temperaturen (Störstellenerschöpfung) gemessen werden. In diesem Bereich gilt $n \approx n_\mathrm{D}$.

                                      {{5}}
Um die Dichte $n_\mathrm{A}$ der Akzeptoren in einem p-Typ-Halbleiter zu bestimmen, wird analog die Ladungsträgerdichte $n$ im Bereich mittlerer Temperaturen (Störstellenerschöpfung) gemessen. In diesem Bereich gilt $n \approx n_\mathrm{A}$.


## Aufgabe 3 

> Wie lassen sich durch Messung der Temperaturabhängigkeit des Hall-Koeffizienten die Energielücke $E_\mathrm{g}$ eines Halbleiters sowie bei einem n-Typ-Halbleiter der Abstand $E_\mathrm{d}$ des Donatorniveaus von der Leitungsbandkante bzw. bei einem p-Typ-Halbleiter der Abstand $E_\mathrm{a}$ des Akzeptorniveaus von der Valenzbandkante bestimmen?

                                      {{1}}
Aus einer temperaturabhängigen Messung des Hall-Koeffizienten $R_\mathrm{H}$ erhält man den Temperaturverlauf der Ladungsträgerdichte $n$ (siehe auch Aufgabe 2). Dieser ist schematisch in der nachfolgenden Abbildung gezeigt:
![Temperaturverlauf der Ladungsträgerdichte $n$ und des chemischen Potenzials $\mu$ in einem dotierten n-Typ-Halbleiter](Bilder/Fermienergie_n-Typ_Temperatur.png "Temperaturverlauf der Ladungsträgerdichte $n$ und des chemischen Potenzials $\mu$ in einem dotierten n-Typ-Halbleiter. *Quelle: Rudolf Gross und Achim Marx, Vorlesungsskript Festkörperphysik, 2008*")

                                      {{2}}
**Bei hohen Temperaturen** steigt $\ln n$ mit $-E_\mathrm{g} / (2 k_\mathrm{B} T)$ an. Aus dem Anstieg kann also direkt die Bandlücke $E_\mathrm{g}$ berechnet werden.

                                      {{3}}
**Bei niedrigen Temperaturen** (ohne Kompensation) steigt $\ln n$ mit $-E_\mathrm{d} / (2 k_\mathrm{B} T)$ an. Aus dem Anstieg kann bei einem n-Typ-Halbleiter also direkt das Donatorniveau $E_\mathrm{d}$ berechnet werden.

                                      {{4}}
**Für p-Typ-Halbleiter** steigt bei niedrigen Temperaturen (ohne Kompensation) die Ladungsträgerdichte $\ln n$ mit $-E_\mathrm{a} / (2 k_\mathrm{B} T)$ an. Aus dem Anstieg kann hier das Akzeptorniveau $E_\mathrm{a}$ berechnet werden.


## Aufgabe 4

> Betrachten Sie p-Typ Germanium mit einer Akzeptorkonzentration von $n_\mathrm{A} = {10}^{14}\, \mathrm{cm}^{-3}$ bei einer Temperatur von $T = 400\, \mathrm{K}$. Dominiert die intrinsche oder die extrinsische Leitfähigkeit? Folgende Werte für Germanium sind gegeben: $E_\mathrm{g} = 0,\!64 \, \mathrm{eV}$; $m_\mathrm{e}^\ast = 0,\!55 \, m_0$; $m_\mathrm{h}^\ast = 0,\!37 \, m_0$; $\mu_\mathrm{e} = 0,\!39 \, \mathrm{m^2/Vs}$; $\mu_\mathrm{h} = 0,\!19 \, \mathrm{m^2/Vs}$.

                                      {{1}}
Für den extrinsischen Fall nehmen wir an, dass alle Störstellen ionisiert vorliegen:
$$p \approx n_\mathrm{A} = {10}^{14}\, \mathrm{cm}^{-3} = 10^{20} \, \mathrm{m}^{-3}$$

                                      {{2}}
Die Minoritäten können näherungsweise vernachlässigt werden ($n \approx 0$). Für die Leitfähigkeit folgt:
$$\sigma = e p \mu_\mathrm{h} = 3,\!04 \, \mathrm{(\Omega m)^{-1}} = 0,\!0304 \, \mathrm{(\Omega cm)^{-1}}$$

                                      {{3}}
Für den intrinsischen Fall gilt gemäß Übung 2, Aufgabe 4:
$$n_i = p_i = 2 \left( \frac{k_\mathrm{B} T}{2 \pi \hbar^2} \right)^{3/2} \left( m_\mathrm{e}^\mathrm{eff} m_\mathrm{h}^\mathrm{eff} \right)^{3/4} \cdot \exp \left( - \frac{E_\mathrm{g}}{2 k_\mathrm{B} T} \right)$$
$$n_i = p_i = 1,\!09 \cdot 10^{21} \, \mathrm{m}^{-3} = 1,\!09 \cdot 10^{15} \, \mathrm{cm}^{-3}$$

                                      {{4}}
Für die Leitfähigkeit folgt hier:
$$\sigma = e(n \mu_\mathrm{e} + p \mu_\mathrm{h}) = 101 \, \mathrm{(\Omega m)^{-1}} = 1,\!01 \, \mathrm{(\Omega cm)^{-1}}$$

                                      {{5}}
Damit ist die intrinsische Leitfähigkeit deutlich höher und dominiert den Beitrag der Dotieratome.


## Aufgabe 5 

> Skizzieren Sie das Bandschema eines Schottky-Kontakts vor und nach dem Kontakt zwischen p-Typ Germanium ($\Phi_\mathrm{H} = 5,\!3 \, \mathrm{eV}$) und Silber ($\Phi_\mathrm{M} = 4,\!7 \, \mathrm{eV}$).
>
> a) Berechnen Sie die Breite der Raumladungszone für $n_\mathrm{A} = {10}^{14}\, \mathrm{cm}^{-3}$ und $\varepsilon_r = 16,\!6$.
>
> b) Berechnen Sie den Strom durch diesen Kontakt bei einer angelegten Spannung von $+1 \, \mathrm{V}$ und $-1 \, \mathrm{V}$, wenn $I_\mathrm{S} = 2,\!5 \, \mathrm{nA}$ und die Temperatur $T = 400\, \mathrm{K}$ betragen.


                                      {{1}}
Da $\Phi_\mathrm{H} > \Phi_\mathrm{M}$, ergibt sich folgendes Bandschema vor und nach dem Kontakt:
![Schematische Zeichnung der Energiebänder für ein Metall und einen p-Typ-Halbleiter](Bilder/metal_p-type.png "Energiebänder für ein Metall und einen p-Typ-Halbleiter (a) vor und (b) nach dem Kontakt. *Quelle: Rolf E. Hummel, Electronic Properties of Materials, Springer, 2011*")

                                      {{2}}
**a)** Die Breite der Raumladungszone berechnet sich folgendermaßen:
$$d = \sqrt{\frac{2 \varepsilon_0 \varepsilon_r}{e^2 n_\mathrm{A}} (\Phi_\mathrm{H} - \Phi_\mathrm{M})} = 3,\!3~\mathrm{µm}$$
Bei dieser Version der Formeln ist zu beachten, dass $\Phi_\mathrm{H}$ und $\Phi_\mathrm{M}$ in $\mathrm{eV}$ eingesetzt werden; sie gilt nur für Akzeptoren $n_\mathrm{A}$ und ohne äußere Spannung.

                                      {{3}}
**b)** Der Strom durch den Schottky-Kontakt wird mit Hilfe der Shockley-Gleichung berechnet:
$$I = I_\mathrm{S} \cdot \left[ \exp \left( \frac{e U}{k_\mathrm{B} T} \right) - 1 \right]$$

                                      {{4}}
Für die positive Spannung von $+1 \, \mathrm{V}$ ergibt sich ein sehr hoher Strom:
$$I(+1 \, \mathrm{V}) = 9938 \, \mathrm{A}$$

                                      {{5}}
Für die negative Spannung von $-1 \, \mathrm{V}$ fließt nur der Sperrstrom:
$$I(-1 \, \mathrm{V}) \approx -I_\mathrm{S} = -2,\!5 \, \mathrm{nA}$$


## Aufgabe 6 

> Es wird ein abrupter pn-Übergang ohne angelegte äußere Spannung betrachtet.
>
> a) Wie kommt es zur Bandverbiegung an diesem pn-Übergang?
>
> b) Was versteht man unter einer Raumladungszone?
>
> c) Skizzieren Sie qualitativ in drei Diagrammen den vom Ort abhängigen Verlauf der Ladungsträgerdichte, des elektrischen Feldes und des elektrostatischen Potentials über einen unsymmetrischen pn-Übergang.
>
> d) Welche Auswirkung hat eine äußere Spannung auf die Bandverbiegung des pn-Übergangs?


                                      {{1}}
**a)** Ein pn-Übergang entsteht, wenn ein p-dotiertes Halbleitermaterial (viele Löcher als Majoritätsträger) auf ein n-dotiertes Material (viele Elektronen als Majoritätsträger) trifft. Elektronen aus dem n-Gebiet **diffundieren** ins p-Gebiet, wo die Elektronenkonzentration viel geringer ist. Umgekehrt diffundieren Löcher vom p- ins n-Gebiet.

                                      {{2}}
Das obere Bild zeigt den p-n-Übergang vor der Diffusion, das untere nach Erreichen des Gleichgewichts:
![Schematische Zeichnung der Diffusion von Elektronen und Löchern an einem pn-Übergang](Bilder/Pn_Junction_Diffusion_and_Drift.svg "Darstellung der Diffusion von Elektronen und Löchern an einem pn-Übergang. *Quelle: [Wikipedia](https://en.wikipedia.org/wiki/Depletion_region#/media/File:Pn_Junction_Diffusion_and_Drift.svg)*")

                                      {{3}}
Dadurch bleiben im n-Gebiet (nahe der Grenzfläche) positiv geladene Donatoren zurück (weil die beweglichen Elektronen wegdiffundiert sind) und im p-Gebiet negativ geladene Akzeptoren (weil die Löcher wegdiffundiert sind). Diese zurückbleibenden Raumladungen erzeugen ein **internes elektrisches Feld** (von n nach p gerichtet). Das elektrische Feld wirkt der Diffusion entgegen. Nach kurzer Zeit stellt sich ein Gleichgewicht ein zwischen Diffusion (Teilchenbewegung) und Drift (Feldbewegung).

                                      {{4}}
Die **Bandverbiegung** spiegelt nun das elektrische Potential innerhalb der Sperrschicht wider. Die Energie eines Elektrons steigt, wenn es sich gegen ein elektrisches Feld bewegen muss. Daher liegt im n-Gebiet das Leitungsband tiefer (niedrige Elektronenenergie). Im p-Gebiet liegt das Leitungsband höher (hohe Elektronenenergie).

                                      {{5}}
**b)** Die **Raumladungszone** ist der Bereich am pn-Übergang, in dem keine freien Ladungsträger mehr vorhanden sind, sondern nur die ortsfesten Ionen, die das interne elektrische Feld und die Potential-Barriere aufbauen.

                                      {{6}}
**c)** Oben sind Löcher- und Elektronenkonzentration am pn-Übergang gezeigt, darunter die Ladungen, das elektrische Feld und das elektrische Potential:
![Schematische Zeichnung der Ladungsträgerkonzentration, der Ladungen, des elektrischen Feldes und des elektrischen Potentials an einem pn-Übergang](Bilder/Pn-junction-equilibrium-graphs.png "Darstellung der Ladungsträgerkonzentration, der Ladungen, des elektrischen Feldes und des elektrischen Potentials an einem pn-Übergang. *Quelle: [Wikipedia](https://en.wikipedia.org/wiki/Depletion_region#/media/File:Pn-junction-equilibrium-graphs.png)*")

                                      {{7}}
**d)** Durch eine äußere Spannung wird die Potentialbarriere entweder vergrößert (Sperr-Richtung) oder verkleinert (Durchlass-Richtung):
![Animation des Banddiagramms, des elektrischen Feldes und der elektrischen Ladung an einem pn-Übergang in Durchlass-Richtung](Bilder/PN_band.gif "Animation des Banddiagramms, des elektrischen Feldes und der elektrischen Ladung an einem pn-Übergang in Durchlass-Richtung: Bei einem pn-Übergang im Durchlassmodus nimmt die Breite der Raumladungszone ab. Sowohl der p- als auch der n-Übergang sind mit einem Dotierungsniveau von $10^{15} \, \mathrm{cm}^{-3}$ dotiert, was zu einem internen Potential von $\approx 0,\!59 \, \mathrm{V}$ führt. Gezeigt sind auch die unterschiedlichen Quasi-Fermi-Niveaus für das Leitungsband und das Valenzband im n- und p-Bereich (rote Kurven). *Quelle: [Wikipedia](https://en.wikipedia.org/wiki/Depletion_region#/media/File:PN_band.gif)*")