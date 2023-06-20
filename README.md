# Steuerung der Abgasklappe Yamaha Motorräder

Kontakt:

Die Idee

Die Idee, welche hinter dem Klappenmodul steckt, ist recht simpel erklärt. Ich wollte ein Modul erstellen, welche unabhängig der Motordrehzahl die Abgasklappe betätigen kann ohne einen Fehler im Dashboard meines Motorrads
zu generieren. Dabei war es mir wichtig, eine Platine zu haben, welche einen geringen Bauraum aufweißt und wirklich Plug and Play ins Motorrad eingebaut werden kann. Nach vielen Versionen ist am Ende eine Platine entstanden
die dem Motorrad eine Abgasklappe simuliert und welche über die Nachrichten welche über das Can-Bus gesendet werden gesteuert werden kann. 

Features

Durch den lesenden Zugriff auf das Can-Bus ist das Modul in der Lage auf jede Einstellung im Dashboard zu reagieren und die Abgasklappe zu fahren. Unterschieden kann das Verhalten der Abgasklappe in zwei Modi. Der 
Standardmodus wo die Klappe wie im Standard des jeweiligen Motorrades gefahren wird und der offene Modus. Im offenen Modus ist die Auspuffklappe permanent offen, unabhängig von weiteren Gegebenheiten.

Konfiguration

Damit das Modul weiß welche Can-Bus Nachricht für Ihn relevant ist, muss diese vor dem Programmieren definiert werden. Grundsätzlich kann gesagt werden, dass jede Einstellung aus dem Dashboard zum Steuern des Modul möglich ist. 

z.B.

PWR 1-2 -> Klappen offen
PWR 3 -> Standard

oder 

TCS 0-3 -> Klappen offen
Rest -> Standard

usw. usw.
