Berlin Freifunk: Technologie/Firmware

Technology In the "Participate" section
https://berlin.freifunk.net/de/participate/ it was already mentioned
that you become a Freifunker when you set up a Freifunk router and make
it available to others. In general, a router is a prerequisite for
access to the Internet.

![](Pictures/100000000000050C00000384690D3E5382772C44.png){width="17cm"
height="11.841cm"}Bildquelle:
<https://commons.wikimedia.org/wiki/File:03-freiffunk-router-mit-gaesten2.png>

Freifunk is sometimes abbreviated as FF. A Freifunk network consists of
a large number of wireless connections, as the term "network" suggests.
The meshes of the network are formed by long-range directional antennas
for uplink to a hub and shorter-range omnidirectional antennas. There is
also a small-scale network with connections to other nearby nodes. Your
Freifunk router can become part of it and strengthen the network.

![](Pictures/10004F2E0000FA9C00006E49047AA695E2B23C62.svg){width="17cm"
height="7.481cm"}Bildquelle:
https://commons.wikimedia.org/wiki/File:Freifunk\_Mesh.svg

The Freifunk community as a "grassroots movement" owns the
community-operated network and uses special software, as do many other
similar communities. This software must be adapted to the hardware used
by the various manufacturers. This customized software is referred to as
"Firmware". For different hardware, special, adapted software/firmware
is required that can only be executed on the appropriate hardware; this
is called "runnable".

The current Berlin Freifunk firmware is called falter and was released
in spring 2021. The firmware is constantly being improved, resulting in
a new version with a new name. Each Freifunk community usually uses its
own firmware that only works in the respective local community.

All of them are based on the open source Linux version OpenWrt
(https://de.wikipedia.org/wiki/Open\_Source), which is optimized for
Internet support. Further information about the OpenWrt project
organization can be found on the "About OpenWrt" pages
(https://openwrt.org/). For software developers, OpenWrt serves as a
so-called "framework". Such a framework provides a software basis and
thus helps in creating an application. The developer of an application
can access it and does not have to laboriously create a complete
software environment himself.

![](Pictures/1000000100000A00000002BF187B81FF249E4BF4.png){width="17cm"
height="4.667cm"}

However, no in-depth detailed knowledge is necessary to get started with
Freifunk because only the firmware created and provided by developers is
used.

People often ask why there is no Freifunk software available for this or
that router? Individual, unsuitable types of processors or too little
memory prevent the implementation of OpenWrt on some devices. Without
OpenWrt and sufficient free memory, there is no Freifunk firmware, quite
simply. In addition, you need to find someone to carry out the task,
implement software for a router, also quite simple. Therefore, Freifunk
firmware is not offered for all routers from the OpenWrt list. A later
chapter describes how you can compile the software yourself, provided
OpenWrt is running on the target and you have the appropriate knowledge.

New Page
\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#

Firmware/Image

As already mentioned, support for OpenWrt is a prerequisite for
implementing Falter on a potential Freifunk router. Since Falter is
based on OpenWrt, OpenWrt\'s "Table of Hardware" can be used as the
first criterion for supported hardware. If you are interested, you can
find information about the devices supported by OpenWrt at
(https://openwrt.org/supported\_devices). This often answers some
questions about why the Freifunk software is not offered for certain
routers. Without OpenWrt there is no Freifunk software.

You can download ready-made images for the most common routers from the
Freifunk firmware selector. The list
https://selector.berlin.freifunk.net/ provides information as to whether
the FF firmware is available if you already have a router. If you are
planning a purchase, I would recommend one on the list to be sure to get
the Freifunk firmware. This can be checked by entering the manufacturer
and the type designation in the search line. If the result is positive,
the appropriate firmware can be downloaded there, but only if it is
available according to the list. It is important to pay attention to the
version number. A different version number means changes to the
router\'s hardware by the manufacturer, which may prevent implementation
of the Freifunk firmware.

Tip: Before you buy hardware, inquire about pool devices that are
available on Freifunk on the mailing list and in the chat. We have
technology on the shelves waiting to be used! :-)

When buying a new router from large shipping companies, the version
number is often not specified in the offer; the latest model is usually
delivered with the latest version. It then often turns out that this
model with a higher version number is not in the compatibility list. The
FF software can work on this model, but this does not necessarily have
to be the case. Often a careless attempt will result in the new router
being bricked and rendered unusable.

Tip: On eBay, routers are often offered with a version number (cheap),
which can be a safe alternative to blindly buying the latest router with
an unknown version number - at least at the beginning.

In order to make the router FF-compatible, the appropriate FF firmware
must be "flashed" onto the router. Through so-called "flashing", the
manufacturer's firmware, which is located in a rewritable memory, is
completely replaced by the Freifunk firmware. Such a finished firmware
package for a listed router is called an image. The firmware, the image,
comes in different versions. You should know the differences between
them to choose the right firmware for you. A general distinction is made
between factory images and sysupgrade images. Factory images are only
used when flashing the router for the first time, i.e. when flashing
from the original firmware to the Freifunk firmware, i.e. during the
initial installation. Sysupgrade images update to a new version if FF
software is already installed on the device. However, there are
exceptions; details on how exactly it works with your router can be
found in the OpenWrt Wiki (https://openwrt.org/toh/start) on the article
page for your router model.

It should be warned in advance that flashing the wrong firmware version
can make the router unusable - this is called \"bricking\". So care is
required. Occasionally a repair is possible, but unfortunately not
always for all makes.

The installation and flashing of the firmware/image is described in a
separate section. Firmware/Howto
<https://wiki.freifunk.net/Berlin:Firmware/HowTo>.

The "Image Types" section was slightly shortened from
<https://wiki.freifunk.net/Berlin:Firmware#Unterst.C3.BCtzte_Router> ,
copyright is CC BY-SA 3.0

Image types:

tunnel-berlin-tunneldigger (standard)

Direct routing of the Freifunk data stream via your own connection was
made difficult in Germany for a long time due to liability for
interference. The legal situation improved significantly here in 2017,
but there are still uncertainties that not every Freifunker wants to
accept. In order to remove these uncertainties from the individual user
and to enable the Freifunk data stream to be isolated from the
connection owner\'s data stream, the Freifunk Community Berlin has
created a new tunnel solution.

FF uses tunnel diggers as a new technology. Tunneldigger was developed
by Wlan-Slovenija and is already used by several other Freifunk
communities. Tunneldigger has the advantage that it is more
resource-efficient compared to OpenVPN. We therefore need less flash,
less CPU on the routers and no more certificate.

notunnel

Ideally, every Freifunker who has bandwidth left over for an Internet
uplink should make this capacity available to other users. An operator
of open WLAN can now neither be warned with a fee nor be held liable for
damages, see Section 8 (3) of the Telemedia Act.

The notunnel firmware does not route traffic through a tunnel. Instead,
it is sent directly to the Internet. Anyone who decides to operate
without a tunnel and still receives warnings can either use the warning
responder (<https://abmahnbeantworter.ccc.de/>)

or contact the support
association(<https://foerderverein.freie-netzwerke.de/kontakt/>) .

Find out more about your rights at
[https://freifunkstattangst.de](https://freifunkstattangst.de/) .

backbone

The image for those who want to configure manually. The setup wizard and
OpenVPN are missing, but more debugging network tools are available.
Since Falter, it has been possible to quickly create images for any
device supported by OpenWrt. Please take a look at the page Building
your own Falter firmware if you are familiar with software creation. A
later chapter describes how you can compile the software yourself,
provided OpenWrt is running on the target, there is enough free memory
available and you have the appropriate knowledge.
<https://wiki.freifunk.net/Berlin:Tutorials/Falter_Firmware_selber_machen>

New Page
\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#

<https://wiki.freifunk.net/Berlin:Firmware#Unterst.C3.BCtzte_Router>

Abschnitt Hinweise zur Firmware (historisch) -- Abschnitt/liste aus der
Quelle mit den Links direkt übernommen (Lizenz CC BY-SA 3.0)

**Hinweise zur Firmware (historisch), **[]{#anchor}**Releases**

Hedy 1.0.4, 2019-06-26

[README](https://wiki.freifunk.net/index.php?title=Berlin:Firmware/v1.0.4&action=edit&redlink=1),
[CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v1.0.4/CHANGELOG.md),
Download der Firmware siehe Links in der [Tabelle
oben](https://wiki.freifunk.net/Berlin:Firmware#Unterst.C3.BCtzte_WLAN-Router),
für Entwickler: [alle
Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/1.0.4/)

Hedy 1.0.3, 2019-05-31

[README](https://wiki.freifunk.net/Berlin:Firmware/v1.0.3),
[CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v1.0.3/CHANGELOG.md),
[alle
Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/1.0.3/)

Hedy 1.0.2, 2019-01-21

[README](https://wiki.freifunk.net/Berlin:Firmware/v1.0.2),
[CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v1.0.2/CHANGELOG.md),
[alle
Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/1.0.2/)

Hedy 1.0.1, 2018-05-29

[README](https://github.com/freifunk-berlin/firmware/blob/v1.0.1/README.md),
[CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v1.0.1/CHANGELOG.md),
[alle
Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/1.0.1/),
[Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2018-May/037868.html)

Die Software hat sich gegenüber Hedy 1.0.0 nicht geändert, es ist jetzt
aber ein Upgrade von Kathleen zur VPN03-Variante möglich.

Hedy 1.0.0, 2018-02-26

[README](https://github.com/freifunk-berlin/firmware/blob/v1.0.0/README.md),
[CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v1.0.0/CHANGELOG.md),
[alle
Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/1.0.0/),
[Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2018-February/037118.html)

Dieses Release sollte nur auf Routern installiert werden, die komplett
neu aufgesetzt werden

Kathleen 0.3.0, 2017-04-10

[README](https://github.com/freifunk-berlin/firmware/blob/v0.3.0/README.md),
[CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v0.3.0/CHANGELOG.md),
[alle
Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/0.3.0/),
[Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2017-April/035492.html)

Kathleen 0.2.0, 2016-11-27

[README](https://github.com/freifunk-berlin/firmware/blob/v0.2.0/README.md),
[CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v0.2.0/CHANGELOG.md),
[alle
Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/0.2.0/),
[Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2016-November/034719.html)

Kathleen 0.1.2, 2015-07-02

[README](https://github.com/freifunk-berlin/firmware/blob/v0.1.2/README.md),
[CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v0.1.2/CHANGELOG.md),
[alle
Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/0.1.2/),
[Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2015-July/028638.html)

Kathleen 0.1.1, 2015-05-30

[README](https://github.com/freifunk-berlin/firmware/blob/v0.1.1/README.md),
[CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v0.1.1/CHANGELOG.md),
[alle
Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/0.1.1/),
[Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2015-May/028249.html)

Kathleen 0.1.0, 2015-02-19

[README](https://github.com/freifunk-berlin/firmware/blob/v0.1.0/README.md),
[CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/v0.1.0/CHANGELOG.md),
[alle
Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/0.1.0/),
[Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2015-February/027330.html)

Router mit 4MB Flash (insbesondere WR841) werden von dieser Version
nicht unterstützt.

[\#217](https://github.com/freifunk-berlin/firmware/issues/217) (s.u.)
ist nicht richtig gefixt.

Kathleen 0.0.0, 2014-10-29

[README](https://github.com/freifunk-berlin/firmware/blob/0.0.0/README.md),
[CHANGELOG](https://github.com/freifunk-berlin/firmware/blob/0.0.0/CHANGELOG.md),
[alle
Firmware-Images](https://buildbot.berlin.freifunk.net/buildbot/stable/0.0.0/),
[Announcement](https://lists.berlin.freifunk.net/pipermail/berlin/2014-October/025802.html)

[\#191](https://github.com/freifunk-berlin/firmware/issues/191): Auf
Routern mit 4MB Flash (u.a. TP-Link WR841) läuft das Dateisystem schnell
voll, Rekonfiguration mit \"Save&Apply\" funktioniert dann nicht.

[\#217](https://github.com/freifunk-berlin/firmware/issues/217):
Monitoring/collectd macht wenigstens in einigen Setups Probleme
(Speicherleck, Reboots des Routers alle paar Stunden). Bei Routern mit
nur 32MB RAM (TP-Link WR842, WR1043 v1) das Monitoring am besten
abschalten.
