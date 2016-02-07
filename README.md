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
1. Wie kann ich mit Bitcoin bezahlen?
1. [Wo kann ich mit Bitcoin bezahlen?](#wo_kann_ich_mit_bitcoin_bezahlen)
1. Wo kann ich Bitcoin bekommen?
1. Was bedeutet Bitcoin für die Banken?
1. Vereinfacht Bitcoin Geldwäsche oder Drogenkauf?
1. Was passiert, wenn keine neuen Bitcoin mehr erzeugt werden?
1. Was heißt `Multi Signature`?

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
Eine solche Überweisung ist, egal ob für Kleinstbeträge und Beträge von mehreren Millionen, schnell (typischerweise Sekunden bis wenige Minuten), günstig (ein Euro-Cent oder weniger), sicher und weltweit möglich.

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

## <a name="was_ist_eine_bitcoin_wert"></name>Was ist eine Bitcoin wert?
Eine Bitcoin hat keinen festgeschriebenen Wert, ähnlich zu Aktien oder traditionellen Währungen.
Während bei traditionellen Währungen die Möglichkeit die Steuern in dieser Währung zu zahlen, oder das Bruttoinlandsprodukt des jeweiligen Staates eine gewisse Sicherheit geben, ist dies bei Bitcoin nicht gegeben.

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
 
## <a name="wo_kann_ich_mit_bitcoin_bezahlen"></a>Wo kann ich mit Bitcoin bezahlen?
Da man nicht um Erlaubnis fragen muss, kann prinzipiell jeder Händler Bitcoin entgegennehmen.
Verschiedene Anbieter wie beispielsweise [Coinbase](https://www.coinbase.com) und [BitPay](https://www.bitpay.com) bieten Integrationen in vorhandene Shops an und zahlen den Händlern auf Wunsch den Gegenwert einer Bezahlung in Dollar bzw. Euro aus.

Namhafte US-Firmen wie Dell, Microsoft, Expedia und Overstock akzeptieren (teilweise) Bitcoin.
Für den deutschsprachigen Raum gibt es [diese interessante Liste](http://bitcoinblog.de/2016/01/11/die-bitcoin-shopping-liste/).
Die seite [coinmap.org](http://coinmap.org) zeigt außerdem Akzeptanzstellen auf einer Karte.

## <a name="sternchen"></a>Was bedeuten die Sternchen?
Einige der Aussagen sind nicht absolut richtig, was zu Recht auch von kritischen und informierten Lesern angemängelt werden könnte.
An den Stellen, an denen die vollständig korrekte Erklärung zu weit gehen würde und die gewählte Formulierung trotzdem die Kernaussage ausdrückt, deutet ein Sternchen auf eine solche Inkorrektheit hin.

Im Kontext der IT gilt "Verschlüsselte E-Mails können nur Sender und Empfänger lesen" auch nicht immer.
Selbst bei guten Verschlüsselungsverfahren kann man mit extrem hohem Rechenaufwand (mehr, als selbst der NSA physikalisch möglich ist) jede Nachricht entschlüsseln.
Hier würde deshalb "Verschlüsselte E-Mails können nur* Sender und Empfänger lesen" stehen. 

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
