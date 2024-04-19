<!--
author:   Hartmut Stöcker
email:    hartmut.stoecker@physik.tu-freiberg.de
version:  0.0.1
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


## Aufgabe 1

> Die magnetische Suszeptibilität eines kristallinen Materials kann bestimmt werden, indem eine zylindrische Probe an einem Balkenende der Gouy’schen Waage aufgehängt wird, die sich vor dem Versuchsbeginn im Gleichgewicht befindet. Das untere Ende der Probe wird in ein Magnetfeld gebracht. Um die Waage wieder ins Gleichgewicht zu bringen, muss ein Ausgleichsgewicht am anderen Balkenende aufgelegt werden.
>
> ![Schema der Gouy-Waage](Bilder/Gouy-Waage.png "Schema der Gouy-Waage. *Quelle: A. Armbrust, H. Janetzki, Aufgaben zur Festkörperphysik, 1999*") <!-- style = "width: 350px;" -->
>
> Berechnen Sie für eine zylindrische Probe mit dem Durchmesser $d = 2r = 5~\mathrm{mm}$, die in ein Magnetfeld der Stärke $H = 10^4~\mathrm{Oe}$ gebracht und mit einem Gegengewicht von $0,\!5~\mathrm{g}$ ausgeglichen wird, die magnetische Suszeptibilität. Um welche Form des Magnetismus handelt es sich?

                                      {{1}}
Die magnetische Energiedichte (auch als magnetischer Druck bezeichnet) berechnet sich aus:
$$w_\mathrm{mag} = \frac{1}{2} B H = \frac{1}{2 \mu_0 \mu_r} B^2 = \frac{\mu_0 \mu_r}{2} H^2$$

                                      {{2}}
Das Volumenintegral über $w_\mathrm{mag}$ ergibt die potentielle Energie $E_\mathrm{mag}$ des Magnetfeldes. Dieses Integral führen wir genau über das Volumen der ins Magnetfeld $H$ eingetauchten Probe aus. Wir nehmen an, dass zwischen den Polschuhen ein homogenes Magnetfeld $H$ wirkt, das nach außen sehr schnell abfällt. Mit der Querschnittsfläche $A = \pi r^2$ und der Eintauchtiefe $z$ der Probe ins Magnetfeld erhalten wir:
$$E_\mathrm{mag} = \int_V w_\mathrm{mag} \, \mathrm{d}V = \int_V \frac{\mu_0 \mu_r}{2} H^2 \, \mathrm{d}V = \frac{\mu_0 \mu_r}{2} H^2 \cdot \int_V \mathrm{d}V = \frac{\mu_0 \mu_r}{2} H^2 \cdot \pi r^2z$$

                                      {{3}}
Da das Magnetfeld bereits ohne Probe eine potentielle Energie besitzt, weil ja $\mu_{r,1} = 1$ gilt, müssen wir die Änderung der potentiellen Energie betrachten:
$$\Delta E_\mathrm{mag} = E_\mathrm{mag,2} - E_\mathrm{mag,1} = \frac{\mu_0}{2} (\mu_{r,2}-\mu_{r,1}) \cdot H^2 \cdot \pi r^2z$$

                                      {{4}}
Die relative Permeabilität $\mu_{r}$ hängt mit der gesuchten magnetischen Suszeptibilität $\chi$ über $\mu_{r} = 1 + \chi$ zusammen. Da für Luft $\mu_{r,1} = 1$ gilt, ist $\chi_1 = 0$ und insgesamt:
$$\Delta E_\mathrm{mag} = \frac{\mu_0}{2} (\chi_2-\chi_1) \cdot H^2 \cdot \pi r^2z = \frac{\mu_0 \chi_2}{2} \cdot H^2 \cdot \pi r^2z$$

                                      {{5}}
Wird die Probe entlang der Richtung $z$ verschoben, ergibt sich aus der dadurch hervorgerufenen Änderung der potentiellen Energie eine Kraft:
$$F = \frac{\mathrm{d} \Delta E_\mathrm{mag}}{\mathrm{d} z} = \frac{\mu_0 \chi_2}{2} \cdot H^2 \cdot \pi r^2$$

                                      {{6}}
Bereits im Jahr 1889 ist von Louis Georges Gouy vorgeschlagen worden, diese Kraft $F$ zu messen und daraus die magnetische Suszeptibilität $\chi_2$ einer Probe zu bestimmen. Die zylindrische Probe wird dabei an einer Waage hängend zwischen die Pole eines Magneten gebracht. Die durch das Magnetfeld $H$ hervorgerufene Kraft wird als Gewichtsänderung an der Waage registriert. Die Gegenkraft ist also die Gewichtskraft $F_G = mg$:
$$F = \frac{\mu_0 \chi_2}{2} \cdot H^2 \cdot \pi r^2 = mg$$

                                      {{7}}
Die gesuchte Größe erhalten wir also aus:
$$\chi_2 = \frac{2mg}{\mu_0 H^2 \pi r^2}$$

                                      {{8}}
Die Stärke des Magnetfeldes $H$ ist im CGS-System gegeben und muss zunächst umgerechnet werden. Es gilt:
$$1~\mathrm{Oersted} = 1~\mathrm{Oe} = \frac{1000}{4 \pi} \, \mathrm{\frac{A}{m}}$$

                                      {{9}}
Damit erhalten wir schließlich einen Wert von:
$$\chi_2 = 6,\!3 \cdot 10^{-4}$$

                                      {{10}}
Dieser Wert stellt eine einheitenlose Volumensuszeptibilität dar. Aufgrund des Vorzeichens (positiv) und der Größe des Wertes (zwischen $0$ und $1$) handelt es sich um eine paramagnetische Probe.

## Aufgabe 2 

> Skizzieren Sie mit Hilfe eines symbolischen Kästchenschemas die Besetzung der $\mathrm{4f}$-Orbitale im Grundzustand der Ionen Eu^2+^, Tb^3+^ und Yb^3+^. Wie lauten die entsprechenden Termbezeichnungen des Grundzustands in spektroskopischer Notation?

                                      {{1}}
***********************************
Alle genannten Elemente gehören zu den Lanthanoiden und haben damit eine abgeschlossene Xenon-Konfiguration, zwei Elektronen im Zustand $\mathrm{6s}$ sowie unterschiedlich viele $\mathrm{4f}$-Elektronen. 

![Periodensystem der Elemente](Bilder/Periodensystem-der-elemente_1280x720.png "Periodensystem der Elemente. *Quelle: https://www.joqora.de/blog/das-periodensystem-der-elemente *") <!-- style = "width: 600px;" -->
************************************

                                      {{2}}
************************************
Ausgehend vom voll besetzten Atom werden je nach Ionisationsgrad Elektronen entnommen. Bei der Besetzung beachten wir vor allem die 2. Hundsche Regel: „Der Gesamtspin $S$ nimmt den maximal möglichen Wert an, die Spins der einzelnen Elektronen $m_s$ stehen also möglichst parallel.“ Daraus ergibt sich:

| Ion    | Konfiguration                      | Kästchenschema für die $\mathrm{4f}$-Orbitale |
|--------|------------------------------------|----------------|
| Eu^2+^ | $\mathrm{[Xe] \, 6s^2 \, 4f^5}$    | $\fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{\phantom{↑↓}} \fbox{\phantom{↑↓}}$ |
| Tb^3+^ | $\mathrm{[Xe] \, 6s^2 \, 4f^6}$    | $\fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{\phantom{↑↓}}$  |
| Yb^3+^ | $\mathrm{[Xe] \, 6s^2 \, 4f^{11}}$ | $\fbox{↑↓} \fbox{↑↓} \fbox{↑↓} \fbox{↑↓} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}}$ |
************************************

                                      {{3}}
************************************
Für die Termbezeichnungen müssen wir die Quantenzahlen zuordnen:

- Gesamtspin $S = |\sum m_s|$: Ergibt sich aus der 2. Hundschen Regel, d. h. er nimmt den maximal möglichen Wert an.
- Gesamtbahndrehimpuls $L = |\sum m_l|$: Nach der 3. Hundschen Regel werden die Unterzustände mit der Magnetquantenzahl $m_l$ so besetzt, dass $L$ maximal wird.
- Gesamtdrehimpuls $J$: Folgt aus der 4. Hundschen Regel: Ist die Schale weniger als halbvoll, so ist $J=|L-S|$. Ist die Schale mehr als halbvoll, so ist $J=L+S$.
************************************

                                      {{4}}
************************************
Erläuterung zum Wert für $L$ nach der 3. Hundschen Regel: 

- Das erste Elektron einer neuen Schale erhält den maximalen Wert von $|m_l|=l$. Für eine $\mathrm{f}$-Schale ist $l=3$. 
- Das zweite Elektron darf wegen der 2. Hundschen Regel nicht denselben Wert für $m_l$ bekommen, da beide Elektronen bereits den gleichen Spin $m_s$ besitzen. Gemäß Pauli-Prinzip müssen die zwei Elektronen unterschiedliche Zustände einnehmen. Das 2. Elektron bekommt also den zweitgrößten Wert $|m_l|=l-1$. 
- Ist die Schale halbgefüllt, so müssen nach der 2. Hundschen Regel alle $m_l = -l, ..., +l$ einmal vergeben sein, d. h. $L$ ist dann gleich Null. 
- Bei der Befüllung der zweiten Hälfte der Schale werden die $m_l$ in der gleichen Reihenfolge wie bei Befüllung der ersten Hälfte vergeben.
************************************

                                      {{5}}
************************************
Beispiel Eu^2+^: 

- Das neutrale Eu-Atom hat 7 $\mathrm{4f}$-Elektronen. Das Eu^2+^-Ion hat entsprechend nur 5 $\mathrm{4f}$-Elektronen.
- Der Gesamtspin nimmt den maximal möglichen Wert $S = \frac{5}{2}$ an, wenn alle $m_s = +\frac{1}{2}$ parallel ausgerichtet sind.
- Die Bahndrehimpulse werden beginnend mit dem größten Wert $m_l=l=3$ an die einzelnen Elektronen verteilt. Die fünf Elektronen besitzen also die Werte $m_l = +3, +2, +1, 0, -1$. Der Gesamtbahndrehimpuls ist also $L = |\sum m_l| = 5$. 
- Da die Schale weniger als halbvoll ist, gilt $J=|L-S|=\frac{5}{2}$.
************************************

                                      {{6}}
************************************
Termbezeichnung: 

- Die spektroskopische Termbezeichnung folgt dem Schema: $^{2S+1}(L)_J$.
- Für $2S+1$ und $J$ werden direkt Zahlen eingesetzt, für $L$ kommen aufrechte Großbuchstaben zum Einsatz: $\mathrm{0 = S, 1 = P, 2 = D, 3 = F, 4 = G, 5 = H, 6 = I}$.
- Für das Beispiel Eu^2+^ ergibt sich also: $\mathrm{^6H_{5/2}}$
************************************

                                      {{7}}
************************************
Lösungsübersicht: 

| Ion    | Konfiguration                      | Kästchenschema | $S$ | $L$ | $J$ | Termsymbol |
|--------|------------------------------------|----------------|-----|-----|-----|------------|
| Eu^2+^ | $\mathrm{[Xe] \, 6s^2 \, 4f^5}$    | $\fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{\phantom{↑↓}} \fbox{\phantom{↑↓}}$ | $\frac{5}{2}$ | $5$ | $\frac{5}{2}$ | $\mathrm{^6H_{5/2}}$ |
| Tb^3+^ | $\mathrm{[Xe] \, 6s^2 \, 4f^6}$    | $\fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{\phantom{↑↓}}$  | $3$ | $3$ | $0$ | $\mathrm{^7F_0}$ |
| Yb^3+^ | $\mathrm{[Xe] \, 6s^2 \, 4f^{11}}$ | $\fbox{↑↓} \fbox{↑↓} \fbox{↑↓} \fbox{↑↓} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}} \fbox{↑\phantom{↓}}$ | $\frac{3}{2}$ | $6$ | $\frac{15}{2}$ | $\mathrm{^4I_{15/2}}$ |
************************************


## Aufgabe 3

> Berechnen Sie den Landé-Faktor $g$ und das effektive magnetische Moment der $\mathrm{4f}$-Ionen La^3+^, Pr^3+^ und Tb^3+^. Vergleichen Sie die Ergebnisse mit den experimentell ermittelten Werten.  Weshalb liefern abgeschlossene Schalen eines Atoms keinen Beitrag zum Langevin- Paramagnetismus?

                                      {{1}}
Ein magnetischer Dipol $\vec{\mu}_1$ erzeugt in seiner Umgebung die magnetische Feldstärke (siehe Aufgabe 4):
$$\vec{B}_1(\vec{r}) = \frac{\mu_0}{4\pi} \cdot \frac{3(\vec{\mu}_1 \vec{r})\vec{r} - r^2\vec{\mu}_1}{r^5}$$

                                      {{2}}
Der Betrag des Magnetfeldes $\vec{B}_1$ wird maximal, wenn $\vec{\mu}_1$ und $\vec{r}$ parallel ausgerichtet sind. Die Bedingung $\vec{\mu}_1 || \vec{r}$ bedeutet, dass das Magnetfeld auf einer Achse entlang des Vektors $\vec{\mu}_1$ betrachtet wird. Unter dieser Bedingung ist $(\vec{\mu}_1 \vec{r})\vec{r} = \vec{\mu}_1 r^2$ und die Formel für das Magnetfeld vereinfacht sich zu:
$$\vec{B}_1(\vec{r}) = \frac{\mu_0}{4\pi} \cdot \frac{3\vec{\mu}_1 r^2 - r^2\vec{\mu}_1}{r^5} = \frac{\mu_0}{4\pi} \cdot \frac{2\vec{\mu}_1 r^2}{r^5} = \frac{\mu_0}{2\pi} \cdot \frac{\vec{\mu}_1}{r^3}$$

                                      {{3}}
Befindet sich in diesem Magnetfeld $\vec{B}_1$ im Abstand $r_0$ ein zweiter Dipol $\vec{\mu}_2$, so besitzt er die potentielle Energie:
$$E_2 = - \vec{\mu}_2 \cdot \vec{B}_1 (r_0) = - \frac{\mu_0}{2\pi} \cdot \frac{\vec{\mu}_1 \vec{\mu}_2}{r_0^3}$$

                                      {{4}}
Gemäß Aufgabenstellung besitzen die beiden magnetischen Momente den Betrag $\mu_1 = \mu_2 = \mu_\mathrm{B} = 9,\!274\cdot 10^{−24}~\mathrm{A\,m^2}$ und den Abstand $r_0 = 3~\mathrm{Å} = 3 \cdot 10^{-10}~\mathrm{m}$. Damit ergibt sich der Betrag der potentiellen Energie zu:
$$|E_2| = 6,\!36 \cdot 10^{-25}~\mathrm{J} \approx 4~\mathrm{µeV}$$

                                      {{5}}
Durch thermische Anregung kann diese geringe Energiemenge leicht bereitgestellt werden, sodass die magnetische Dipolwechselwirkung gestört bzw. zerstört wird. Erst bei sehr niedrigen Temperaturen kann sie beobachtet werden. Da die thermische Energie $E_\mathrm{therm} = k_\mathrm{B} T$ ist, erhält man die Grenztemperatur aus:
$$T = \frac{|E_2|}{k_\mathrm{B}} = 0,\!064~\mathrm{K} < 100~\mathrm{mK}$$


## Aufgabe 4 

> Betrachten Sie als einfachsten Fall ein Zweiniveausystem, das wegen $J=½$ nur die zwei Energieniveaus $E = \pm ½ g μ_\mathrm{B} B_0$ annehmen kann. Berechnen Sie das mittlere magnetische Moment, welches sich in diesem Fall bei Anlegen eines magnetischen Feldes $B_0$ ergibt. Diskutieren Sie den Einfluss von Temperatur und Magnetfeld.

                                      {{1}}
************************************
Zunächst soll der Abstand der nächsten Nachbarn $r_0$ berechnet werden. Dieser hängt vom Strukturtyp und vom Gitterparameter ab:

![Strukturmodell des kubisch raumzentrierten Gitters (bcc) und Skizze der sich berührenden Atome entlang der Raumdiagonale](Bilder/Abstand_bcc.png "Strukturmodell des kubisch raumzentrierten Gitters (bcc) und Skizze der sich berührenden Atome entlang der Raumdiagonale. *Quelle: A. Armbrust, H. Janetzki, Aufgaben zur Festkörperphysik, 1999*")
![Strukturmodell des hexagonal dichtest gepackten Gitters (hcp) und Skizze der sich berührenden Atome](Bilder/Abstand_hcp.png "Strukturmodell des hexagonal dichtest gepackten Gitters (hcp) und Skizze der sich berührenden Atome. *Quelle: A. Armbrust, H. Janetzki, Aufgaben zur Festkörperphysik, 1999*")
![Strukturmodell des kubisch flächenzentrierten Gitters (fcc) und Skizze der sich berührenden Atome entlang der Flächendiagonale](Bilder/Abstand_fcc.png "Strukturmodell des kubisch flächenzentrierten Gitters (fcc) und Skizze der sich berührenden Atome entlang der Flächendiagonale. *Quelle: A. Armbrust, H. Janetzki, Aufgaben zur Festkörperphysik, 1999*")
************************************

                                      {{2}}
************************************
Gemäß der Abbildungen kann $r_0$ folgendermaßen berechnet werden:

| Material | Struktur | Formel für $r_0$     | Ergebnis             |
| -------- | -------- | -------------------- | -------------------- |
| Fe       | bcc      | $a/2 \cdot \sqrt{3}$ | $2,\!482~\mathrm{Å}$ |
| Co       | hcp      | $a$                  | $2,\!507~\mathrm{Å}$ |
| Ni       | fcc      | $a/2 \cdot \sqrt{2}$ | $2,\!492~\mathrm{Å}$ |
************************************

                                      {{3}}
Man erhält also, dass der Nächste-Nachbar-Abstand für alle drei betrachteten Materialien etwa $r_0 \approx 2,\!5~\mathrm{Å}$ beträgt. Die nachfolgende Rechnung wird also für alle drei Materialien das gleiche Ergebnis erbringen.

                                      {{4}}
Wie in Aufgabe 3 wird der Betrag des Magnetfeldes $\vec{B}$ maximal, wenn $\vec{\mu}$ und $\vec{r}$ parallel ausgerichtet sind. Unter dieser Bedingung vereinfacht sich die Formel für das Magnetfeld zu:
$$\vec{B}(\vec{r}) = \frac{\mu_0}{2\pi} \cdot \frac{\vec{\mu}}{r^3}$$

                                      {{5}}
Einsetzen der Werte $\mu \cong \mu_\mathrm{B} = 9,\!274\cdot 10^{−24}~\mathrm{A\,m^2}$ und $r_0 \approx 2,\!5~\mathrm{Å}$ ergibt:
$$B = 0,\!118~\mathrm{\frac{Vs}{Am}} \approx 0,\!12~\mathrm{T}$$

                                      {{6}}
Die maximale Energie der Dipol-Dipol-Wechselwirkung beträgt damit:
$$| E_\mathrm{mag} | = \vec{\mu} \cdot \vec{B} (r_0) = 1,\!1 \cdot 10^{-24}~\mathrm{J} \approx 6,\!9~\mathrm{µeV}$$

                                      {{7}}
Eine entsprechend große thermische Energie $E_\mathrm{therm} = k_\mathrm{B} T$ erhält man bereits bei:
$$T = \frac{|E_\mathrm{mag}|}{k_\mathrm{B}} = 80~\mathrm{mK}$$

                                      {{8}}
Für $T = T_\mathrm{C} = 1000~\mathrm{K}$ liegt die thermische Energie sogar bei $E_\mathrm{therm} = k_\mathrm{B} T_\mathrm{C} = 86~\mathrm{meV}$. Für $|E_\mathrm{mag}| = E_\mathrm{therm}$ müsste $B \approx 1500~\mathrm{T}$ sein. Die klassische Dipol-Dipol-Wechselwirkung kann also nicht beobachtet werden!