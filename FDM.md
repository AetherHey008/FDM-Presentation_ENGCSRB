[![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://liascript.github.io/course/?https://raw.githubusercontent.com/AetherHey008/FDM-Presentation_ENGCSRB/refs/heads/main/FDM.md?token=GHSAT0AAAAAAD2BJYHDEVRZCXJRB653UFPG2PPQ2YQ)

#### FDM Printing

![](https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExODNlOGZna2xuN3M5bHV4cHl5NnM2b2Z1MDB3OHJ6ZDNzbWV6dnJjYiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/tKrpJSggdryRdJLfus/giphy.gif)<!--style="width: 100%; max-width: 80%;"-->

### What is 3D printing in gerneral?

In general 3D pritnign describes the process of constructing a three-dimensional object from a 3D-model (.obj, .stl, .cad , .3mf, .sldprt)



![](https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExeTU5bGtqcGVsY2oxajQ4MDI2ajk3N240MXp6ejQwcTk1eHc4aTZ6dSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/NPDydge3v69UIYtVCe/giphy.gif)<!--style="width: 100%; max-width: 80%;"-->



### Types of 3D Printers

||  Resin Printing (SLA/DLP/MSLA) 	|   Powder Printing (SLS/MJF)	|   Filament Printing (FDM/FFF)	|   Material Jetting (PolyJet)	|   Binder Jetting	| Metal 3D Printing (DMLS/SLM, EBM, DED, Bound Metal)   |
|Quick description| Resin 3D printers use a light source to cure liquid resin into hardened plastic in a process called photopolymerization.  	|SLS 3D printers use a high-power laser to sinter small particles of polymer powder into a solid structure.	| FDM 3D printers work by extruding thermoplastic filaments, such as ABS and PLA, through a heated nozzle, melting the material, and depositing it along programmed paths layer by layer on a build platform.	|Material jetting printers deposit tiny droplets of liquid photopolymer through arrays of inkjet nozzles and cure them instantly with UV light.	|Instead of melting powder layer by layer, a printhead deposits liquid binder to glue selected regions of powder into a “green” part while the surrounding powder acts as support.	|    |
||   	|   	|   	|   	|   	|     |
||  	|   	|   	|   	|   	|    |
|| 	|   	|   	|   	|   	|    |


### Im Fokus: Teamwork

Obwohl Einstimmigkeit darüber besteht, dass kooperative Arbeit für Ingenieure
Grundlage der täglichen Arbeitswelt ist, bleibt die Wissensvermittlung im Rahmen
der Ausbildung nahezu aus.

> __Frage:__ _Welche Probleme sehen Sie bei der Teamarbeit (kommaseparierte Stichpunkte)? _
>
>    [[___]]

                                    {{1-2}}
********************************************************************************

> **Spezifisches Ziel:** Wir wollen Sie für die Konzepte und Werkzeuge der
> kollaborativen Arbeit bei der Softwareentwicklung "sensibilisieren".
>
> - Wer definiert die Feature, die unsere Lösung ausmachen?
> - Wie behalten wir bei synchronen Codeänderungen der Überblick?
> - Welchen Status hat die Erfüllung der Aufgabe X erreicht?
> - Wie können wir sicherstellen, dass Code in jedem Fall kompiliert und Grundfunktionalitäten korrekt ausführt?
> - ...

********************************************************************************

### Warum das Ganze (Big Picture)? 

> Anhand der Veranstaltung entwickeln Sie ein "Gefühl" für guten und schlechten
> Codeentwürfen und hinterfragen den Softwareentwicklungsprozess.

      {{1-2}}
********************************************************************************

**Beispiel 1: Mariner 1 Steuerprogramm-Bug (1962)**

![An Atlas-Agena 5 carrying the Mariner 1 spacecraft](./img/00_Einleitung/Atlas_Agena_with_Mariner_1.jpg "wikimedia, Autor: NASA, [Link](https://de.wikipedia.org/wiki/Datei:Atlas_Agena_with_Mariner_1.jpg)")

Mariner 1 ging beim Start am 22. Juli 1962 durch ein fehlerhaftes Steuerprogramm verloren, als die Trägerrakete vom Kurs abkam und 293 Sekunden nach dem Start gesprengt werden musste. Ein Entwickler hatte einen Überstrich in der handgeschriebenen Spezifikation eines Programms zur Steuerung des Antriebs übersehen und dadurch statt geglätteter Messwerte Rohdaten verwendet, was zu einer fehlerhaften und potenziell gefährlichen Fehlsteuerung des Antriebs führte.

> **Potentieller Lösungsansatz**: Testen & Dokumentation

********************************************************************************

      {{2}}
********************************************************************************

**Beispiel 2: Toll-Collect On-Board-Units (2003)**

Das Erfassungssystem für die Autobahngebühren für Lastkraftwagen sollte ursprünglich zum 31. August 2003 gestartet werden. Nachdem die organisatorischen und technischen Mängel offensichtlich geworden waren, erfolgte eine mehrfache Restrukturierung. Seit 1. Januar 2006 läuft das System, mit einer Verzögerung von über zwei Jahren, mit der vollen Funktionalität. Eine Baustelle war die On-Board-Units (OBU), diese konnte zunächst nicht in ausreichender Stückzahl geliefert und eingebaut werden, da Schwierigkeiten mit der komplexen Software der Geräte bestanden.

Die On-Board-Units des Systems

- reagierten nicht auf Eingaben
- ließen sich nicht ausschalten
- schalteten sich grundlos aus
- zeigten unterschiedliche Mauthöhen auf identischen Strecken an
- wiesen Autobahnstrecken fehlerhaft als mautfrei/mautpflichtig aus

> **Potentieller Lösungsansatz**: vollständige Spezifikation, Testen auf Integrationsebene, Projektkoordination

*******************************************************************************

### Warum das Ganze (Detail)? 

> __Das nachfolgende Beispiel sollte Ihnen bekannt sein. Welchen Vorteil bringt eine Lösung in Form eines Python Skripts?__

> Gegeben ist ein gleichschenkliges Stabwerk. Dieses besteht aus Stäben $s1$, $s2$ und $s3$ mit den Knoten $A(0,0)$, $B(1,1.5)$ und $C(2,0)$. Dabei ist Knoten $A$ ein Festlager und Knoten $C$ ein Loslager. Im folgenden ist das Stabwerk maßstäblich dargestellt mit der $x$-Achse in horizontaler Richtung und der $y$-Achse in vertikaler Richtung:
> 
> ![alt text](./img/00_Einleitung/stabwerk_aufgabe.png)<!--style="width: 100%; max-width: 30vh;"-->
> 
> Im Knoten $B$ greift eine Kraft $\boldsymbol{F}$ an mit den Komponenten $\boldsymbol{F} = [-1, -1]\,\text{N}$.
>
> __Aufgaben__
>
> 1. Leiten Sie aus der Skizze das lineare Gleichungssystem der Form $\boldsymbol{A} \cdot \boldsymbol{x} = \boldsymbol{b}$ her, welches das gezeigte Fachwerk beschreibt und tragen Sie es hier ein. Dabei steht der Lösungsvektor $\boldsymbol{x}$ für die Stab- und Lagerkräfte im Stabwerk.
> 2. Berechnen Sie die Stab- und Lagerkräfte mit Hilfe der Numpy-Funktion [`numpy.linalg.solve`](https://numpy.org/doc/stable/reference/generated/numpy.linalg.solve.html), welche direkt ein System von linearen Gleichungssystemen iterativ lösen kann. Geben Sie die berechneten Kräfte formatiert aus.

Insgesamt gibt es in dieser Aufgabe 6 unbekannte Größen: Die Stabkräfte $F_{s1}$, $F_{s2}$ und $F_{s3}$, die Lagerkräfte im Knoten $A$ in $x$- und $y$-Richtung $F_{Ax}$ und $F_{Ay}$ sowie die Lagerkraft im Knoten $C$ in $y$-Richtung $F_{Cy}$. Daher müssen ebenfalls 6 Gleichungen aufgestellt werden, um die gesuchten Größen berechnen zu können.

Diese 6 Gleichungen erhält man, indem man in den drei Knotenpunkten jeweils das Kräftegleichgewicht in $x$- und $y$-Richtung aufstellt. Beispielhaft soll dieses Vorgehen am Knoten $A$ erläutert werden. In folgender Abbildung sind die Stabkräfte $F_{s1}$ und $F_{s2}$ sowie die Lagerkräfte am Knoten $A$ angezeichnet:

![alt text](./img/00_Einleitung/stabwerk_erlaeuterung.png)

Die zwei Kräftegleichgewichte in $x$- und $y$-Richtung lauten dann wie folgt:

$$ \begin{align*} F_{s1} \cos{\alpha} + F_{s3} + F_{Ax}&= 0 \\ F_{s1} \sin{\alpha} + F_{Ay} &= 0 \end{align*} $$

Analog werden die Kräftegleichgewichte in den Knotenpunkten $B$ und $C$ gebildet. Anschließend können die Koeffizienten für die Koeffizientenmatrix und der konstante Vektor aufgestellt werden.

#### Schritt 1: Modellierung

Für alle 6 Gleichungen in den Knoten $A$, $B$ und $C$ gilt:

$$ \begin{align*} F_{s1} \cos{\alpha} + F_{s3} + F_{Ax} &= 0 \\ F_{s1} \sin{\alpha} + F_{Ay} &= 0 \\ -F_{s1} \sin{\frac{\alpha}{2}} + F_{s2} \sin{\frac{\alpha}{2}} - F_x &= 0 \\ -F_{s1} \cos{\frac{\alpha}{2}} - F_{s2} \cos{\frac{\alpha}{2}} - F_y &= 0 \\ - F_{s2} \cos{\alpha} - F_{s3}  &= 0 \\ F_{s2} \sin{\alpha} + F_{Cy} &= 0\end{align*}$$


Daraus kannn das linearen Gleichungssystem mit Koeffizientenmatrix $\boldsymbol{A}$ und konstantem Vektor $\boldsymbol{b}$ abgeleitet werden:

$$ \begin{pmatrix} \cos{\alpha} & 0 & 1 & 1 & 0 & 0 \\ \sin{\alpha} & 0 & 0 & 0 & 1 & 0 \\ -\sin{\frac{\beta}{2}} & \sin{\frac{\beta}{2}} & 0 & 0 & 0 & 0 \\ -\cos{\frac{\beta}{2}} & -\cos{\frac{\beta}{2}} & 0 & 0 & 0 & 0 \\ 0 & -\cos{\alpha} & -1 & 0 & 0 & 0 \\ 0 & \sin{\alpha} & 0 & 0 & 0 & 1\end{pmatrix} \cdot \begin{pmatrix} F_{s1} \\ F_{s2} \\ F_{s3} \\ F_{Ax} \\ F_{Ay} \\ F_{Cy} \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ F_x \\ F_y \\ 0 \\ 0 \end{pmatrix} $$

Die Winkel $\alpha$ und $\beta$ können mit Hilfe des Arkustangens und der geometrischen Abmessungen direkt bestimmt werden:

$$ \begin{align*} \alpha &= \arctan{\frac{1.5}{1}} \approx 56{,}31^\circ \\ \beta &= 180^\circ - 2\,\alpha \approx 67{,}38^\circ \end{align*} $$

#### Schritt 2: Transformation

```python CalcSolution.py
# Laden der Module
import numpy as np

# Berechnung der Winkel
alpha = np.arctan(1.5/1)
beta = np.pi - 2*alpha

# Komponenten des Kraftvektors
Fx = -1
Fy = -1

# Koeffizientenmatrix
A = np.array([
    [np.cos(alpha), 0, 1, 1, 0, 0],
    [np.sin(alpha), 0, 0, 0, 1, 0],
    [-np.sin(0.5*beta), np.sin(0.5*beta), 0, 0, 0, 0],
    [-np.cos(0.5*beta), -np.cos(0.5*beta), 0, 0, 0, 0],
    [0, -np.cos(alpha), -1, 0, 0, 0],
    [0, np.sin(alpha), 0, 0, 0, 1]]
    )

b = np.array([0, 0, Fx, Fy, 0, 0])
x = np.linalg.solve(A, b)

print(f"Die Kräfte im Stabwerk sind wie folgt:")
print(f"    Stabkraft 1 = {x[0]:.3f} N")
print(f"    Stabkraft 2 = {x[1]:.3f} N")
print(f"    Stabkraft 3 = {x[2]:.3f} N")
print(f"    Lagerkraft Ax = {x[3]:.3f} N")
print(f"    Lagerkraft Ay = {x[4]:.3f} N")
print(f"    Lagerkraft Cy = {x[5]:.3f} N")
```
@LIA.eval(`["main.py"]`, `none`, `python3 main.py`, `*`)

#### Schritt 3: Analyse

Ein entscheidender Vorteil der skriptbasierten Lösung wird sichtbar, sobald wir die Eingangsgrößen variieren wollen. Im folgenden Beispiel wird $F_x$ im Bereich $[-5, 5]\,\text{N}$ durchlaufen (bei konstantem $F_y = -1\,\text{N}$) und die resultierende Stabkraft $F_{s1}$ aufgetragen.

> **Hinweis:** Da die Koeffizientenmatrix $\boldsymbol{A}$ nur von der Geometrie abhängt und der Vektor $\boldsymbol{b}$ linear in $F_x$ ist, ist auch die Lösung $\boldsymbol{x} = \boldsymbol{A}^{-1} \boldsymbol{b}$ **linear** in $F_x$. Die resultierende Kurve ist also eine Gerade — ein erster Hinweis auf den linearen Charakter des Modells.

```python ParameterStudy.py
import numpy as np
import matplotlib.pyplot as plt

alpha = np.arctan(1.5/1)
beta = np.pi - 2*alpha
Fy = -1

A = np.array([
    [np.cos(alpha), 0, 1, 1, 0, 0],
    [np.sin(alpha), 0, 0, 0, 1, 0],
    [-np.sin(0.5*beta), np.sin(0.5*beta), 0, 0, 0, 0],
    [-np.cos(0.5*beta), -np.cos(0.5*beta), 0, 0, 0, 0],
    [0, -np.cos(alpha), -1, 0, 0, 0],
    [0, np.sin(alpha), 0, 0, 0, 1]]
    )

Fx_range = np.linspace(-5, 5, 101)
Fs1 = np.zeros_like(Fx_range)

for i, Fx in enumerate(Fx_range):
    b = np.array([0, 0, Fx, Fy, 0, 0])
    x = np.linalg.solve(A, b)
    Fs1[i] = x[0]

plt.figure(figsize=(7, 4))
plt.plot(Fx_range, Fs1, label=r"$F_{s1}(F_x)$")
plt.axhline(0, color="gray", linewidth=0.5)
plt.axvline(0, color="gray", linewidth=0.5)
plt.xlabel(r"$F_x$ in N")
plt.ylabel(r"$F_{s1}$ in N")
plt.title(r"Stabkraft $F_{s1}$ in Abhängigkeit von $F_x$ (bei $F_y=-1\,$N)")
plt.grid(True)
plt.legend()
plt.tight_layout()
plt.savefig("Fs1_vs_Fx.png", dpi=120)
print("Plot gespeichert als Fs1_vs_Fx.png")
```
@LIA.eval(`["main.py"]`, `none`, `python3 main.py`, `*`)

       | 15. Mai   | Anwendungsbeispiel **TODO** Godot?                |                   |
| 7     | 18. Mai   | Versionsmanagement im SWE-Prozess I               | gemeinsam<!-- class="icon-joined" -->          |
|       | 22. Mai   | Versionsmanagement im SWE_Prozess II             | gemeinsam<!-- class="icon-joined" -->          |
| 8     | 25. Mai   | _Pfingstmontag_<!-- class="holiday icon-pentecoste" -->                                    |   _Pfingstmontag_<!-- class="holiday icon-pentecoste" -->  |
|       | 29. Mai   | UML Konzepte                                      | gemeinsam<!-- class="icon-joined" -->          |
| 9     | 01. Juni  | UML Diagrammtypen                                 | gemeinsam<!-- class="icon-joined" -->          |
|       | 05. Juni  | Anwendung und Fehlerfälle von KI                  | gemeinsam<!-- class="icon-joined" -->          |
| 10    | 08. Juni  | Generics                                          |                   |
|       | 12. Juni  | Container                                         |                   |
| 11    | 15. Juni  | Dokumentation und Build Toolchains                |                   | 
|       | 19. Juni  | Delegaten                                         |                   |
| 12    | 22. Juni  | Events                                            |                   |
|       | 26. Juni  | Threadkonzepte in C#                              |                   |
| 13    | 29. Juni  | Taskmodell                                        |                   |
|       | 03. Juli  | Testen                                            |                   |
| 14    | 06. Juli  | Continuous Integration in GitHub                  |                   |
|       | 10. Juli  | Design Pattern                                    |                   |
| 15    | 13. Juli  | Language Integrated Query                         |                   |
|       | 17. Juli  | GUI - MAUI                                        |                   |



### Durchführung

     {{0-1}}
************************************************************************

Die Vorlesung findet

- Montags,  18:00 - 19:30
- Freitags, 08:00 - 09:30

im Audimax 1001 (**SWE**) und in KKB-2030 (**Einführung in SWE**) statt,

> Achten Sie im Zeitplan auf die mit "gemeinsam" gekennzeichneten Termine, die wir hier im Audimax übergreifend anbieten.

Die Materialien der Vorlesung sind als Open-Educational-Ressources konzipiert
und stehen unter Github bereit.

https://github.com/TUBAF-IfI-LiaScript/VL_Softwareentwicklung

https://tubaf-ifi-liascript.github.io/softwareentwicklung.html

> Wie können Sie sich einbringen?
>
> * __Beiträge während der Vorlesungen__ ... Bringen Sie, soweit möglich Ihren Rechner mit. Wir bemühen uns die Inhalte in starkem Maße interaktiv zu gestalten.
>
> * __Allgemeine theoretische Fragen/Antworten__ ... Dabei können Sie sich über
>   github/ das Opal-Forum in die Diskussion einbringen.
>
> * __Rückmeldungen/Verbesserungsvorschläge zu den Vorlesungsmaterialien__ ...
>   _"Das versteht doch keine Mensch! Ich würde vorschlagen ..."_ ...
>   dann korrigieren Sie uns. Alle Materialien sind Open-Source. Senden Sie mir
>   einen Pull-Request und werden Sie Mitautor.

************************************************************************

     {{1-2}}
************************************************************************

Die Übungen bestehen aus selbständig zu bearbeitenden Aufgaben, wobei einzelne
Lösungen im Detail besprochen werden. Wir werden die Realisierung der Übungsaufgaben
über die Plattform [GitHub](https://github.com/) abwickeln.

> Wie können Sie sich einbringen?
>
> * __Allgemeine praktische Fragen/Antworten__ ... in den genannten Foren bzw.
>   in den Übungsveranstaltungen
>
> * __Eigene Lösungen__ ... Präsentation der Implementierungen in den Übungen
>
> * __Individuelle Fragen__ ... an die Übungsleiter per Mail oder in einer
>   individuellen Session

Für die Übungen  werden wir Aufgaben vorbereiten, mit denen die Inhalte der Vorlesung vertieft werden. 

> Hinweis auf das Agententeam und den damit einhergehenden Versuch während des Semester.

************************************************************************
