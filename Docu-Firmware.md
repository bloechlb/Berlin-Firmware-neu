Berlin Freifunk: Technologie/Firmware

Technologie

Im Abschnitt „Mitmachen" <https://berlin.freifunk.net/de/participate/>
wurde bereits erwähnt, dass man zum/r Freifunker-in wird, wenn man einen
Freifunkrouter aufsetzt und für andere verfügbar macht. Generell ist ein
Router voraussetzung für den Zugang zum Internet.

![](Pictures/100000000000050C00000384690D3E5382772C44.png){width="17cm"
height="11.841cm"}Bildquelle:
<https://commons.wikimedia.org/wiki/File:03-freiffunk-router-mit-gaesten2.png>

Nachfolgend wird Freifunk gelegnetlich mit FF abgekürzt. Ein
Freifunk-Netzwerk besteht aus eine Vielzahl drahtloser Verbindungen, wie
die Bezeichnung „Netz" bereits vermuten lässt. Die Maschen des Netzes
werden durch Richtantennen mit großer Reichweite für die
Aufwärtsverbindung zu einem Hub als auch Rundstrahlantenne mit kürzerer
Reichweite gebildet. Dazu kommt ein kleinteiliges Netz mittels
Verbindungen zu anderen Knoten in der Nähe. Dein Freifunk-Router kann
Teil davon werden und das Netz verstärken.

![](Pictures/10004F2E0000FA9C00006E49047AA695E2B23C62.svg){width="17cm"
height="7.481cm"}Bildquelle:
https://commons.wikimedia.org/wiki/File:Freifunk\_Mesh.svg

Die Freifunk-Gemeinschaft als „Graswurzelbewegung" ist im Besitz des
gemeinschaftlich betriebenen Netzwerkes und nutzt spezielle Software,
ebenso wie viele andere gleichartige Gemeinsachaften. Diese Software
muss an die benutzte Hardware der verschiedenen Hersteller angepasst
sein. Diese angepasste Software wird als „Firmware" bezeichnet. Für
unterscheidliche Hardware ist demnach eine spezielle, angepasste
Software/Firmware nötig, die nur auf der passenden Hardware ausgeführt
werden kann, man nennt das „lauffähig ist".

Die aktuelle Berliner Freifunk-Firmware heißt falter und wurde im
Frühjahr 2021 veröffentlicht. Die Firmware wird laufend verbessert, was
in eine neue Version mit neuem Namen mündet. Jede
Freifunk-Gemeinschaften nutzt gewöhnlich eine eigene Firmware die nur in
jeweiligen örtlichen Gemeinschaft funktioniert.

Alle haben als Basis die auf Internetunterstützung optimierte open
source Linux-Version OpenWrt
(https://de.wikipedia.org/wiki/Open\_Source). Weitere Informationen zur
OpenWrt-Projektorganisation findest Du auf den Seiten „Über OpenWrt"
(https://openwrt.org/). Für die Entwickler von Software dient OpenWrt
als so genanntes „Framework". Solch ein Framework stellt eine
Softwarebasis zur Verfügung und hilft damit beim Erstellen einer
Anwendung. Der Entwickler einer Anwendung kann darauf zugreifen und muss
nicht eine komplette Softwareumgebung arbeitsaufwendig selbst erstellen.

![](Pictures/1000000100000A00000002BF187B81FF249E4BF4.png){width="17cm"
height="4.667cm"}

Um mit Freifunk zu beginnen sind jedoch keine vertieften
Detailkenntnisse nötig, weil nur die von Entwicklern erstellte und
bereitgestellte Firmware genutzt wird.

Häufig wird gefragt, warum für diesen oder jenen Router keine
Freifunk-Software angeboten wird? Einzelne, ungeeignete Typen von
Prozessoren oder zu wenig Speicher verhindern bei manchen Geräten die
Implementation von OpenWrt. Ohne OpenWrt und ausreichend freien Speicher
auch keine Freifunk-Firmware, ganz einfach. Außerdem muss sich jemand
finden, der die Aufgabe ausführt, Software für einen Router
implementiert, auch ganz einfach. Deshalb wird nicht für alle Router aus
der OpenWrt-Liste Freifunk-Firmware angeboten. In einem späteren Kapitel
wird beschrieben, wie man die Software selbst kompilieren kann, sofern
OpenWrt auf dem Target läuft und man über entsprechende Kenntnisse
verfügt.

Neue Page
\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#

Firmware/Image

Wie bereits erwähnt, ist die Unterstützung von OpenWrt Voraussetzung für
die Implementation von Falter auf einem potentiellen Freifunk-Router. Da
Falter auf OpenWrt basiert, kann die „Table of Hardware" von OpenWrt als
erstes Kriterium für unterstützte Hardware genommen werden.
Informationen zu den von OpenWrt unterstützten Geräten findest Du bei
Interesse auf (<https://openwrt.org/supported_devices>). Das beantwortet
oft manche gestellte Frage, warum die Freifunk-Software für bestimmter
Router nicht angeboten wird. Ohne OpenWrt keine Freifunk Software.

Vorgefertigte Images für die gängigsten Router kannst du von dem
Freifunk Firmware-Selector downloaden. Die Liste
<https://selector.berlin.freifunk.net/> gibt Auskunft, ob die
FF-Firmware erhältlich ist, wenn Du bereits einen Router hast. Wenn Du
einen Kauf planst würde ich einen in der Liste vorhandenen empfehlen um
die Freifunk-Firmware mit Sicherheit zu bekommen. Das kann geprüft
werden, indem man Hersteller und die Typbezeichnung in die Suchzeile
eingibt. Dort kann im positiven Ergebnis die passende Firmware
runtergeladen werden, aber eben nur sofern diese nach Liste verfügbar
ist. Es ist wichtig, auf die Versionsnummer zu achten. Eine andere
Versionsnummer bedeutet Änderungen der Hardware des Routers durch den
Hersteller, die möglicherweise eine Implementierung der
Freifunk-Firmware verhindert.

Tipp: Bevor Du Hardware kaufst, erkundige Dich nach Pool-Geräten zur
Freifunk-Verfügung auf Mailing-Liste und im Chat. Wir haben Technik in
den Regalen, die auf Verwendung wartet! :-)

Beim Kauf eines neuen Routers bei großen Versandfirmen wird im Angebot
oft die Versionsnummer nicht angegeben, es wird gewöhnlich das neueste
Modell mit der neuesten Version geliefert. Es zeigt sich dann oft, dass
dieses Modell mit höherer Versionsnummer nicht in der
Kompatibilitätsliste steht. Die FF-Software kann auf diesem Modell
funktionieren, das muss aber nicht zwangsläufig der Fall sein. Oft wird
bei einem leichtsinnigen Versuch dann der neuer Router gebrickt und
unbrauchbar.

Tipp: Bei ebay werden Router oft mit Angabe der Versionsnummer
(preisgünstig) angeboten, was eine sichere Alternative zum Blindkauf des
neuesten Routers unbekannter Versionsnummer darstellen kann -- zumindest
für den Anfang.

Um den Router FF-tauglich zu machen muss die passende FF-Firmware auf
den Router „geflasht" werden. Durch sogenanntes „Flashen" wird die
Herstellerfirmware die in einem wiederbeschreibbaren Speicher sitzt
vollständig durch die Freifunk-Firmware ersetzt. Ein solches fertiges
Firmware-Paket für einen gelisteten Router nennt man Image. Die
Firmware, das Image, gibt es in verschiedenen Varianten. Du solltest die
Unterschiede zwischen ihnen kennen, um die richtige Firmware für dich
aussuchen zu können. Generell wird zwischen Factory-Images und
Sysupgrade-Images unterschieden. Factory-Images werden ausschließlich
beim ersten Flashen des Routers benutzt, also dann, wenn von der
originalen Firmware auf die Freifunk-Firmware geflasht wird, also bei
der Erstinstallation. Sysupgrade-Images updaten auf eine neue Version
wenn auf dem Gerät bereits FF-Software installiert ist. Es gibt aber
Ausnahmen, Details, wie genau es bei deinem Router funktioniert, findest
du im OpenWrt-Wiki (<https://openwrt.org/toh/start>) auf der
Artikelseite für dein Router-Modell.

Vorab soll warnend erwähnt werden, dass das Flashen einer falschen
Firmware-Version den Router unbrauchbar machen kann -- das nennt man
„bricken". Also ist Sorgfalt geboten. Gelegentlich ist eine Reparatur
möglich, aber leider nicht immer bei allen Fabrikaten.

Die Installation, das Flashen der Firmware/des Images wird in einem
eigenen Abschnitt beschrieben. Firmware/Howto
<https://wiki.freifunk.net/Berlin:Firmware/HowTo>.

Den Abschnitt „Image-Typen" leicht gekürzt aus
<https://wiki.freifunk.net/Berlin:Firmware#Unterst.C3.BCtzte_Router>
übernommen, copyright ist CC BY-SA 3.0

Image-Typen:

tunnel-berlin-tunneldigger (Standard)

Das direkte Ausleiten des Freifunk-Datenstromes über den eigenen
Anschluss war in Deutschland lange Zeit durch die Störerhaftung
erschwert. Die rechtliche Situation hat sich 2017 hier deutlich
verbessert, doch es gibt immer noch Unsicherheiten, die nicht jeder
Freifunker eingehen will. Um diese Unsicherheiten vom einzelnen User zu
nehmen und eine Isolierung des Freifunkdatenstromes vom Datenstrom des
Anschlusseigentümers zu ermöglichen, hat die Freifunk-Community Berlin
eine neue Tunnellösung geschaffen.

Als neue Technik nutzen wir Tunneldigger. Tunneldigger wurde von
Wlan-Slovenija entwickelt und wird bereits von einigen anderen
Freifunk-Communities genutzt.

Tunneldigger hat den Vorteil, dass es im Vergleich zu OpenVPN
ressourcenschonender ist. Wir brauchen somit weniger Flash, weniger CPU
auf den Routern und auch kein Zertifikat mehr.

notunnel

Idealerweise sollte jeder Freifunker, der Bandbreite für einen
Internet-Uplink übrig hat, diese Kapazität anderen Nutzern zur Verfügung
stellen. Ein Betreiber von offenem WLAN kann nun weder kostenpflichtig
abgemahnt noch schadenersatzpflichtig gemacht werden, siehe §8 (3)
Telemediengesetz.

Die notunnel-Firmware leitet den Datenverkehr nicht durch einen Tunnel.
Stattdessen wird er direkt ins Internet ausgeleitet. Wer sich für den
Betrieb ohne Tunnel entscheidet und doch noch Abmahnungen bekommt, kann
entweder den Abmahnbeantworter benutzen oder sich an den Förderverein
wenden.

Erfahre mehr über deine Rechte unter https://freifunkstattangst.de.

backbone

Das Image für die, die manuell konfigurieren wollen. Der
Einrichtungsassistent und OpenVPN fehlen, dafür sind mehr
Debugging-Netzwerktools verfügbar.

tunnel-berlin-tunneldigger (Standard)

Das direkte Ausleiten des Freifunk-Datenstromes über den eigenen
Anschluss war in Deutschland lange Zeit durch die Störerhaftung
erschwert. Die rechtliche Situation hat sich 2017 hier deutlich
verbessert, doch es gibt immer noch Unsicherheiten, die nicht jeder
Freifunker eingehen will. Um diese Unsicherheiten vom einzelnen User zu
nehmen und eine Isolierung des Freifunkdatenstromes vom Datenstrom des
Anschlusseigentümers zu ermöglichen, hat die Freifunk-Community Berlin
eine neue Tunnellösung geschaffen.

Als neue Technik nutzen wir Tunneldigger
(https://wiki.freifunk.net/Tunneldigger). Tunneldigger wurde von
Wlan-Slovenija (<https://wlan-si.net/>) entwickelt und wird bereits von
einigen anderen Freifunk-Communities genutzt.

Tunneldigger hat den Vorteil, dass es im Vergleich zu OpenVPN
ressourcenschonender ist. Wir brauchen somit weniger Flash, weniger CPU
auf den Routern und auch kein Zertifikat mehr.

notunnel

Idealerweise sollte jeder Freifunker, der Bandbreite für einen
Internet-Uplink übrig hat, diese Kapazität anderen Nutzern zur Verfügung
stellen. Ein Betreiber von offenem WLAN kann nun weder kostenpflichtig
abgemahnt noch schadenersatzpflichtig gemacht werden, siehe §8 (3)
Telemediengesetz.

Die notunnel-Firmware leitet den Datenverkehr nicht durch einen Tunnel.
Stattdessen wird er direkt ins Internet ausgeleitet. Wer sich für den
Betrieb ohne Tunnel entscheidet und doch noch Abmahnungen bekommt, kann
entweder den Abmahnbeantworter (<https://abmahnbeantworter.ccc.de/>)
benutzen oder sich an den Förderverein
(<https://foerderverein.freie-netzwerke.de/kontakt/>) wenden.

Erfahre mehr über deine Rechte unter https://freifunkstattangst.de.

backbone

Das Image für die, die manuell konfigurieren wollen. Der
Einrichtungsassistent und OpenVPN fehlen, dafür sind mehr
Debugging-Netzwerktools verfügbar.

Seit Falter ist es möglich, schnell Images für jedes Gerät zu erzeugen,
das von OpenWrt unterstützt wird. Bitte schaue dir dazu die Seite Falter
Firmware selber bauen an sofern Du mit Softwareerstellung vertraut bist.
In einem späteren Kapitel wird beschrieben, wie man die Software selbst
kompilieren kann, sofern OpenWrt auf dem Target läuft, ausreichend
freier Speicher verfügbar ist und man über entsprechende Kenntnisse
verfügt.
https://wiki.freifunk.net/Berlin:Tutorials/Falter\_Firmware\_selber\_bauen

Neue Page
\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#

<https://wiki.freifunk.net/Berlin:Firmware#Unterst.C3.BCtzte_Router>

Abschnitt Hinweise zur Firmware (historisch) -- Abschnitt/liste aus der
Quelle mit den Links direkt übernommen (Lizenz CC BY-SA 3.0)

**Hinweise zur Firmware (historisch), **[]{#anchor}**Releases**

Hedy 1.0.4, 2019-06-26

> [README](https://wiki.freifunk.net/index.php?title=Berlin:Firmware/v1.0.4&action=edit&redlink=1),
> [CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v1.0.4/CHANGELOG.md),
> Download der Firmware siehe Links in der [Tabelle
> oben](https://wiki.freifunk.net/Berlin:Firmware#Unterst.C3.BCtzte_WLAN-Router),
> für Entwickler: [alle
> Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/1.0.4/)

Hedy 1.0.3, 2019-05-31

> [README](https://wiki.freifunk.net/Berlin:Firmware/v1.0.3),
> [CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v1.0.3/CHANGELOG.md),
> [alle
> Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/1.0.3/)

Hedy 1.0.2, 2019-01-21

> [README](https://wiki.freifunk.net/Berlin:Firmware/v1.0.2),
> [CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v1.0.2/CHANGELOG.md),
> [alle
> Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/1.0.2/)

Hedy 1.0.1, 2018-05-29

> [README](https://github.com/freifunk-berlin/firmware/blob/v1.0.1/README.md),
> [CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v1.0.1/CHANGELOG.md),
> [alle
> Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/1.0.1/),
> [Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2018-May/037868.html)

> Die Software hat sich gegenüber Hedy 1.0.0 nicht geändert, es ist
> jetzt aber ein Upgrade von Kathleen zur VPN03-Variante möglich.

Hedy 1.0.0, 2018-02-26

> [README](https://github.com/freifunk-berlin/firmware/blob/v1.0.0/README.md),
> [CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v1.0.0/CHANGELOG.md),
> [alle
> Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/1.0.0/),
> [Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2018-February/037118.html)

> Dieses Release sollte nur auf Routern installiert werden, die komplett
> neu aufgesetzt werden

Kathleen 0.3.0, 2017-04-10

> [README](https://github.com/freifunk-berlin/firmware/blob/v0.3.0/README.md),
> [CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v0.3.0/CHANGELOG.md),
> [alle
> Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/0.3.0/),
> [Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2017-April/035492.html)

Kathleen 0.2.0, 2016-11-27

> [README](https://github.com/freifunk-berlin/firmware/blob/v0.2.0/README.md),
> [CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v0.2.0/CHANGELOG.md),
> [alle
> Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/0.2.0/),
> [Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2016-November/034719.html)

Kathleen 0.1.2, 2015-07-02

> [README](https://github.com/freifunk-berlin/firmware/blob/v0.1.2/README.md),
> [CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v0.1.2/CHANGELOG.md),
> [alle
> Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/0.1.2/),
> [Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2015-July/028638.html)

Kathleen 0.1.1, 2015-05-30

> [README](https://github.com/freifunk-berlin/firmware/blob/v0.1.1/README.md),
> [CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v0.1.1/CHANGELOG.md),
> [alle
> Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/0.1.1/),
> [Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2015-May/028249.html)

Kathleen 0.1.0, 2015-02-19

> [README](https://github.com/freifunk-berlin/firmware/blob/v0.1.0/README.md),
> [CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v0.1.0/CHANGELOG.md),
> [alle
> Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/0.1.0/),
> [Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2015-February/027330.html)

> Router mit 4MB Flash (insbesondere WR841) werden von dieser Version
> nicht unterstützt.

> [\#217](https://github.com/freifunk-berlin/firmware/issues/217) (s.u.)
> ist nicht richtig gefixt.

Kathleen 0.0.0, 2014-10-29

> [README](https://github.com/freifunk-berlin/firmware/blob/0.0.0/README.md),
> [CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/0.0.0/CHANGELOG.md),
> [alle
> Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/0.0.0/),
> [Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2014-October/025802.html)

> [\#191](https://github.com/freifunk-berlin/firmware/issues/191): Auf
> Routern mit 4MB Flash (u.a. TP-Link WR841) läuft das Dateisystem
> schnell voll, Rekonfiguration mit \"Save&Apply\" funktioniert dann
> nicht.

[\#217](https://github.com/freifunk-berlin/firmware/issues/217):
Monitoring/collectd macht wenigstens in einigen Setups Probleme
(Speicherleck, Reboots des Routers alle paar Stunden). Bei Routern mit
nur 32MB RAM (TP-Link WR842, WR1043 v1) das Monitoring am besten
abschalten.

For English scrool down!
\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#

Berlin Freifunk: Technology/Firmware

Technology

In the section "Getting involved"
<https://berlin.freifunk.net/de/participate/> it was already mentioned
that you become a Freifunker when you set up a Freifunk router and make
it available to others. Freifunk is sometimes abbreviated as FF. A
Freifunk network consists of a large number of wireless connections, as
the term "network" suggests. The meshes of the network are formed by
long-range directional antennas for uplink to a hub and shorter-range
omnidirectional antennas. There is also a small-scale network with
connections to other nearby nodes. Your Freifunk router can become part
of it and strengthen the network. As a "grassroots movement", the
Freifunk community uses special software, as do many other
community-operated networks that are owned by users. This software must
be adapted to the hardware used by the various manufacturers. This
customized software is referred to as "Firmware". For different
hardware, special, adapted software/firmware is required that can only
be executed on the appropriate hardware; this is called "runnable".
