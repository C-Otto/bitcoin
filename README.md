# Bitcoin
Ein Versuch, Bitcoin und die Blockchain verständlich zu erklären

## Über diese Seite
Das Ziel dieser Seite ist, interessieren Lesern möglichst verständliche Informationen zum Thema Bitcoin und Blockchain zu geben.
Dabei werden neben Grundlagen auch interessante Details erklärt, die häufig falsch verstanden und in Artikeln falsch präsentiert werden.

Diese Seite lebt von Mitarbeit und Kritik. Ergänzungen, Korrekturen und Ähnliches dürfen gerne per [Pull Request](https://github.com/C-Otto/bitcoin/pulls) eingebracht werden.
Wer auf Probleme hinweisen oder Fragen stellen möchte, darf dafür gerne einen [Issue](https://github.com/C-Otto/bitcoin/issues) aufmachen.
Zusätzlich ist es natürlich auch möglich, Feedback per [E-Mail](mailto:bitcoin@c-otto.de) zu senden.

## Inhaltsverzeichnis

1. [Was ist Bitcoin?](#was_ist_bitcoin)
1. [Was ist die Blockchain?](#was_ist_die_blockchain)
1. [Was ist neu an Bitcoin?](#was_ist_neu_an_bitcoin)
1. [Wer steht hinter Bitcoin?](#wer_steht_hinter_bitcoin)
1. [Was ist eine Bitcoin wert?](#was_ist_eine_bitcoin_wert)
1. [Sieht Jeder meine Überweisungen?](#sieht_jeder_meine_ueberweisungen)
1. [Wie viele Bitcoin gibt es? Was ist mit Inflation?](#wie_viele_bitcoin_gibt_es)
1. [Wie wird die Blockchain aufgebaut? Wie arbeiten Miner?](#wie_wird_die_blockchain_aufgebaut)
1. [Wie sicher ist Bitcoin?](#wie_sicher_ist_bitcoin)
1. [Wie skaliert Bitcoin?](#wie_skaliert_bitcoin)
1. [Was sind Micropayments?](#was_sind_micropayments)
1. [Wurde Bitcoin gehackt? Ist Bitcoin pleite? Wurden Bitcoin-Kunden betrogen?](#wurde_bitcoin_gehackt)
1. [Braucht Bitcoin viel Strom?](#braucht_bitcoin_viel_strom)
1. [Wie kann ich mit Bitcoin bezahlen?](#wie_kann_ich_mit_bitcoin_bezahlen)
1. [Wo kann ich mit Bitcoin bezahlen?](#wo_kann_ich_mit_bitcoin_bezahlen)
1. [Wo kann ich Bitcoin bekommen?](#wo_kann_ich_bitcoin_bekommen)
1. [Was bedeutet Bitcoin für die Banken?](#was_bedeutet_bitcoin_fuer_die_banken)
1. [Vereinfacht Bitcoin Geldwäsche oder Drogenkauf?](#vereinfacht_bitcoin_geldwaesche_oder_drogenkauf)
1. [Was passiert, wenn keine neuen Bitcoin mehr erzeugt werden?](#was_passiert_wenn_keine_neuen_bitcoin_mehr_erzeugt_werden)
1. Was heißt `Multi Signature`?
1. Muss ich zum Benutzen die komplette Blockchain speichern?
1. Was brauche ich auf meinem Computer oder Handy, um Bitcoin benutzen zu können?
1. Wie speichere und sichere ich Bitcoin?
1. Was sind `Smart Contracts`?

## Weitere Quellen
- [Wie funktioniert Bitcoin? bitcoin.org](https://bitcoin.org/de/wie-es-funktioniert)
- [p2pLabs Lecture #1: Bitcoin & Blockchain-Technologie](https://www.youtube.com/watch?v=jAuqoOwepl0)
- [Analysis of hashrate-based double-spending](https://bitcoil.co.il/Doublespend.pdf)

## Autoren
### Dr. Carsten Otto
[Carsten Otto](mailto:bitcoin@c-otto.de) ist promovierter Informatiker und agiler Software-Entwickler.
Er ist besonders an den Technik-Details von Bitcoin interessiert.

## <a name="was_ist_bitcoin"></a>Was ist Bitcoin?
Bitcoin ist eine neue Technologie, mit der man digital bezahlen kann.
Hierbei kommt keine klassische Währung wie Euro oder US-Dollar zum Einsatz, sondern Bitcoin.
Beispielsweise kann ein Kunde einem Verkäufer einen Bitcoin-Betrag überweisen und dafür die Gegenleistung in Empfang nehmen.
Eine solche Überweisung ist, egal ob für Kleinstbeträge und Beträge von mehreren Millionen, schnell (typischerweise Sekunden bis wenige Minuten), günstig (ein Euro-Cent oder weniger), sicher und weltweit möglich.

Eine Besonderheit von Bitcoin ist, dass man als Teilnehmer an diesem Bezahlnetzwerk keiner zentralen Institution vertrauen muss.
Bei der Verwendung von Kreditkarten oder Diensten wie PayPal muss man dem Betreiber vertrauen, bei Bargeld dem Staat.
Bei Bitcoin gibt es eine solche zentrale Institution nicht.
Potenzielle Probleme wie Datendiebstahl, Zensur und unkontrollierbare Inflation werden dadurch vermieden.

## <a name="was_ist_die_blockchain"></a>Was ist die Blockchain?
Die Blockchain ist die Speicher-Technologie hinter Bitcoin, in der alle Zahlungsinformationen gespeichert werden.
Dies entspricht den zentralen Registern bei Banken oder anderen Bezahl-Anbietern.
Im Gegensatz zu klassischen Verfahren ist die Blockchain allerdings dezentral.
Das heißt, dass man die Informationen nicht an einer zentralen Stelle (beispielsweise im Rechenzentrum der Bank) manipulieren kann, sondern man stattdessen alle Kopien ändern muss.

Jeder[*](#sternchen) Teilnehmer am Bitcoin-Netzwerk hat eine Kopie der Blockchain und überprüft jede Transaktion basierend auf dieser Kopie.
Manipulationen werden daher frühzeitig erkannt und sind damit unpraktikabel.

Neue Zahlungen werden als zusätzliche Information in der Blockchain gespeichert.
Hierbei werden regelmäßig die neuesten Transaktionen in Form von Blöcken gebündelt und an die Teilnehmer des Netzwerkes verteilt.
Ein solcher neuer Block wird mit dem vorherigen Block verknüpft, so dass eine Kette von Blöcken ("Blockchain") entsteht.

## <a name="was_ist_neu_an_bitcoin"></a>Was ist neu an Bitcoin?
Vor der Erfindung von Bitcoin waren digitale Bezahlungen nur sicher möglich, wenn man einem zentralen Anbieter wie PayPal vertraut hat.
Dieser zentrale Anbieter hat einen Überblick über die jeweiligen Kontostände.
Wenn eine Überweisung ausgeführt wird, kontrolliert der Anbieter diese und passt die Kontostände an. 
Ohne diese Kontrolle wäre es wie bei einer MP3-Datei möglich, einen Geldbetrag zu kopieren und mehrfach auszugeben.

Ohne eine zentrale Instanz ist es allerdings nicht möglich gewesen, die Informationen zuverlässig aktuell zu halten.
Verteilverfahren wie "Peer to Peer" funktionieren gut und effizient, garantieren aber nicht, dass jeder Teilnehmer zu einem bestimmten Zeitpunkt die relevanten Daten auch wirklich hat.
Hierbei kann es also zu dem Konflikt kommen, dass man eine Bezahlung akzeptiert hat, aber kurz danach die Information bekommt, dass dieses Geld bereits anders ausgeben wurde.
Insbesondere, wenn einzelne Teilnehmer betrügen möchten, ist dieses dezentrale Verfahren nicht zuverlässig genug.

Mit der Blockchain wird dieses Problem gelöst, da die Blockchain nicht[*](#sternchen) nachträglich verändert werden kann und den gespeicherten Bezahlinformationen daher vertraut werden kann.

## <a name="wer_steht_hinter_bitcoin"></a>Wer steht hinter Bitcoin?
Die ursprüngliche Idee wurde von "Satoshi Nakamoto" im Jahr 2008 publiziert.
Bis heute ist allerdings nicht bekannt, wer hinter diesem Pseudonym steckt.

Unabhängig davon wer die Technik erfunden hat, hat diese Person oder Gruppe "Satoshi Nakamoto" keine Möglichkeit, fundamentale Änderungen vorzunehmen oder sonstwie zu betrügen.
Die Bezahlinformationen werden von allen Teilnehmern überprüft, und die dafür zugrundeliegenden Regeln können von einem Angreifer nicht beliebig verändert werden.

Die Grundannahme hinter Bitcoin ist, dass einzig die Mehrheit der Teilnehmer entscheidet, welche Regeln gültig sind.
Ein einzelner Angreifer kann also nicht betrügen, da eine entsprechende Transaktion von der Mehrheit der Teilnehmer bei der Überprüfung auffallen und verworfen werden würde.
Wenn allerdings die Mehrheit der Teilnehmer mit dem Betrüger zusammen arbeitet, gibt es hierfür keinen Schutz.
Hierbei ist allerdings zu bedenken, dass ein System, das in der Mehrheit aus Betrügern besteht, prinzipiell nicht benutzbar ist.

## <a name="was_ist_eine_bitcoin_wert"></a>Was ist eine Bitcoin wert?
Eine Bitcoin hat keinen festgeschriebenen Wert, ähnlich zu Aktien oder traditionellen Währungen.
Klassischen Währungen haben einen Wert, da man mit ihnen Dinge und Leistungen bezahlen kann - insbesondere Steuern.
Zusammen mit Kennzahlen wie dem Bruttoinlandsprodukt des jeweiligen Staates ergibt sich eine gewisse Sicherheit. 
Bei Bitcoin ist dies allerdings nicht gegeben.

Der Kurs entsteht durch Angebot und Nachfrage, ausgehend von Argumenten wie der Menge (Stichwort Inflation), der Benutzbarkeit, Sicherheit und Verbreitung.
Dementsprechend hatte eine Bitcoin kurz nach der ersten Transaktion im Jahr 2009 keinen Kurs (bzw. 0,00€).
Im Mai 2010 wurde für 10.000 Bitcoin Pizza bestellt, der damalige Kurs lag also bei etwa 0,03€ pro Bitcoin.

Durch ein besseres Verständnis des Sicherheitskonzepts und der Vorteile einer digitalen Währung, und natürlich auch
der Software-Weiterentwicklung, aber auch Spekulation und "Hype", hat sich der Preis in den letzten Jahren mit einigen
starken Schwankungen entwickelt und liegt aktuell bei mehreren hundert Euro pro Bitcoin.

Den aktuellen Kurs kann man beispielsweise unter [bitcoin.de](https://www.bitcoin.de/de/) einsehen:

<img src="https://bitcoinapi.de/widget/current-btc-price">

## <a name="sieht_jeder_meine_ueberweisungen"></a>Sieht Jeder meine Überweisungen?
Die Blockchain enthält jede Transaktion mit Angaben zu Quelle, Ziel, Betrag und Zeitpunkt.
Dementsprechend sind diese Details der Überweisung offen einsehbar.
Während man bei klassischen Banken aber nur ein Konto oder eine Kreditkarte hat, generiert man bei Bitcoin generell viele solcher "Konten" (genannt Adressen).

Dadurch, dass man hunderte bis tausende dieser Adressen benutzt und für jede Transaktion eine neue Adresse generieren kann, ist die Verknüpfung von einzelnen Adressen an konkrete Personen schwer.
Für eine konkrete Überweisung kann ich zwar eine Adresse mit meinem Handelspartner verknüpfen, ich weiß allerdings nicht welche Adressen dieser zusätzlich verwaltet.
Da jeder Teilnehmer auch (mit Hilfe von Bitcoin-Software) selbstständig diese Addressen verwaltet und es kein zentrales Register wie bei einer Bank gibt, ist das Bezahlen im Bitcoin-Netzwerk "pseudonym".

## <a name="wie_viele_bitcoin_gibt_es"></a>Wie viele Bitcoin gibt es? Was ist mit Inflation?
Aktuell, Anfang 2016, sind rund 14,7 Millionen Bitcoin im Umlauf, insgesamt wird es rund 21 Millionen Bitcoin geben.

Teil des Bitcoin-Protokolls ist, dass regelmäßig neue Bitcoins erzeugt und in Umlauf gebracht werden.
Die Grundidee ist, dass diese Neuschaffung alle vier Jahre halbiert wird.
In den ersten vier Jahren, bis zum 28.11.2012, wurden insgesamt 50% aller jemals verfügbaren Bitcoin erzeugt.
Seitdem, bis ca. Mitte 2016, werden weitere 25% erzeugt, und bis ca. 2020 noch einmal weitere 12,5%.
Die letzten 12,5% werden entsprechend über die darauf folgenden Jahre erzeugt.

Die Inflation ist also Teil des Protokolls, und man kann mit hoher Genauigkeit ausrechnen, wie viele Bitcoin es zu einem bestimmten Termin gibt.

Ähnlich zu einem Euro, den man in 100 Euro-Cent unterteilen kann, ist die kleinste Bitcoin-Einheit (genannt 1 Satoshi) 0,00000001 Bitcoin.
Dadurch ist es selbst bei einem hohen Bitcoin-Preis auch möglich, Transaktionen im Cent-Bereich (oder darunter) durchzuführen.

## <a name="wie_wird_die_blockchain_aufgebaut"></a>Wie wird die Blockchain aufgebaut? Wie arbeiten Miner?
Die Blockchain ist eine Kette von Blöcken, wobei jeder Block einzelne Transaktionen enthält und auf den Vorgängerblock verweist.
Einen neuen Block kann man nicht nach Belieben hinzufügen, da es anderenfalls leicht möglich wäre eine zweite parallele Blockchain zu erzeugen.
Wenn zwei oder mehrere Blockchains parallel existieren, ist nicht immer klar, welcher Blockchain man vertrauen kann.

Es gibt also nicht nur die Herausforderung, regelmäßig Blöcke (mit neuen Transaktionen) zu erzeugen, sondern auch dieses Erzeugen nicht zu einfach zu machen.
Das als "Proof of Work" bekannte Konzept sorgt dafür, dass genau dies möglich ist.

Zu jedem Block wird eine Prüfsumme berechnet und nur Blöcke, die eine Prüfsumme mit bestimmten Eigenschaften ergeben, werden als gültig angesehen.
Um diese Prüfsumme zu beinflussen, enthält jeder Block eine ansonsten unbedeutende Zahl.
Ändert man diese Zahl, ändert sich die Prüfsumme.
Nach genug Versuchen oder mit etwas Glück findet man also eine Zahl, so dass der Block mit dieser Zahl eine als gültig angesehene Prüfsumme hat.

Die Teilnehmer im Netzwerk, bzw. deren Rechner, die an dieser Blockerzeugung teilnehmen, nennt man Miner.
Prinzipiell arbeiten alle Miner nach dem gleichen Muster:
Eingehende Transaktionen werden überprüft, und zusammen mit einer zufälligen Zahl wird daraus ein Block mit Verweis auf den Vorgängerblock erstellt.
Wenn sich dadurch eine gültige Prüfsumme ergibt, wird dieser Block an die anderen Netzwerk-Teilnehmer verschickt, und neue Blöcke nehmen diesen Block als Vorgänger.
Wenn die Prüfsumme allerdings nicht zu den Anforderungen passt, wird der Vorgang mit einer anderen Zahl wiederholt.
Das wiederholt sich, bis die Prüfsumme passt oder ein neuer gültiger Block empfangen wurde.

Dieser Aufwand bedeutet für die Miner immense Strom- und Hardwarekosten, ist aber für die [Sicherheit von Bitcoin](#wie_sicher_ist_bitcoin) essentiell.
Damit die Miner trotzdem Blöcke hinzufügen, ist eine Belohnungs-Transaktion Teil eines jeden erzeugten Blocks:
Pro Block werden (aktuell) 25 neu erzeugte Bitcoin an den Miner ausgezahlt.
Der Miner kann diese Belohnung nach einer kurzen Wartezeit (100 Blöcke, die auf dem gefundenen Block aufbauen müssen) ausgeben und beispielsweise benutzen, um seine Stromrechnung zu zahlen.

Wie in der Antwort zur Frage ["Wie viele Bitcoin gibt es? Was ist mit Inflation?"](#wie_viele_bitcoin_gibt_es) erwähnt, werden neue Bitcoins nicht mit einer konstanten Geschwindigkeit erzeugt.
Bis zum 28.11.2012 hat jeder Block eine Belohnung von 50 Bitcoin enthalten, ab ca. Mitte 2016 wird die aktuelle Belohnung von 25 Bitcoin wieder halbiert, auf dann 12,5 Bitcoin.

## <a name="wie_sicher_ist_bitcoin"></a>Wie sicher ist Bitcoin?
Zum Thema Sicherheit gibt es diverse Fragestellungen.
Eine wichtige Frage, vielleicht die wichtigste bei digitalen Zahlungsmitteln, ist: Wie sicher kann ich mir sein, dass ich wirklich Geld bekommen habe und es später auch ausgeben kann?

Ein Händler gibt sein Produkt sinnvollerweise nur dann an den Kunden, wenn dieser bezahlt hat.
Diese Bezahlung muss so sein, dass der Händler dieses Geld anschließend selber ausgeben kann.
Wenn die Bezahlung zurückgezogen werden kann, oder andere Marktteilnehmer das Geld nicht akzeptieren, ist das offensichtlich nicht im Interesse des Empfängers.

Bei Bitcoin-Transaktionen gibt es beliebig viele Stufen der Sicherheit.

### "Zero Confirmation"
Im einfachsten Fall vertraut man einer Bezahlung, sobald man diese im eigenen Computer bzw. Mobilgerät sieht (und die darauf laufende Software die Transaktion überprüft hat).
Hierbei ist allerdings nicht sichergestellt, dass die Transaktion in den nächsten (oder einen späteren) Block hinzugefügt wird.
Der Absender der Transaktion kann theoretisch parallel eine konkurrierende Transaktion veröffentlichen, so dass nur eine der beiden Varianten gültig sein kann.
Wenn nun diese andere Transaktion in einen Block hinzugefügt wird, ist die ursprüngliche Transaktion wertlos und ungültig.
Durch das Beobachten des Netzwerkes, ob eine solche konkurrierende Transaktion bekannt wird, kann man in einigen Fällen frühzeitig (innerhalb von Sekunden) von dem Problem erfahren.
Es ist allerdings mit mehr Aufwand für den Betrüger auch möglich, die konkurrierende Transaktion "heimlich", beispielsweise mit Hilfe eines Miners, in den nächsten Block unterzubringen. 
Diesen sogenannten "Zero Confirmation"-Transaktionen sollte man sogesehen nicht vertrauen, insbesondere bei großen Beträgen (Hauskauf etc.).
Der Aufwand für den Betrüger ist allerdings für kleinere Beträge wie bei einem Kaffee-Kauf recht hoch, so dass es für das Geschäft sinnvoller sein kann das kleine Risiko einzugehen als auf die schnelle Bezahlmöglichkeit zu verzichten.
 
### Mehrere Bestätigungen
Sicherer ist es, einer Transaktion nur zu vertrauen, wenn diese in einem Block enthalten ist ("1 Confirmation").
Um eine solche Transaktion ungültig bzw. rückgängig zu machen, müsste man diesen Block nachträglich aus der Blockchain entfernen.
Dies ist allerdings nur möglich, wenn man eine parallele Blockchain konstruieren kann, die mindestens so viele Blöcke enthält wie die des oben erwähnten Blocks.
Da nach der Veröffentlichung des neuen Blocks alle Miner darauf aufbauend neue Blöcke hinzufügen, muss man also schneller zwei Blöcke erzeugen als alle anderen Miner brauchen um einen Block zu erzeugen.

Da es auch hier halbwegs praktikable Betrugsszenarien gibt, empfiehlt es sich für höhere Beträge darauf zu warten, dass die Transaktion in einem Block enthalten ist, auf dem aufbauend noch mindestens ein weiterer Block existiert ("2 Confirmations" oder mehr).
Für einen Betrüger, der mit einer Wahrscheinlichkeit von weniger als 50% Blöcke hinzufügen kann, sinkt die Erfolgs-Wahrscheinlichkeit exponentiell in der Anzahl der aufzuholenden Blöcke.

Für Beträge im Bereich von wenigen 1.000€ ist ein Angriff nach zwei Bestätigungen schon unrentabel, sofern der Angreifer mit einer Wahrscheinlichkeit von höchstens 4% Blöcke hinzufügen kann.
Bei gleicher Stärke des Angreifers reichen schon 5-6 Bestätigungen, um Angriffe selbst bei Transaktionen im Millionenbereich unrentabel zu machen.
 
## <a name="wie_skaliert_bitcoin"></a>Wie skaliert Bitcoin?
Da alle Transaktionen an alle Teilnehmer geschickt werden, und diese alle Transaktionen speichern, kann das Bitcoin-Netzwerk nur eine begrenzte Anzahl von Transaktionen pro Sekunde bewältigen.

Der Speicherverbrauch ist aktuell vergleichsweise unproblematisch, alle Bitcoin-Transaktionen von 2009 bis Anfang 2016 verbrauchen ca. 60 GByte an Festplatten-Platz.
Festplatten sind viel größer (und werden immer größer), außerdem kann man beispielsweise mit Mobilgeräten auch bezahlen ohne diese Daten lokal vorzuhalten. 

Aktuell ist Bitcoin auf ca. 3-4 Transaktionen pro Sekunde begrenzt, während das VISA-Netzwerk durchgehend ca. 2.000 Transaktionen pro Sekunde bewältigt.
Der eigentliche Grund für die aktuelle Grenze ist die Limitierung der Block-Größe.
Jeder gefundene Block darf maximal 1.000.000 Byte groß sein (ca. 1 MByte), woraus sich die Anzahl der maximal enthaltenen Transaktionen ergibt.

Würde man größere Blöcke erlauben, könnte man dadurch natürlich mehrere Transaktionen pro Block bestätigen.
Hierbei ist aber zu beachten, dass dadurch auch mehr Daten durch das Netzwerk geschickt, auf Datenträgern gespeichert und von Prozessoren verifiziert werden müssen.
Seit Mitte 2015 wird kontrovers diskutiert, wie bzw. ob man diese Limitierung anpasst oder gar löscht.
Zusätzlich gibt es weitere Bemühungen durch Protokoll-Optimierungen mehr Transaktionen pro Block bestätigen zu können, beispielsweise indem man jede Transaktion verkleinert.

Auf lange Sicht ist es allerdings unwahrscheinlich, dass alle Transaktionen (inklusive [Micropayments](#was_sind_micropayments) und den Alltagstransaktionen aller Menschen auf der Welt) mit dem aktuellen Blockchain-Modell abgearbeitet werden.
Stattdessen sind Modelle in der Entwicklung, die auf die Sicherheit der Bitcoin-Blockchain aufsetzen und viele kleine Transaktionen außerhalb der Blockchain bewältigen können.

## <a name="was_sind_micropayments"></a>Was sind Micropayments?
Micropayments sind Transaktionen von Kleinstbeträgen, welche es aufgrund der hohen Kosten im klassischen Umfeld mit Kreditkarten und PayPal eher wenig gibt.
Um per Bitcoin beispielsweise 0,20€ zu überweisen muss[*](#sternchen) man aktuell weniger als einen Euro-Cent an Transaktionsgebühren zuzahlen.
Dadurch ist es leicht möglich, einzelne Käufe wie Zeitungsartikel oder Fotos bequem zu bezahlen, oder Kleinstspenden ähnlich einem Facebook-Like zu verteilen.

## <a name="wurde_bitcoin_gehackt"></a>Wurde Bitcoin gehackt? Ist Bitcoin pleite? Wurden Bitcoin-Kunden betrogen?
In den Nachrichten findet man leider häufig Berichte über Bitcoin-Pleiten, Betrug, Hacks und ähnliches.
Hierbei handelt es sich meistens um einen konkreten Anbieter, der Bitcoin als Bezahlmöglichkeit genutzt hat.
Wenn diese Firma pleite geht, ihre Kunden betrügt, oder gehackt wird, hat das also nichts mit Bitcoin als Protokoll und Netzwerk zu tun, sondern nur mit dieser einen Firma.
Entsprechend gilt ja auch nicht "VISA wurde gehackt", wenn ein großer Anbieter wie Target die Kontrolle über die persönlichen und Kreditkarten-Daten von Millionen Kunden nach einem Hackerangriff verliert.

Ähnliches gilt, wenn einzelne Anbieter, die im Auftrag der Kunden Bitcoin verwahren, diese analog zu einem Bankeinbruch verlieren.

Bitcoin funktioniert seit der Inbetriebnahme 2009 und ist nicht tot oder pleite.
Angriffe auf das Bitcoin-Protokoll, so dass man Bitcoins beliebiger Teilnehmer stehlen konnte, gab es auch noch nicht.

## <a name="braucht_bitcoin_viel_strom"></a>Braucht Bitcoin viel Strom?
Das [Erzeugen von Blöcken durch die Miner](#wie_wird_die_blockchain_aufgebaut) kostet Strom.
Da in diesem Prozess bei dem Versuch eine passende Zahl zu finden nur ansonsten sinnlose Prüfsummen berechnet werden, könnte man diesen Schritt auch weglassen oder ersetzen und dadurch Strom und Aufwand sparen.
Wichtig für die Sicherheit im Bitcoin-Netzwerk ist allerdings, dass ein potenzieller Angreifer nicht nach Beliebigen Blöcke hinzufügen kann.

Für das Hinzufügen eines Blockes muss Rechenkraft und damit Energie investiert werden.
Je mehr Energie durch die Mehrheit der ehrlichen Miner investiert wird, desto mehr Energie muss ein Angreifer investieren um mit hoher Wahrscheinlichkeit eigene Blöcke zu erzeugen.

Dies ist ein großer Vorteil gegenüber beispielsweise der Möglichkeit, das Hinzufügen eines Blockes einem zufällig ausgewählten Teilnehmer im Netzwerk zu erlauben:
Ein Angreifer könnte mit geringem Aufwand eine nahezu unbegrenzte Anzahl von Teilnehmer-Rechnern starten oder deren Existenz vortäuschen.
Energie lässt sich allerdings nicht kopieren oder fälschen.

Aktuell (Anfang 2016) werden global, aufsummiert über alle Miner, ca. 832 x 10^15 (832.000.000.000.000.000) Prüfsummenberechnungen pro Sekunde durchgeführt.
Ein effizienter Miner (AntMiner S7) schafft 4 x 10^9 Hashes/Joule.
Damit verbrauchen alle Miner zusammen mindestens 208 Megawatt.
Da nicht alle Miner so effizient arbeiten, ist ein Verbrauch von 300 MW realistischer.

Dieser Wert ist unabhängig von der Anzahl der Transaktionen, da die Schwierigkeit einen Block hinzuzufügen nur aus der Erzeugungs-Geschwindigkeit der vorherigen Blöcke berechnet wird.

## <a name="wie_kann_ich_mit_bitcoin_bezahlen"></a>Wie kann ich mit Bitcoin bezahlen?
Für eine Bitcoin-Transaktion muss man die Empfängeradresse und den zu zahlenden Betrag kennen.
Die Empfängeradresse, ähnlich zu einer IBAN oder PayPal-Adresse, kann vom Empfänger direkt genannt werden (Beispiel: `1Et6T7N6BA9vQB9MjrWRnaoT4dDtTtbfhU`).
Üblich ist auch, die Adresse und ggf. auch den Betrag und eine Beschreibung in Form eines QR-Codes anzugeben, der mit Smartphone-Apps automatisch ausgewertet werden kann:
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAJYAAACWCAYAAAA8AXHiAAALy0lEQVR4Xu2d0XbruA5D2///6M7KiVebygrBTUpupsV9mxtZpkgQhCjV5/3t7e3jbfP/Pj7yr3h/f/9mzeOz0W+3h8bfHycabXgcG/02uoaMJW7tzNvxL7GRjL1FMR91MvPD2M7CDSzt9I5/9ey1EQbWLbMGRq0yXy0E96eIDYpFIzuitXXsH5/9BiyCfGI8cRoZG9mg1hKVwpOThvKcDUBnLVeVbuWn7FpHwBpYE7YwsLJw+hpnYB2+MGPNSzCH1P0JA8vA+oadHymFROiR3dvjytQ7ooWrZzsaLJu5ROhHJXZVgEf2UDovihvxH2IsEjgD6xwGBRZSjrNAN7AmJWnmPDMWgdRZ7/xZxiI7MMUApMQ+jiXOV/ZWmVvNS8pSNJacbJB3vlwpJA41sOah7vjl12osA2sOlqq+VYXTjDXxUCczO7ROdJ5L4aHzHg+hldbIBkfdQqhqofH9q449VJYTQKu5nv2uGIqUrFWJkI33uBP9998GloaCgXX2kSIhA0vj6nTzIPEIHmLGeuKyqrZQDq3SscooEnkz1mLGIs6PdFMnyEQvPNqgwEC63uS2KbFX2bhCj6ldd9UGNe/LXZtRAj0r/JXDDKy7J5WfsuSCGqTZSRV6zVh3D5HdcuR7JR+uYE0V8x+5mlwtLSownvcM4E5SV4nl1G7oTLRLZJNNgYFlYH3iUGWUgXXWQiuZexeZuBQmtM9vZsJtwPpYtS0AFpJA7WohAHO/iW7irpUim0gNsrZdY98NLO1a0prItkPUVl+BkiScXuH6EQZWwqcGVsJJwxADK+EzAyvhpFXAIlQ9mrWqgUds2HXFhmiuqKlIdsc8zF9PdP6qKCrzJ/urGosE1cCaQ4FsYjoAzuo+8g7Z8jCwrvsgx59lLIXCiIKvyD7Ckqq0/MT2fZf9pMxH4CYlVrHbN/FuYN1dq5xGApAtQ0ouEG1ENhsE7KTFYWBNUGJg6dRRPjKwDCyNooKPwrPC6ACYWEM0QFSOVamuloCVeoyUll3+JbFZ5bOTdou+Qbpr4VWhb2DNIaPKUnXTRXaxBtbhAQJusoM0Y9295VK4+MOyBtYBrMcGadUp/xD68AFYRc3kPUQvqPdmt/5EE5K+ENFyZGzUqlDyIVsmxzaMmjfcFVZLgAqwgXVkdfA1ZgMroVlIVhOGUk1Fko2PY81Yc+Cja+LZUthhIZJ9JKikG012OK/AqMTeagKpxCStn5O9BlbvEJowrErOLEDIPCRJFAGQ9lNaY6nFEPaojlULj8oZYQASDANr7gEDq9luMLAKwIpYirAOYQsytqMBCK1X/aA0TLb0qa0+2b2TjVRH75YPoQ0s3TIwsCYtgzFLOkgnLETGmrF0Id6ljZXeNWOJf5m1k2B/mrGytxt0bnyNUO3+6lwqS6JdIWG3qzQVOQhXzPO4dnK8tisW6UPoqgEq49W8xPkG1ln3EUCujIWBlfgoyDM2UIFQQSVJo+Z6Ocba8edfygmkAbmrLBEbIibsbDZWzasAHv1O/EBiUf4T+1XtBuUUsphoLqLPyDwG1rn83v4fA0she/idsDEBc2deuIRvw81YE+91nEKeXVWyVrG8AiEBGvEDqR7pL/qR7BsXRp4lxpN5ibPJUUZUClf6oSr0O62fViJEfSyyfSe6pGqwchLJvqq9ii3I2qpjVUJF56DK/uwOWM1jxpogzIw1F+RIEpixzsgysBYAK9vHUmWGaCOE/OJf/0iqDuYlxz+kpBKdR3pPaq3Z8qY0IZkn3W4wsHQWk8B0QKa0JgFlNTEUHgysxA3SSAxXA/OngFXdpdycVHU+yXKVJdVdbGeXRewnTNLRedX3EP+qxCjfeV+lQ0hgyMIVWAgISdIQvRNpFgPr8A5xfrV8GFh3z1XBe3t2FyGMMTVjLdZY1aArQR513lVZyjIjSVz1zvQ/Nl51mDLghPTG9wx2dZyvWDsBlpIPVa2s5APxr4E1Qb4KMk2WzHj1zipYCAgNrMNbRC8Q1lFBzgCFjlHvNLCoR4fxHQcSqq5uyZvLe/r4rwNW9aMgROgpis0GS7HOFQJXaUIC7shewsZRubsKsNt2haSFQEAZ9ZuiICsQrmIsAgDSmyLzGlhPtJEZS39KifQJq6xJhL6KWfo+lpqIMEvUV7nqPdVAEftI2eyMVc9mY0MqiZI3BlbzT+wJ0JTeiRKOlHayAaomuYH1pPyasc4pYcY6fNLJYgNrM7CidkMncKvqemQDoXySjaS8EftU+Yh8RtZ6xY5X6bryZ4zUxAZWfJPg5h8CFjLWwGoKZ+JsM9Ydbrs2EOO8ZixS9yZjXQrngC3feSdd5KhsKh13BSspG6qlhbCksqE6V/U5lW+K+QysF7mRaWA92eqTA+Dq2DGLyC4rykAVVDOWbk2cYlH9S+jOrrAKLAUkckZGOs4EeLvWRloRVT+Q8qdikT7SUc6taiEyr1pM1aFKhygbn4FUPUeuzRhYiZ3Trqw2sO7Or/rBjHV4gNxZIm0BpeWymutPM1b1BilpIRAAdIIa6SYCLAUIos+yJUyV+WgeoncVK2U3OajdQHSSgXX3gNJnBhY8uzKwDKwwaVwK2flZp+yQ04pV1aNT+iJZgkrhLhbq6Aeyg6w6UTpp0cffXkFrZjXUrMxHu80TdqIv+pE+C9nikmw0sM4tBJJAqzSgamMYWJOomLHm4O0wbHgIvYtZVrFQJxuzvahV7Q9VWhQLkeqR3YmOLKT0I2nZGFgJBosCpQDx+LtixizYV2lWA+uJx81YuuWhQEhYiIw1Y5mxnhIlYdhxbPp2g9IaVT1G5lVHLVUGUw6szkvKpNI3pBwTDUvGkvUYWIk/MDCwCKSO8py96EeYZddYM9a8LRCxHfGZGkvgZcYyY33iZRuwOhOTPgvp0pPtOilZRLNENkRZ3NmRIXYYPgi8yr+dtYUft60ujjhUCWcDS0eBdMhJy8DAOjxgxjprsE7itoD1aofQZDE6l3MjVjqfMMKuklWdV3mLyJ10g3RlebuCWZSTSIklGsvAOtoNZix20U8lhYFlYH0SkUthjt+XlcJVJWBXA0+xR9RS2HaUUbxtmgvtvEF6xXHa7c1Eu5U/CjI6gvTASFBJlhDhT2wgQSfzksTIJomKSweEBtYECeQPGQiQVrExeafaSO0CoYFlYH16YCUIEbCiQ2gyEdFjJKOIDatKS8RChFlIWeoAYJe9nbWGh9AkqAaWDgMpx0QLGViwROGdSPCvsxJhvytQfwpYUYNU52BtBNk5RW8gh6/EUgKAqn3KHlLWr7KXxC3dblCOIL8TA6uBI4HpaKGqfcpfxH4D6/CmgaVgte8rNp1EIHEzY0HdV20Ej3pRQet/z1jVO+/KMdmWggoU6bxHu1hV7qJd7avNq842V/lMxSbyWfnOu4E198Cq2w1RIhhYh3c64nJV9pmx7h4gO2kz1gTASqNcwSwjmElQfxVjEYRetbvovCdbrhUIs3pxFOhkXmUrSYTI3iv8+Y8ZH8W7gaXCu/Zfm9dv+xphYME/AO2AWYnYbOAIs6jDYrKDzNqnWhWdc8XsbpjYKhmr6nAVcNJoqy68Y8OqQKlgVP2rtJt6b/Z3wpKnhItKYXXhnaCu0gAdGwysexQMrAkaDawsLz0fZ2AZWH0UTWb43wEr0k3j+shlw2ozVWkWIsjJZqRqL5EokT9XonG0KWw3kAUQABhYdw8YWAloG1ha8EbMeFUbgzBqIuyfQ8xYhyuq+kGxOAmcGSsB3SpjKX2TeHV7CGEL9bJVPTr1nuj3VbHoxObHNVbH+I7zH581sHKeVGz9TTv/RIM0WgYxPucOPcrA0j4aNxvqiR85hI52hVXtIxcafKeTsGZVQ83sI2uNGHZVoqoEUz5OMxaZ6AqwqG46cfArBPUVbCCSgODBjDXx1qqzQlXWDSwC1cS1mSvYTZW3VwjqK9hwCWNB/KSHE12SnlQwDXnnT5XYKrDGpRNtRMaSWITXZshEZCwJMpk3YiXyTgOr4/X7swZWQlPtAiUBsNJn1RJmxiok0aqut4HFnT/67D8BS3d2nn/GuAAAAABJRU5ErkJggg==">

Eine weitere Möglichkeit ist die Übertragung der Daten per Nahfunk (NFC).
Hierbei hält man das Handy einfach an das Bezahlterminal (oder ein anderes Handy).

Eine Transaktion entsteht dadurch, dass man den Betrag zzgl. einer eventuellen Transaktionsgebühr, die Empfängeradresse und die Absende-Adresse kombiniert.
Zusätzlich muss man noch beweisen, dass man berechtigt ist von der ausgewählten Absende-Adresse zu überweisen - analog zum PIN/TAN-Verfahren beim Onlinebanking oder der Unterschrift bei klassischen Überweisungen.
Werden diese Informationen nun kombiniert abgesendet, wird das Bitcoin-Netzwerk diese überprüfen und weltweit weiterleiten.
Sekunden später sieht der Empfänger bereits die Transaktion, und nach wenigen[*](#sternchen) Minuten ist die Transaktion in einem der nächsten Blöcke enthalten.
   
Da man als Teilnehmer im Bitcoin-Netzwerk normalerweise mehrere Adressen benutzt, wählt das verwendete Programm automatisch aus den zur Verfügung stehenden Adressen.
Man muss deshalb die Absende-Adresse nicht selber angeben.
Im Normalfall werden sogar mehrere Absende-Adressen kombiniert, wobei als Teil der eigentlichen Transaktion "Wechselgeld" an eine neu generierte Adresse überwiesen wird.
Aber auch dies wird von den jeweiligen Programmen automatisch erledigt und ist aber für den Anwender nicht direkt sichtbar. 

## <a name="wo_kann_ich_mit_bitcoin_bezahlen"></a>Wo kann ich mit Bitcoin bezahlen?
Da man nicht um Erlaubnis fragen muss, kann prinzipiell jeder Händler Bitcoin entgegennehmen.
Verschiedene Anbieter wie beispielsweise [Coinbase](https://www.coinbase.com) und [BitPay](https://www.bitpay.com) bieten Integrationen in vorhandene Shops an und zahlen den Händlern auf Wunsch den Gegenwert einer Bezahlung in Dollar bzw. Euro aus.

Namhafte US-Firmen wie Dell, Microsoft, Expedia und Overstock akzeptieren (teilweise) Bitcoin.
Für den deutschsprachigen Raum gibt es [diese interessante Liste](http://bitcoinblog.de/2016/01/11/die-bitcoin-shopping-liste/).
Die Seite [coinmap.org](http://coinmap.org) zeigt außerdem Akzeptanzstellen auf einer Karte.

## <a name="wo_kann_ich_bitcoin_bekommen"></a>Wo kann ich Bitcoin bekommen?
Eine einfache Möglichkeit ist, mit jemandem zu tauschen der bereits Bitcoin hat.

In (nicht nur) Deutschland kann man sich bei [bitcoin.de](http://www.bitcoin.de) anmelden und einen Tauschpartner im Marktplatz finden.
Hierbei überweist man den Euro-Betrag per SEPA-Überweisung und bekommt kurz danach den Bitcoin-Betrag gutgeschrieben.

Die Smartphone-App Mycelium bietet einen Trader-Modus, in dem man Tauschpartner in der Nähe finden kann.
Dazu wird auch eine [Online-Karte](https://www.mycelium.com/lt/m/) angeboten.

International gibt es noch diverse andere Marktplätze und Börsen.
An dieser Stelle sei nur auf [Coinbase](https://www.coinbase.com), [Circle](https:/www.circle.com), [Anycoin Direct](https://anycoindirect.eu), [Kraken](https://www.kraken.com/) und [Bitstamp](https://www.bitstamp.net/) verwiesen.

## <a name="was_bedeutet_bitcoin_fuer_die_banken"></a>Was bedeutet Bitcoin für die Banken?
Für Banken ist Bitcoin als Währung eher uninteressant.
Die Blockchain-Technologie allerdings bietet einige neue Möglichkeiten, die auch für Banken interessant sind.

Banken können in der Blockchain sofort sehen, dass bestimmte Werte übertragen wurden.
Statt Bitcoin-Überweisungen könnte man mit der gleichen Technik prinzipiell auch Aktien oder andere Besitzrechte übertragen.
Das Verwalten solcher Besitzrechte ist im klassischen Bankenumfeld kompliziert und teuer, da die Informationen unter Einbeziehung mehrerer Teilnehmer weitergereicht werden.

## <a name = "vereinfacht_bitcoin_geldwaesche_oder_drogenkauf"></a>Vereinfacht Bitcoin Geldwäsche oder Drogenkauf?
Drogen werden selten per Kreditkarte oder Banküberweisung gekauft, da hierbei Spuren hinterlassen werden.
Die Polizei und andere Behörden können mit diesen Informationen schnell die Beteiligten identifizieren.
Ähnliches gilt für Geldwäsche.

Bei Bitcoin werden sämtliche Transaktionsdaten in der Blockchain veröffentlicht, sind also auch für diese Behörden verfügbar.
Den einzelnen Bitcoin-Adressen ist allerdings nicht offensichtlich eine Person zugeordnet.
Strafverfolgungsbehörden haben aber trotzdem die Möglichkeit, die Meta-Informationen (Uhrzeit, Betrag, ...) auszuwerten und zusammen mit bereits bekannten Zuordnungen (von gefassten Drogendealern, oder bekannten Unternehmen) zu verknüpfen.
Wer also im großen Stil Drogen kauft oder verkauft, hinterlässt eine Spur, die mit hohem Aufwand aufbereitet werden kann.
Insbesondere an der Schnittstelle zu klassischen Währungen, also dem Verkauf an einer Bitcoin-Börse oder dem Kauf von Waren in einem Online-Shop, ist es für die Behörden verhältnismäßig leicht zusätzliche Informationen zu gewinnen.

Für Geldwäsche, wobei es im Normalfall um größere Summen geht, ergibt sich ein ähnliches Bild.
Hinzu kommt, dass größere Beträge schwer zu tauschen sind bzw. entsprechende Angebote an den Börsen auffällig sind.
Das aktuell geringe Handelsvolumen von Bitcoin macht Geldwäsche im großen Stil riskant und damit uninteressant.
 
Im Vergleich zu Bargeld bietet Bitcoin zwar einige Vorteile insbesondere bei Online-Zahlungen, ist aber nicht uneingeschränkt für kriminelle Aktivitäten sinnvoll einsetzbar

## <a name="was_passiert_wenn_keine_neuen_bitcoin_mehr_erzeugt_werden"></a>Was passiert, wenn keine neuen Bitcoin mehr erzeugt werden?
Wie der Antwort zur [Frage "Wie viele Bitcoin gibt es? Was ist mit Inflation?"](#wie_viele_bitcoin_gibt_es) beschrieben, wird ca. alle vier Jahre die Anzahl neu erzeugter Bitcoin pro Block halbiert.
Ungefähr im Jahr 2140 werden somit keine neuen Bitcoin mehr erzeugt, wobei dann ca. 21 Millionen Bitcoin existieren.
Je Bitcoin gibt es (aktuell) acht Nachkommastellen, so dass es dann rund 2,1 Billiarden Recheneinheiten gibt.

Pro hinzugefügtem Block werden die neu erzeugten Bitcoin als [Belohnung an den jeweiligen Miner](#wie_wird_die_blockchain_aufgebaut) ausgezahlt.
Zusätzlich werden die Gebühren der im Block enthaltenen Transaktionen ausgezahlt, was aktuell nur knapp 0,4 Bitcoin zusätzlich zu den neuen 25 Bitcoin ausmacht.

Um die Kosten der Miner dauerhaft zu decken, ist es langfristig also nötig den Minern mehr Gebühren pro Block auszuzahlen.
Eine Möglichkeit ist, dass die einzelnen Transaktionen teurer werden.
Es ist aber auch denkbar, mehr Transaktionen in einem Block zu bestätigen, so dass die Gebühren pro Transaktion trotzdem gering sein können.

Außerdem kann es für Marktteilnehmer, deren Geschäftsmodell auf Bitcoin basiert, sinnvoll sein auch ohne Kostendeckung Mining-Equipment zu betreiben.

## <a name="sternchen"></a>Was bedeuten die Sternchen?
Einige der Aussagen sind nicht absolut richtig, was zu Recht auch von kritischen und informierten Lesern angemängelt werden könnte.
An den Stellen, an denen die vollständig korrekte Erklärung zu weit gehen würde und die gewählte Formulierung trotzdem die Kernaussage ausdrückt, deutet ein Sternchen auf eine solche Inkorrektheit hin.

Im Kontext der IT gilt "Verschlüsselte E-Mails können nur Sender und Empfänger lesen" auch nicht immer.
Selbst bei guten Verschlüsselungsverfahren kann man mit extrem hohem Rechenaufwand (mehr, als selbst der NSA physikalisch möglich ist) jede Nachricht entschlüsseln.
Hier würde deshalb "Verschlüsselte E-Mails können nur* Sender und Empfänger lesen" stehen. 

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
