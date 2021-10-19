---
title: Stand der Forschung
fignos-cleveref: True
fignos-plus-name: Fig.
header-includes: \usepackage{subcaption}
...

# Stand der Forschung
Im folgenden Teil wird ein Überblick über den aktuellen Stand der Forschung gegeben. Dabei wird auf die Grundlagenforschung eingegangen, welche bereits in den 1960er Jahren ihren Ursprung fand. Ferner werden Visualisierungsmethoden beleuchtet, welche während der Pandemie vertreten waren. Es wird eine Konferenz vorgestellt, auf der jährlich Erkenntnisse bezüglich der Forschung zum Thema Visualisierung diskutiert werden. Abschließend wird eine relativ neue Forschungsdisziplin präsentiert, welche sich mit dem Thema "Big Data" und Visualisierung auseinander setzt.

## Grundlagen
Der Einfluss der menschlichen Wahrnehmung auf Visualisierungen ist ein wichtiger Faktor zur Verbesserung des Datenverständnisses. Bereits 1962 hat der Forscher Bela Julész Experimente mit grafischen Mustern durchgeführt (vgl. [@julesz_visual_1962]). In seinem Experiment hat er nach Kriterien gesucht, welche eine visuelle Diskriminierung von Grafiken ermöglichen. Diskriminierung definiert er als "[...] spontaneous visual process which gives the immediate impression of two distinct fields. " ([@julesz_visual_1962]). Seine Probanden konnten im Ergebnis primär zwischen Clustern oder Linien unterscheiden, welche sich durch Helligkeitsunterschiede oder räumliche Nähe diskriminieren ließen (vgl. [@julesz_visual_1962]). Visualisierungen lassen sich also mit Hilfe von Helligkeitsunterschieden oder Gruppierungen so optimieren, dass diese für den Betrachter leicht zu erkennen sind.

Treisman untersucht 1977 ein Phänomen, bei dem die Probanden sich auf gezeigte Buchstaben konzentrieren sollten, welche gleichzeitig auch mit Zahlen umgeben wurden (z.B. 1 K P D 2). Die Teilnehmer sollten nun zunächst die Form, Farbe und Position der Zahlen berichten und anschließend die der Buchstaben. Dabei fiel auf, dass die Probanden die Merkmale vertauschten, also beispielhaft statt eines roten K ein blaues K berichteten. Dieses Phänomen nennt Treisman die illusionäre Konjunktion, welche auch die Grundlage der "Feature Integration Theorie" bildet. Es benötigt selektive Aufmerksamkeit um Merkmale zu diskriminieren. Gibt es nicht genug Zeit für die Verarbeitung von visuellen Eindrücken, so können die interpretierten Objekte falsche Bindungen eingehen (vgl. [@treisman_focused_1977]).
Mit der "Feature Integration Theory" hat Treisman eine Theorie veröffentlicht und Experimente durchgeführt, die sich mit dem Thema Aufmerksamkeit beschäftigen. Welche Faktoren spielen hierbei eine Rolle? In ihrem Paper "A Feature-Integration Theory of Attention" hat Sie 1980 in einigen Experimenten herausgefunden, dass es einen seriellen Engpass in der visuellen Verarbeitung gibt. Verschiedene Merkmale des visuellen Inputs können zwar gleichzeitig aufgenommen werden, aber die Interpretation einzelner Objekte nur seriell erfolgen (vgl. [@treisman_feature-integration_1980], S. 132).

\begin{center}
  \includegraphics[width=.3\linewidth]{source/figures/fig-2-1.png}
  \captionof{figure}{Ein Beispiel zur Demonstration des "Pop Out Effekts" (Wikimedia, 2021)}
  \label{fig:2-1}
\end{center}

Ein weiteres interessantes Phänomen in der visuellen Wahrnehmung des Menschen ist die präattentive Wahrnehmung. Präattentive Wahrnehmung lässt sich am einfachsten mit dem "pop-out effect" umschreiben. Rote Früchte an eine grünen Apfelbaum werden im Bewusstsein sofort als solche wahrgenommen. Ein gutes Beispiel dafür ist @fig:2-1.

Anne Treisman ist auch hier eine der ersten Wissenschaftlerinnen, die eine Theorie dazu veröffentlich haben. In ihrem Paper "Preattentive Processing in Vision" unterscheidet sie zwischen zwei Funktionen der visuellen Wahrnehmung: Einerseits gibt es eine vorgeschaltete, parallele Wahrnehmung, welche einfache Merkmale ohne bewusste Aufmerksamkeit wahrnehmen und verarbeiten kann. Andererseits gibt es einen späteren Verarbeitungsprozess, bei dem bewusste Aufmerksamkeit nötig ist (vgl. [@treisman_preattentive_1985]). Treisman stellt die Theorie auf, dass es eine "master map of locations" geben muss, welche die Aufmerksamkeit mit Hilfe von verschiedenen Merkmalskarten wie Farbe, Orientierung oder Textur an ein Objekt bindet. Die verschiedenen Merkmalskarten können parallel abgefragt werden, während die genaue Lokalisierung eines Objektes bewusste Aufmerksamkeit erfordert. (vgl. [@treisman_preattentive_1985]).

\begin{center}
  \includegraphics[width=.5\linewidth]{source/figures/fig-2-2.png}
  \captionof{figure}{Auszug einer diskriminierbaren Textur nach Julész. (B. Julesz, Gilbert, \& Victor, 1978, S. 138, Fig. 3)}
  \label{fig:2-2}
\end{center}

Der Wissenschaftler Bela Julész führte noch weitere Versuche mit Texturen durch, welche die Probanden diskriminieren mussten (vgl. [@julesz_inability_1973]; [@julesz_visual_1978]). Er untersuchte dabei, ob Variationen in den Texturen durch das Unterbewusstsein wahrgenommen wurden oder nicht (vgl. @fig:2-2). Seine Ergebnisse waren dabei nicht ganz schlüssig, da unterschiedliche Kontraste zwar präattentiv wahrgenommen wurden, bei Variation von Orientierung und Regelmäßigkeit ließ sich die präattentive Wahrnehmung aber nur teilweise nachweisen (vgl. [@healey_attention_2012], S. 1173). Er modifiziert daraufhin seine Theorie der "Textons, the elements of texture perception and their interactions" (vgl. [@julesz_textons_1981]) und definiert eine Gruppe von Merkmalen, welche durch die präattentive Verarbeitung wahrgenommen werden, die Textons. Dies sind primär Merkmale der "first-order statistics", also Kontraste. Julész definiert drei Klassen für Textons:

> 1. "Elongated blobs" - zum Beispiel Rechtecke oder Linien mit bestimmten Eigenschaften wie Farbton, Orientierung oder Größe
  2. "Terminators" - Segmente, die das Ende einer Linie bilden
  3. "Crossing of line segments" - Segmente, die eine Linie von anderen Segmenten unterbrechen
(vgl. [@julesz_textons_1981], [@healey_attention_2012], S. 1173)

Colin Ware führte 1988 Experimente mit Farbsequenzen durch um den Einfluss von Farben näher zu erforschen. Insgesamt führte er drei verschiedene Experimente mit 5 verschiedenen Farbskalen durch (vgl. [@ware_color_1988], S. 43). Hierzu mussten die Probanden mit Hilfe eines Farbwählers die Farbe treffen, welche ihnen gezeigt wurde (vgl. [@ware_color_1988], S. 43). Unter den Farbsequenzen waren unter anderem verschiedene Grautöne, eine Sättigungsskala und ein Farbspektrum zwischen zwei Farben. Im ersten Experiment wurde die Fehlerrate gemessen, mit welcher die Probanden die Farben unterschieden. Hierbei hatte das Farbspektrum mit zwei Farben die geringste Fehlerquote (vgl. [@ware_color_1988], S. 44).

Rogowitz und Treinish haben in einem Paper zwei Klassen von Regeln definiert, welche für den Visualisierungsprozess von Daten wichtig sind: Klasse 1 Regeln stellen sicher, dass die Struktur der Daten sich in der Visualisierung wieder findet. Bei Klasse 2 Regeln wird die Struktur der Daten transformiert, um gezielt Aufmerksamkeit zu lenken, Details zu unterstreichen oder die Daten in bestimmte Regionen einzuteilen (vgl. [@rogowitz_architecture_1993]).

## Visualisierungen während der Pandemie

Während der Corona-Pandemie seien primär zwei Darstellungsformen stark vertreten: Nach Leung et al. sind dies einmal Unterschiede bezüglich der Pandemiesituation zwischen Ländern und Kontinenten und Unterschiede zwischen  verschiedenen Zeiträumen und mit unterschiedlichen Maßnahmen zur Eindämmung der Pandemie (vgl. [@leung_big_2020]). In ihrem Artikel beschreiben die Autoren ein Tool zur Big-Data Analyse und nennen auch einige Negativbeispiele. So zeigen sie einen Chart, in dem die Neuinfektionen an einem Tag weltweit als "Bubble-Map" dargestellt werden (vgl. @fig:2-3). Für dieses Anwendungsszenario sei dieser Visualisierungstyp nicht gut gewählt, da der Graph durch die Überlappung der einzelnen Bubbles nicht gut abzulesen sei (vgl. [@leung_big_2020], S. 416). Besser sei eine eingefärbte Weltkarte mit einem Farbspektrum (vgl. @fig:2-3).

Zur Prognose der Pandemiesituation gibt es verschiedene Ansätze. In den letzten 10 Jahren haben sich laut Macal und North vor allem agentenbasierte Modellierungen zur Beschreibung von komplexen Situationen durchgesetzt (vgl. [@macal_agent-based_2009]). Bei agentenbasierten Modellen liegt der Fokus auf dem Individuum. Hierbei wird versucht, Einflüsse, welche unter realen Bedingungen existieren, abzubilden. Einzelne "Agenten" werden simuliert und deren Einfluss aufeinander untersucht (vgl. [@macal_agent-based_2009]). Durch die Entwicklung von leistungsstärkeren Computern sei es möglich geworden, solche Modelle zu erstellen (vgl. [@macal_agent-based_2009], S. 87). Gewöhnliche Modelle seien demnach für die Modellierung von komplexen Situationen nicht mehr zeitgemäß, so die Autoren (vgl. [@macal_agent-based_2009], S. 87).

\begin{center}
  \includegraphics[width=\linewidth]{source/figures/fig-2-3.png}
  \captionof{figure}{C. K. Leung et al., 2020, S. 416, Fig. 1+3}
  \label{fig:2-3}
\end{center}

Kerr et al. haben mit dem Covasim ein agentenbasiertes Modell zur Simulation von Infektionsgeschehen und Prävention entwickelt (vgl. [@kerr_covasim_2021]). Hiermit lässt sich auch der Einfluss von Kontaktbeschränkungen, wie social-distancing oder das Tragen von Masken, simulieren, wie auch der Einfluss von Impfungen und Tests (vgl. [@kerr_covasim_2021]). Ferner können auch Kontaktverfolgungsapps sowie Isolation berücksichtigt werden (vgl. [@kerr_covasim_2021]).

Der CovidSIM, welcher auch in der hier durchgeführten qualitativen Umfrage zum Einsatz kommt, wurde von Schneider et al. entwickelt und ist ein Simulator zum Pandemieverlauf, welcher auf einem klassischen, mathematischen SEIR Modell beruht (vgl. [@schneider_covid-19_2020]). SEIR-Modelle sind mathematische Modelle, welche zur Beschreibung der Ausbreitung von ansteckenden Krankheiten genutzt werden. Im Modell von Schneider lassen sich Eindämmungsmaßnahmen wie Kontaktreduzierung oder Home-Schooling und Home-Office einstellen. Die Autoren kamen zu dem Ergebnis, das Kontaktreduzierung und Social-Distancing die Pandemie erheblich verzögern können, sie allerdings nicht aufgehalten werden kann (vgl. [@schneider_covid-19_2020]).

Eine weitere Methode, Vorhersagen bezüglich der Pandemieentwicklung zu treffen, ist das Finden von Korrelationen und kausalen Zusammenhängen mit anderen Daten. Leung et al. bezeichnen diese Daten als "digital proxies" (vgl. [@leung_real-time_2021]). So konnten chinesische Forscher einen Zusammenhang zwischen dem verhängten Reiseverbot und dem damit verbundenen Rückgang von Infektionen feststellen (vgl. [@kraemer_effect_2020]). Sie konnten mit Mobilitätsdaten der chinesischen Bevölkerung ein Vorhersagemodell erstellen (vgl. [@kraemer_effect_2020]). Ein Forscherteam des Tropeninstituts am LMU Klinikum in München konnte anhand einer Abwasserüberwachung auf das Coronavirus eine Relation zwischen der Virusbelastung im Abwasser und der Inzidenzzahl feststellen (vgl. [@rubio-acero_et_al_spatially_2021]). Somit lassen sich auch mit indirekten Daten präzise Modelle erstellen.

## IEEE Computer Society Visualization Conference

Die "IEEE Computer Society Visualization Conference" ist eine jährlich stattfindende Versammlung, bei der der aktuelle Forschungsstand zu wissenschaftlichen und informationstechnischen Visualisierungen ausgetauscht wird (vgl. [@ieee_computer_society_technical_comitee_home_2021]).

\begin{center}
  \includegraphics[width=.7\linewidth]{source/figures/fig-2-4.png}
  \captionof{figure}{Aus VisLies Gallerie 2020: Eine geänderte Skalierung manipuliert das Ergebnis (Rogowitz et al., 2020)}
  \label{fig:2-4}
\end{center}

Bernice Rogowitz, eine amerikanische Wissenschaftlerin, welche sich mit dem Themengebiet der menschlichen Wahrnehmung beschäftigt, organisiert während der "IEEE Computer Society Visualization Conference" ein Forum, in welchem Teilnehmer Visualisierungen präsentieren können, welche den Betrachter durch eine verzerrte Darstellung in die Irre leiten (vgl. [@rogowitz_et_al_vislies_2021]). In der Galerie zum Forum von 2020 finden sich einige Beispiele über schlecht gewählte Visualisierungen zur Corona-Pandemie. So findet sich in der Galerie zum Beispiel ein Kuchendiagramm, welches in Summe mehr als 100% ergibt oder einen Vergleich von Neuinfektionen mit geänderter Skala, welche den Betrachter somit in die Irre führt (siehe @fig:2-4) (vgl. [@rogowitz_et_al_vislies_2020]).

\begin{center}
  \includegraphics[width=.7\linewidth]{source/figures/fig-2-5.png}
  \captionof{figure}{Unterschiedliche Farbskalen beeinflussen die Wahrnehmung. (Bernice E. Rogowitz, Treinish, \& Bryson, 1996)}
  \label{fig:2-5}
\end{center}

Schon 1996 beschreibt Rogowitz in ihrem Paper "How Not to Lie with Visualization", wie die Wahl von verschiedenen Farbskalen die Interpretation der gezeigten Visualisierung beeinflussen können (vgl. [@rogowitz_how_1996]). Anhand eines exemplarischen MRT-Scans, welchen sie mit unterschiedliche Farben koloriert, zeigt sie, welchen Einfluss Farbe haben kann. So liege der Fokus bei Nutzung einer gewöhnlichen Regenbogen-Skala auf der Farbe gelb, da diese als dominante Farbe viel zu stark heraussteche (vgl. [@rogowitz_how_1996], S. 268). Ohne Kenntnisse von Grundlagen über die menschliche Wahrnehmung von Farben zu besitzen, sei die Wahl einer korrekten Farbpallete erschwert, so Rogowitz (vgl. [@rogowitz_how_1996], S. 268). Da moderne Visualisierungen eine Vielzahl von Dimensionen besitzen können, wie zum Beispiel Form, Farbe, Textur, öffne dies die Büchse der Pandora bezüglich der Irreführung durch fehlerhaft dargestellte Daten (vgl. [@rogowitz_how_1996], S. 268). Zur Eindämmung dieses Problems schlägt die Autorin die Nutzung von "perceptual rules" ([@rogowitz_how_1996], S. 269) vor.
Konkret stellt sie mit den "Preceptual Rulebased Architecture for Visualizating Data Accurately (PRAVDA)" ([@rogowitz_how_1996], S. 269) ein Regelwerk für verschiedene Datentypen vor.

  >For nominal data, objects should be distinguishably different, but since the data themselves are not ordered, there should be no perceptual ordering in the representation. For ordinal data, objects should be perceptually discriminable, but the ordering of the objects should be apparent in the representation. In interval data, equal steps in data value should appear as steps of equal perceived magnitude in the representation. In ratio data, values increase and decrease monotonically about a true zero or other threshold, which should be preserved in the data representation. ([@rogowitz_how_1996], S. 269)

So sollen bei nominellen Daten die Messpunkte deutlich unterschieden werden können, ordinale Daten sollen wahrnehmbar unterscheidbar sein, bei intervall skalierte Daten soll der jeweilige Schritt sich wahrnehmbar in der Visualisierung wieder finden und bei rationalen Daten die Werte monoton steigen und fallen. Auch der Nullwert soll in der Visualisierung hervorgehoben werden (vgl. [@rogowitz_how_1996], S. 269). Ferner sollen isomorphe Farben oder sogenannte "spatial frequency colors" bevorzugt werden (vgl. [@rogowitz_how_1996], S. 269f). Auf letztere wird im weiteren Verlauf der Arbeit noch Bezug genommen. Ein Farbverlauf von gelb nach blau ist ein Repräsentant für isomorphe Farben. Abschließend sagt Rogowitz, dass moderne Systeme dem Nutzer zwar helfen können, das fehlende Grundwissen des Nutzers aber nicht ersetzen können (vgl. [@rogowitz_how_1996], S. 272).

"Spacial Frequency" heißt übersetzt ins Deutsche Ortsfrequenz und meint in der Wahrnehmungspsychologie die wahrgenommene Sehschärfe (vgl. [@maffei_visual_1973]). Wir können nur einen sehr kleinen Teil unseres Sichtfeldes scharf wahrnehmen. Dieser Teil auf der Retina wird Fovea genannt. Die Fovea nimmt zwar auf der Netzhaut nur einen sehr kleinen Teil ein, dafür sind aber viele Neuronen im visuellen Cortex mit ihr verknüpft (vgl. [@musseler_allgemeine_2017], S. 16ff). Eine hohe Ortsfrequenz bedeutet scharfes Sehen, während eine niedrige Ortsfrequenz unscharfes Sehen meint (vgl. [@maffei_visual_1973]). In einem Experiment haben zwei Forscher im Jahr 2001 festgestellt, dass die Echtheit der wahrgenommenen Farbe mit steigender Ortsfrequenz zunimmt (vgl. [@smith_role_2001]). Die oben genannten Ortsfrequenz-Farben sollten also nach Möglichkeit so gewählt werden, dass deren Farbechtheit nicht durch Ortsfrequenz oder Blickwinkel beeinträchtigt wird.

## Visual analytics

In den letzten Jahrzehnten stieg die Menge an produzierten und gesammelten Daten stärker an, als die Entwicklung von effizienten Methoden zur Analyse und Auswertung dieser Daten (vgl. [@keim_big-data_2013], vgl. [@liu_big_2014]). Keim sagt, dass die Komplexität mancher Probleme ein frühes Einbinden von Menschen in den Auswertungsprozess unmöglich macht (vgl. [@keim_big-data_2013]). Daher sei das Ziel, die Informationsflut zu kontrollieren und Möglichkeiten zur Analyse zu schaffen, so Keim weiter. Keim definiert mit Verweis auf Thomas und Cook die  Wissenschaft um "visual analytics" folgendermaßen:

  > "visual analytics is the science of analytical reasoning supported by interactive visual interfaces according to [@thomas_visual_2006]" ([@keim_big-data_2013])

Keim definiert "visual analytics" als Kombination von automatisierten, statistischen Auswertungsverfahren und zusätzlich mit der Möglichkeit, mit dieser visuell zu interagieren (vgl. [@keim_visual_2010]).

Blascheck et al. haben ein Tool entwickelt, um die Ergebnisse aus "Human Computer Interface" (HCI) Versuchen, also Versuchen, welche die Interaktion von Menschen mit Maschinen erforscht, besser zu analysieren. Mit dem Tool ließen sich Daten von "thinking aloud" Protokollen, "interaction logs" und "eye tracking" erfassen und kombiniert auswerten (vgl. [@blascheck_va_2016]). Die Autoren behaupten, dass aktuell die meisten Forscher Erfassung und Auswertung getrennt voneinander durchführen würden, eine kombinierte Erfassung und Auswertung aber vom Vorteil sei (vgl. [@blascheck_va_2016]). "Thinking aloud" Protokolle enthielten keine Informationen über unbewusste Prozesse. "Interaction logs" könnten in Kombination mit "visual eye tracking" diese Information liefern (vgl. [@blascheck_va_2016]).

Zur Erkennung von raum-zeitlichen Hotspots in großen Datensätzen haben die Forscher Maciejewski et al. in einem Paper eine Sammlung an Werkzeugen präsentiert, welches dem Nutzer erlaubt, in einer visuellen Umgebung mit dem Datensatz zu interagieren und so Abweichungen und Hotspots zu erkennen, wie in @fig:2-7 erkennbar (vgl. [@maciejewski_visual_2010]). Den Autoren nach ist die Auswertung von Daten ein kritischer Flaschenhals in der analytischen Argumentation (vgl. [@maciejewski_visual_2010]).

\begin{center}
  \includegraphics[width=.7\linewidth]{source/figures/fig-2-6.png}
  \captionof{figure}{Der Nutzer sieht seinen Datensatz visualisiert und kann sich Hotspots vergrößert anschauen. (Maciejewski et al., 2010, S. 212)}
  \label{fig:2-7}
\end{center}

Die chinesischen Forscher Pi et al. präsentierten in einem im August 2021 veröffentlichten Paper einen "visual analytics" Ansatz, welcher "convolutional neural networks" nutzt, um quantifizierte Metriken zur Kontaktverfolgung zu generieren (vgl. [@pi_deep_2021]). Dazu nutzten Sie Videodaten von öffentlichen Überwachungskameras, mit welchen sie ein maschinelles Modell (die YOLO-v3 Architektur) trainierten (vgl. [@pi_deep_2021]). Die Genauigkeit lag hierbei bei 69,41% (vgl. [@pi_deep_2021]). Das Modell haben die Forscher dann beispielhaft auf eine Kreuzung in Xiamen, China angewendet und anschließend die Verbreitung des Coronavirus auf eine gesunde Bevölkerung simuliert. Was der Algorithmus hierbei interpretiert, kann in @fig:2-8 nachvollzogen werden. Als Ergebnis erhielten die Wissenschaftler die Bestätigung der Hypothese, dass sich das trainierte Modell zur Kontaktverfolgung und Dokumentation von Infektionszeitpunkt und Infektionsort eignet (vgl. [@pi_deep_2021]).
Auch in der Soziologie ist die Wissenschaft um "visual analystics" von großer Bedeutung. Zur Analyse von sozialen Netzwerken haben die Forscher Federico et al. einen Ansatz veröffentlicht, mit dem sich die Dynamik von sozialen Netzwerken anschaulich analysieren lässt (vgl. [@federico_visual_2011]).

\begin{center}
  \includegraphics[width=.7\linewidth]{source/figures/fig-2-7.png}
  \captionof{figure}{(a) Ein Infizierter überquert die Kreuzung. (b) Jemand kommt dem Infizierten zu nah und der Algorithmus sagt eine Infektion voraus. Der Betroffene kann nun darüber informiert werden. (Pi et al., 2021, S. 10)}
  \label{fig:2-8}
\end{center}
