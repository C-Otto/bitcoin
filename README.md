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
1. [Sieht jeder meine Überweisungen?](#sieht_jeder_meine_ueberweisungen)
1. [Wie viele Bitcoin gibt es? Was ist mit Inflation?](#wie_viele_bitcoin_gibt_es)
1. [Wie wird die Blockchain aufgebaut? Wie arbeiten Miner?](#wie_wird_die_blockchain_aufgebaut)
1. [Wie sicher ist Bitcoin?](#wie_sicher_ist_bitcoin)
1. [Wie skaliert Bitcoin?](#wie_skaliert_bitcoin)
1. Was sind Micropayments?
1. Wurde Bitcoin gehackt? Ist Bitcoin pleite? Wurden Bitcoin-Kunden betrogen?
1. Braucht Bitcoin viel Strom?
1. Wie kann ich mit Bitcoin bezahlen?
1. Wo kann ich mit Bitcoin bezahlen?
1. Wo kann ich Bitcoin bekommen?
1. Was bedeutet Bitcoin für die Banken?
1. Vereinfacht Bitcoin Geldwäsche oder Drogenkauf?

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
Wenn zwei Geschäftspartner, beispielsweise ein Kunde und ein Verkäufer, sich auf einen Bitcoin-Preis einigen, kann der Kunde dem Verkäufer diesen Betrag überweisen und dafür die Gegenleistung in Empfang nehmen.
Eine solche Überweisung ist, egal ob für Kleinstbeträge und Beträge von mehreren Millionen, schnell (typischerweise Sekunden bis wenige Minuten), günstig (ein Euro-Cent oder weniger), sicher, und weltweit möglich.

Eine Besonderheit von Bitcoin ist, dass man als Teilnehmer an diesem Bezahlnetzwerk keiner zentralen Institution vertrauen muss.
Bei der Verwendung von Kreditkarten oder Diensten wie PayPal muss man dem Betreiber vertrauen, bei Bargeld dem Staat.
Bei Bitcoin gibt es eine solche zentrale Institution nicht.
Potenzielle Probleme wie Datendiebstahl, Zensur und unkontrollierbare Inflation werden dadurch vermieden.

## <a name="was_ist_die_blockchain"></a>Was ist die Blockchain?
Die Blockchain ist die Speicher-Technologie hinter Bitcoin, in der alle Bezahl-Informationen gespeichert werden.
Dies entspricht den zentralen Registern bei Banken oder anderen Bezahl-Anbietern.
Im Gegensatz zu klassischen Verfahren ist die Blockchain allerdings dezentral.
Das heißt, dass man die Informationen nicht an einer zentralen Stelle (beispielsweise im Rechenzentrum der Bank) manipulieren kann, sondern man stattdessen alle Kopien ändern muss.

Jeder[*](#sternchen) Teilnehmer am Bitcoin-Netzwerk hat eine Kopie der Blockchain und überprüft jede Transaktion basierend auf dieser Kopie.
Manipulationen werden daher frühzeitig erkannt und damit unpraktikabel.

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

Unabhängig davon wer die Technik erfunden hat, hat diese Person oder Gruppe "Satoshi Nakamoto" keine Möglichkeit fundamentale Änderungen vorzunehmen oder sonstwie zu betrügen.
Die Bezahlinformationen werden von allen Teilnehmern überprüft, und die dafür zugrundeliegenden Regeln können von einem Angreifer nicht beliebig verändert werden.

Die Grundannahme hinter Bitcoin ist, dass einzig die Mehrheit der Teilnehmer entscheidet, welche Regeln gültig sind.
Ein einzelner Angreifer kann also nicht betrügen, da eine entsprechende Transaktion von der Mehrheit der Teilnehmer bei der Überprüfung auffallen und verworfen werden würde.
Wenn allerdings die Mehrheit der Teilnehmer mit dem Betrüger zusammen arbeitet, gibt es hierfür keinen Schutz.
Hierbei ist allerdings zu bedenken, dass ein System, das in der Mehrheit aus Betrügern besteht, prinzipiell nicht benutzbar ist.

## <a name="was_ist_eine_bitcoin_wert"></name>Was ist eine Bitcoin wert?
Eine Bitcoin hat keinen festgeschriebenen Wert, ähnlich zu Aktien oder traditionellen Währungen.
Während bei traditionellen Währungen die Möglichkeit die Steuern in dieser Währung zu zahlen, oder das Bruttoinlandsprodukt des jeweiligen Staates eine gewisse Sicherheit geben, ist dies bei Bitcoin nicht gegeben.

Der Kurs entsteht durch Angebot und Nachfrage, ausgehend von Argumenten wie der Menge (Stichwort Inflation), der Benutzbarkeit, Sicherheit und Verbreitung.
Dementsprechend hatte eine Bitcoin kurz nach der ersten Transaktion im Jahr 2009 keinen Kurs (bzw. 0,00€).
Im Mai 2010 wurde für 10.000 Bitcoin Pizza bestellt, der damalige Kurs lag als bei etwa 0,03€ pro Bitcoin.

Durch ein besseres Verständnis des Sicherheitskonzepts und der Vorteile einer digitalen Währung, und natürlich auch
der Software-Weiterentwicklung, aber auch Spekulation und "Hype", hat sich der Preis in den letzten Jahren mit einigen
starken Schwankungen entwickelt und liegt aktuell bei mehreren hundert Euro pro Bitcoin.

Den aktuellen Kurs kann man beispielsweise unter [bitcoin.de](https://www.bitcoin.de/de/) einsehen:

<img src="https://bitcoinapi.de/widget/current-btc-price">

## <a name="sieht_jeder_meine_ueberweisungen"></a>Sieht jeder meine Überweisungen?
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
Der Aufwand ist allerdings für kleinere Beträge wie bei einem Kaffee-Kauf recht hoch, so dass es für das Geschäft sinnvoller sein kann das kleine Risiko einzugehen als auf die schnelle Bezahlmöglichkeit zu verzichten.
 
### Mehrere Bestätigungen
Sicherer ist es, einer Transaktion nur zu vertrauen, wenn diese in einem Block enthalten ist ("1 Confirmation").
Um eine solche Transaktion ungültig bzw. rückgängig zu machen, müsste man diesen Block nachträglich aus der Blockchain entfernen.
Dies ist allerdings nur möglich, wenn man eine parallele Blockchain konstruieren kann, die mindestens so viele Blöcke enthält wie die des oben erwähnten Blocks.
Da nach der Veröffentlichung des neuen Blocks alle Miner darauf aufbauend neue Blöcke hinzufügen, muss man also schneller zwei Blöcke finden als alle anderen Miner brauchen um einen Block zu finden.

Da es auch hier halbwegs praktikable Betrugsszenarien gibt, empfiehlt es sich für höhere Beträge darauf zu warten, dass die Transaktion in einem Block enthalten ist, auf dem aufbauend noch mindestens ein weiterer Block existiert ("2 Confirmations" oder mehr).
Der für einen Betrüger nötige Aufwand steigt exponentiell in der Anzahl der Blöcke, die die Transaktion enthalten bzw. darauf aufbauen.

Für Beträge im Bereich von wenigen 1.000€ ist ein Angriff nach zwei Bestätigungen schon unrentabel, sofern der Angreifer mit einer Wahrscheinlichkeit von höchstens 4% Blöcke hinzufügen kann.
Bei gleicher Wahrscheinlichkeit reichen schon 5-6 Bestätigungen, um Angriffe selbst bei Transaktionen im Millionenbereich unrentabel zu machen.
 
## <a name="wie_skaliert_bitcoin"></a>Wie skaliert Bitcoin?
Da alle Transaktionen an alle Teilnehmer geschickt werden, und diese alle Transaktionen speichern, kann das Bitcoin-Netzwerk nur eine begrenzte Anzahl von Transaktionen pro Sekunde bewältigen.

Der Speicherverbrauch ist aktuell vergleichsweise unproblematisch, alle Bitcoin-Transaktionen von 2009 bis Anfang 2016 verbrauchen ca. 60 GByte an Festplatten-Platz.
Festplatten sind viel größer (und werden immer größer), außerdem kann man beispielsweise mit Mobilgeräten auch bezahlen kann ohne diese Daten lokal vorzuhalten. 

Aktuell ist Bitcoin auf ca. 3-4 Transaktionen pro Sekunde begrenzt, während das VISA-Netzwerk durchgehend ca. 2.000 Transaktionen pro Sekunde bewältigt.
Der eigentliche Grund für die aktuelle Grenze ist die Limitierung der Block-Größe.
Jeder gefundene Block darf maximal 1.000.000 Byte groß sein (ca. 1 MByte), woraus sich die Anzahl der maximal enthaltenen Transaktionen ergibt.

Würde man größere Blöcke erlauben, könnte man dadurch natürlich mehrere Transaktionen pro Block bestätigen.
Hierbei ist aber zu beachten, dass dadurch auch mehr Daten durch das Netzwerk geschickt, auf Datenträgern gespeichert und von Prozessoren verifiziert werden müssen.
Seit Mitte 2015 wird kontrovers diskutiert, wie bzw. ob man diese Limitierung anpasst oder gar löscht.
Zusätzlich gibt es weitere Bemühungen durch Protokoll-Optimierungen mehr Transaktionen pro Block bestätigen zu können, beispielsweise indem man jede Transaktion verkleinert.

## <a name="sternchen"></a>Was bedeuten die Sternchen?
Einige der Aussagen sind nicht absolut richtig, was zu Recht auch von kritischen und informierten Lesern angemängelt werden könnte.
An den Stellen, an denen die vollständig korrekte Erklärung zu weit gehen würde und die gewählte Formulierung trotzdem die Kernaussage ausdrückt, deutet ein Sternchen auf eine solche Inkorrektheit hin.
Als Beispiel ist die Aussage "Man darf nicht bei Rot über die Kreuzung fahren" nicht ganz richtig, da es Ausnahmen für Einsatzfahrten der Polizei und Feuerwehr gibt.
Wenn man Kindern das Konzept einer Ampel erklärt, wird man allerdings vermutlich trotzdem nicht sofort auf sämtliche gesetzlichen Ausnahmeregelungen eingehen.

Im Kontext der IT gilt "Verschlüsselte E-Mails können nur Sender und Empfänger lesen" auch nicht immer.
Selbst bei guten Verschlüsselungsverfahren kann man mit extrem hohem Rechenaufwand (mehr, als selbst der NSA physikalisch möglich ist) jede Nachricht entschlüsseln.
Hier würde deshalb "Verschlüsselte E-Mails können nur* Sender und Empfänger lesen" stehen. 

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
