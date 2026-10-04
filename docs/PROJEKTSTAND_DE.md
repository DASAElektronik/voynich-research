# Projektstand: Voynich Research

**Stand: 4. Oktober 2026. E001-E006. Keine bestaetigte Entschluesselung.**

## Ziel

Gesucht wird eine feste, nachvollziehbare Lesemethode fuer laengere Passagen des Voynich-Manuskripts. Ein plausibler Satz oder einzelne vertraut wirkende Woerter reichen nicht. Regeln, Datenauswahl, Parameter, Kontrollen und Gegenbeispiele sollen so dokumentiert sein, dass andere die Arbeit nachpruefen koennen.

Die Arbeit wurde von DASAElektronik initiiert und KI-gestuetzt entwickelt. Die Modellbezeichnung laut Unterhaltung lautet GPT-6 Astra Pro; eine unveraenderliche Backend-Revision ist nicht verfuegbar. Die mathematischen Ergebnisse stammen aus ausgefuehrtem Analysecode, nicht aus frei formulierten KI-Uebersetzungen. Externe Begutachtung und unabhaengige Replikation stehen aus.

## Bisherige Arbeit

Die folgenden Angaben fassen die vorbereiteten lokalen Versuchsberichte zusammen. Sie sind keine neue Auswertung waehrend der GitHub-Veroeffentlichung. Code, Originalberichte und Ergebnisarchive sind in dieses Repository noch nicht vollstaendig importiert.

| Versuch | Frage und Vorgehen | Ergebnis und Grenze |
|---|---|---|
| E001 | Ist EVA-m ausschliesslich ein Zeilenendezeichen? Pilot auf f1r-f8v; 199 ausgewaehlte Zeilen. | 26 letzte und 38 fruehere Wortgruppen enden auf m. Die ausschliessliche Regel scheitert; der Positionsunterschied allein erklaert die Funktion nicht. |
| E002 | Folgeprobe f9-f16, ohne das fehlende f12; Gegenpruefung mit zweiter Umschrift. | Unterschiedliche Unsicherheitsmarkierungen fuehren beim strengen Filter zu 143 IT-, aber nur 59 ZL-Zeilen. Die kombinierte IT-Laengen-/Absatzkontrolle liefert p=1/12 bei nur drei variablen Vergleichszeilen. |
| E003 | Unsichere Wortgrenzen und angegebene Lesarten als Varianten erhalten. | Vergleich derselben 145 Zeilen beider Umschriften. Der deskriptive Positionsunterschied bleibt; Variantenbereiche sind keine Konfidenzintervalle und erfassen keine unmarkierten Lesefehler. |
| E004 | Zaehlt auch ein Rand vor einer Zeichnung? Alle bisherigen IT-Gegenbeispiele einbeziehen. | 76 ausdrueckliche m-Komponenten: 34 am Zeilenende, 4 vor Zeichnungen, 35 an sonstigen Wortenden und 3 wortintern. Die strenge Rand-Regel scheitert. |
| E005 | Wortformen und lokale Konzentration auf dem Doppelblatt f3/f6 vergleichen. | 52 m-Endungen in 36 Formen; nach Entfernen der zwei haeufigsten Formen bleiben 42 in 34 Formen. r- und l-Gegenstuecke liefern keinen eindeutigen Schluessel. Die konkrete Ortsbeobachtung war bereits 2024 oeffentlich diskutiert worden. |
| E006 | Kalibrierte feste Schluesselsuche mit einem kleinen lateinischen Viererfolgenmodell; sieben Voynich-Varianten und getrennte Pruefseiten. | Vier kuenstliche Verschluesselungen desselben Kontrolltextes werden vollstaendig geloest. Keine der sieben Voynich-Varianten liefert bestaetigten Klartext. |

## E006 genauer

Das Sprachmodell wurde aus 1.350 normalisierten Woertern von Caesar, De bello Gallico I.1-10, gebildet. Andere Kapitel desselben Werkes, I.11-20, lieferten die Kontrollpassagen. Drei einfache Ersetzungsschluessel und ein homophones Verfahren wurden untersucht. Jede der vier Kontrollen stellte 4.813 Buchstaben im Suchteil und weitere 3.659 im Pruefteil richtig wieder her. Das sind vier Verschluesselungen desselben Textes, nicht vier unabhaengige Werke.

Die Voynich-Suche verwendete 820 bereinigte Wortgruppen auf acht ausgewaehlten Seiten. Ein unveraenderter Schluessel wurde anschliessend auf 619 Wortgruppen von f18r/v bis f21r/v angewandt. Geprueft wurden einzelne EVA-Komponenten, globale m/r- beziehungsweise m/l-Zusammenfassung, umgekehrte Leserichtung, Zusammenziehen unsicherer Wortgrenzen und zwei feste Verbundzeichensaetze.

Die Suche hatte 24 Neustarts mit jeweils 30.000 vorgesehenen Vorschlagsschritten und drei nachfolgenden gierigen Verbesserungsdurchlaeufen. Entwicklungsscores bestimmten den Gewinner; die Pruefseiten wurden nicht zur Anpassung des Schluessels benutzt. Sie sind nach diesem Versuch allerdings bekannt und duerfen kuenftig nicht wieder als ungesehen gelten.

Alle 14 abgeschlossenen Laeufe wurden in E006 mit ihren festen Schluesseln erneut bewertet. Neun vollstaendige Suchlaeufe wurden damals ebenfalls wiederholt. Die fuenf anderen Suchlaeufe erhielten keine vollstaendige zweite Optimierung. Bei diesem Veroeffentlichungsschritt wurde weder die Schluesselsuche noch die Quellpruefung erneut ausgefuehrt.

## Daten und wichtige Korrekturen

EVA bezeichnet eine Umschrift, keine nachgewiesenen Lautwerte. Eine durch Zwischenraeume getrennte Wortgruppe ist noch kein identifiziertes Wort einer natuerlichen Sprache.

E001-E005 verwenden vorwiegend manuell uebertragene Ausschnitte der IT-Umschrift; ZL dient als Gegenpruefung. E006 konnte 17 kleine ZL-Spiegeldateien bytegenau gegen extern gelieferte Git-Blob-Kennungen pruefen. Die vollstaendigen IT-/ZL-Masterdateien und die Originalglyphen sind dadurch nicht verifiziert. Zwei Umschriften desselben Manuskripts sind keine zwei unabhaengigen Handschriften.

Die ZL-Lesung enthaelt auf f2v.5 ein m, obwohl es im entsprechenden frueheren IT-Befund fehlte. An f4v.9 liest ZL cheog an einer Stelle, an der IT ein m geliefert hatte. Eine pal aeografische Entscheidung zwischen diesen Lesungen steht aus. Die frueheren Nullbefunde sind deshalb auf ihre konkrete Umschrift zu beschraenken.

Eine bereits bereinigte Spalte des verwendeten Spiegels verbindet Text teilweise ueber Zeichnungsunterbrechungen hinweg. E006 verwendet deshalb die erhaltene Rohspalte und bewahrt diese Grenzen. Die bisherigen Projektparser behandelten solche Unterbrechungen ebenfalls als Wortgrenzen.

## Was Tests belegen

Die archivierten E006-/Uebergabepruefungen dokumentieren 156 Forschungstests. Spaetere Publikations- und Windows-Reparaturtests sind davon getrennte technische Schutztests, keine zusaetzlichen wissenschaftlichen Experimente. Ein passender Datei-Hash prueft die Datenuebertragung; ein Softwaretest prueft die Implementierung; keines von beidem beweist eine Entschluesselung.

Ein Windows-Fehler beim Uebergabeskript entstand durch das erneute Schreiben einer versionierten Auditdatei. Der vorbereitete Korrekturstand schreibt neue Auditberichte mit festen Zeilenumbruechen in das ignorierte Verzeichnis results/local. Historische Forschungsergebnisse wurden dabei nicht ersetzt.

## GitHub-Veroeffentlichung: tatsaechlich erreicht

Das oeffentliche Zielrepository ist angelegt. Der direkte GitHub-App-Schreibzugriff wurde mit dem Initialisierungs-Commit 678a5705d02c8d8919f4c5aa29d8ac820f129524 und anschliessendem Lesen der README bestaetigt. Dieser Nachweis betrifft einen wirklichen Dateischreibvorgang, nicht nur angezeigte Kontoberechtigungen.

**Der vollstaendige Import ist noch offen.** Die vorbereitete lokale Historie endet auf 51adc17871553d7577ef4340c37996bca0dafd83 und enthaelt 17 Commits einschliesslich Dokumentation und Windows-Korrektur. Diese Kennung ist derzeit kein als importiert bestaetigter Remote-Commit. Die frueheren wissenschaftlichen Commits sollen unveraendert erhalten bleiben. Der neue GitHub-Initialisierungsstand muss dabei ebenfalls beruecksichtigt werden; ein blindes oder erzwungenes Pushen ist nicht vorgesehen.

Auf GitHub wurden in diesem Schritt keine Forschungstests oder GitHub-Actions-Pruefungen ausgefuehrt. Die Originaldateiarchive bleiben vorerst in den Uebergabepaketen. Ein spaeterer Import muss Bestand, Dateiinhalte und Historie am Remote erneut pruefen.

## Quellen und Lizenz

Die ausfuehrlichen lokalen Berichte nennen insbesondere die [Transkriptionsdokumentation von Rene Zandbergen](https://www.voynich.nu/transcr.html), die [IVTFF-Konventionen](https://www.voynich.nu/extra/sp_transcr.html), [Matthew Greens versionierten ZL-Spiegel](https://github.com/matthewdgreen/cipher_benchmark/tree/main/benchmark/unsolved/sources/voynich/transcriptions), [Caesars lateinischen Kontrolltext](https://www.thelatinlibrary.com/caesar/gall1.shtml), [die fruehere Diskussion der Glyphenverteilung](https://www.voynich.ninja/thread-4357.html) und [Patrick Feasters Untersuchung der Uebergangswahrscheinlichkeiten](https://griffonagedotcom.wordpress.com/2021/09/20/transitional-probabilities-in-the-voynich-manuscript/).

Eine allgemeine Lizenz fuer den eigenen Code und die Dokumentation wurde noch nicht festgelegt. Fremde Transkriptionen, Abbildungen und andere Quellen werden nicht neu lizenziert. Manche archivierten Schluessel und Kandidatenausgaben erlauben die Rekonstruktion analysierter Quellausschnitte; ihre Ableitung macht die Quellenrechte nicht gegenstandslos.

## Naechste Forschungsschritte

Vor weiteren Modellanpassungen sind belastbare Originalbilder und konkurrierende Transkriptionen zu vergleichen, vielfaeltigere historische Kontrolltexte festzulegen und komplexere Codiermodelle an bekannten Faellen zu kalibrieren. Erfolgskriterien und neue Pruefdaten muessen vor der Schluesselsuche feststehen. Negative Ergebnisse und Korrekturen bleiben Teil der Arbeit.
