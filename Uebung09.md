<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.0.1
language: de
narrator: Deutsch Female
comment:  Struktur der Materie 2 - Übung 09

@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md
import: https://github.com/liascript/CodeRunner
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 9


## Aufgabe 1

> Was sagen die Kramers-Kronig-Relationen aus und wozu werden sie verwendet?

                                      {{1}}
Die Kramers-Kronig-Relationen setzen Real- und Imaginärteil der dielektrischen Funktion in Form einer Integralgleichung miteinander in Beziehung. Auf diese Weise hängt die Absorption elektromagnetischer Wellen in einem Medium mit dem Brechungsindex zusammen. Es reicht also, die Abhängigkeit einer der beiden Größen von der Frequenz zu kennen, um die andere berechnen zu können.

                                      {{2}}
************************************
Mathematische Grundlage ist der Satz von Cauchy über komplexe analytische Funktionen unter den Bedingungen: 

- Die Funktion $f(x)$ hat in der oberen Halbebene keine Singularitäten.
- $f(x) \rightarrow 0$ für $x \rightarrow \infty$
- $\mathrm{Re}[f(x)]$ ist eine gerade Funktion
- $\mathrm{Im}[f(x)]$ ist eine ungerade Funktion
************************************

                                      {{3}}
Die Kramers-Kronig-Relationen haben die allgemeine Form:
$$\mathrm{Im}[f(x)] = -\frac{2}{\pi} \, \mathcal{P} \! \int_0^\infty \frac{x \cdot \mathrm{Re}[f(t)]}{t^2 - x^2} \, \mathrm{d}t$$
$$\mathrm{Re}[f(x)] = \frac{2}{\pi} \, \mathcal{P} \! \int_0^\infty \frac{t \cdot \mathrm{Im}[f(t)]}{t^2 - x^2} \, \mathrm{d}t$$
Dabei bezeichnet $\mathcal{P}$ den Cauchyschen Hauptwert des auftretenden Integrals.

                                      {{4}}
Für die dielektrische Funktion $\varepsilon' = \varepsilon_1 + \mathrm{i} \varepsilon_2$ gilt:
$$\chi(\omega) = \varepsilon_1(\omega) - 1 = \frac{2}{\pi} \, \mathcal{P} \! \int_0^\infty \frac{\omega' \cdot \varepsilon_2(\omega')}{\omega'^2 - \omega^2} \, \mathrm{d}\omega'$$
$$\varepsilon_2(\omega) = - \frac{2 \omega}{\pi} \, \mathcal{P} \! \int_0^\infty \frac{\varepsilon_1(\omega') - 1}{\omega'^2 - \omega^2} \, \mathrm{d}\omega'$$

                                      {{5}}
Eine wichtige Anwendung ist die Bestimmung von optischen Konstanten aus Reflexionsmessungen, wenn Transmissionsmessungen nicht möglich sind, z. B. oberhalb der Bandkante von Halbleitern.


## Aufgabe 2 

> Wie hängen die optischen Konstanten $n$ und $k$ vom Realteil $\varepsilon_1$ und Imaginärteil $\varepsilon_2$ der dielektrischen Funktion ab (Herleitung)?

                                      {{1}}
Die komplexe Dielektrizitätszahl eines Metalls im Infraroten kann näherungsweise dargestellt werden durch:
$$\varepsilon' = \mathrm{i} \frac{\sigma_0}{\varepsilon_0 \omega}$$

                                      {{2}}
Der komplexe Brechungsindex ist entsprechend:
$$n' = \sqrt{\varepsilon'} = \frac{1 + \mathrm{i}}{\sqrt{2}} \sqrt{\frac{\sigma_0}{\varepsilon_0 \omega}}$$

                                      {{3}}
Da der komplexe Brechungsindex als $n' = n + \mathrm{i} k$ darstellbar ist, folgt daraus:
$$n = k = \sqrt{\frac{\sigma_0}{2 \varepsilon_0 \omega}}$$

                                      {{4}}
Die Formel für den Reflexionskoeffizienten $R$ bei senkrechtem Einfall (aus Aufgabe 1) stellen wir zunächst etwas um:
$$R = \frac{(n - 1)^2 + k^2}{(n + 1)^2 + k^2} = \frac{(n + 1)^2 + k^2 - 4n}{(n + 1)^2 + k^2} = 1 - \frac{4n}{(n + 1)^2 + k^2}$$

                                      {{5}}
Für $n = k \gg 1$ können wir die $1$ im Nenner näherungsweise weglassen und den Zusammenhang folgendermaßen vereinfachen:
$$R \approx 1 - \frac{2}{n}$$

                                      {{6}}
Setzen wir die oben erhaltene Formel für $n$ ein, ergibt sich die Hagen-Rubens-Relation:
$$R \approx 1 - \sqrt{\frac{8 \varepsilon_0 \omega}{\sigma_0}}$$


## Aufgabe 3

> Welche verschiedenen Suszeptibilitätsanteile tragen zur dielektrischen Funktion von Stoffen bei?

                                      {{1}}
Zunächst rechnen wir die gegebenen Wellenlängen in Kreisfrequenzen um:
$$\omega = 2 \pi f = \frac{2 \pi c}{\lambda}$$


                                      {{2}}
Anschließend können wir direkt die Hagen-Rubens-Relation anwenden:
$$R \approx 1 - \sqrt{\frac{8 \varepsilon_0 \omega}{\sigma_0}}$$

                                      {{3}}
************************************
Für die zwei in der Aufgabenstellung genannten Wellenlängen erhalten wir:

<!-- data-type="none" -->
| Wellenlänge $\lambda$ | Kreisfrequenz $\omega$ | Reflexionskoeffizient $R$ |
|-----------------------|------------------------|---------------------------|
| $10~\mathrm{µm}$      | $1,\!88 \cdot 10^{14}~\mathrm{s^{-1}}$  | $0,\!980$ |
| $100~\mathrm{µm}$     | $1,\!88 \cdot 10^{13}~\mathrm{s^{-1}}$  | $0,\!994$ |
************************************

                                      {{4}}
Für sehr gute Leiter (z. B. Al, Cu, Ag) ist im IR-Bereich ein fast ideales Reflexionsvermögen nahe an $R=1$ zu beobachten.


## Aufgabe 4

> Beschreiben Sie den Verlauf der dielektrischen Funktion und den Verlauf des Reflexionsvermögens im Bereich der Plasmonenabsorption von Metallen.

                                      {{1}}
Die verallgemeinerte Permittivität setzt sich zusammen aus:
$$\varepsilon' = \varepsilon_1 + \mathrm{i} \varepsilon_2$$

                                      {{2}}
Der imaginäre Anteil $\varepsilon_2$ hängt direkt mit der Leitfähigkeit $\sigma$ zusammen:
$$\varepsilon_2 = \frac{\sigma}{\varepsilon_0 \omega}$$

                                      {{3}}
Andererseits kann der imaginäre Anteil $\varepsilon_2$ direkt aus den optischen Konstanten ermittelt werden:
$$\varepsilon_2 = 2 n k$$

                                      {{4}}
Gleichsetzen liefert eine Formel für die Leitfähigkeit:
$$\sigma = 2 n k \varepsilon_0 \omega = 2 n k \varepsilon_0 \cdot 2 \pi \frac{c}{\lambda}$$

                                      {{5}}
Mit den gegebenen Werten erhalten wir: $\sigma = 2,\!6 \cdot 10^4~\frac{1}{\mathrm{\Omega m}}$

                                      {{6}}
Der Literaturwert für die spezifische Leitfähigkeit von Kupfer (bei $\omega = 0$) liegt allerdings bei: $\sigma_0 = 5,\!8 \cdot 10^7~\frac{1}{\mathrm{\Omega m}}$

                                      {{7}}
Es ist wichtig, sich klar zu machen, dass eine klare Unterscheidung zwischen freien und gebundenen Ladungsträgern in zeitlich oszillierenden Feldern (z. B. für die Wellenlänge von $600~\mathrm{nm}$) nicht mehr möglich ist. In beiden Fällen haben wir es mit periodischen Verschiebungen von Ladungen zu tun. Nur für $\omega = 0$ können wir das Verhalten von freien und gebundenen Ladungen klar unterscheiden und eine Trennung von Phänomenen, die $\sigma$ bzw. $\varepsilon_2$ zugeordnet werden können, ist evident. Für zeitlich und räumlich variierende Felder ist dies dagegen nicht mehr möglich.


## Aufgabe 5

> Man bestimme den Zusammenhang zwischen Absorptionskoeffizient $\alpha$ und der Eindringtiefe $w$ einer ebenen elektromagnetischen Welle beim Eindringen in ein absorbierendes Medium. Die Eindringtiefe $w$ soll die Entfernung von der Oberfläche beschreiben, bei der die Intensität der Welle auf den Wert $\mathrm{1/e}$ abfällt.

                                      {{1}}
Die verallgemeinerte Permittivität setzt sich zusammen aus:
$$\varepsilon' = \varepsilon_1 + \mathrm{i} \varepsilon_2$$

                                      {{2}}
Das Reziproke ist:
$$\frac{1}{\varepsilon'} = \frac{\varepsilon_1 - \mathrm{i} \varepsilon_2}{\varepsilon_1^2 + \varepsilon_2^2}$$

                                      {{3}}
Der negative Imaginärteil dieser Funktion ist:
$$-\mathrm{Im}\left(\frac{1}{\varepsilon'}\right) = \frac{\varepsilon_2}{\varepsilon_1^2 + \varepsilon_2^2}$$

                                      {{4}}
Diese sogenannte „Energieverlustfunktion“ wird also maximal für $\varepsilon_1 \rightarrow 0$. Genau bei der Plasmafrequenz wird ebenfalls $\varepsilon_1 = 0$. Damit kennzeichnet ein Maximum in der Energieverlustfunktion gerade die Lage der Plasmafrequenz.
