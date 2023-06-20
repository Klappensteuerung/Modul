# Steuerung der Abgasklappe Yamaha Motorräder
![Projektbild](https://github.com/Klappensteuerung/Modul/assets/137152396/a1f806ea-ef26-4ccf-acbd-f1d66fa5db1f)
Kontakt:

[per Mail](mailto:klappensteuerung@web.de?subject=[GitHub]Klappensteuerung)

## Die Idee


Die Idee, welche hinter dem Klappenmodul steckt, ist recht simpel erklärt. Ich wollte ein Modul erstellen, welche unabhängig der Motordrehzahl die Abgasklappe betätigen kann ohne einen Fehler im Dashboard meines Motorrads
zu generieren. Dabei war es mir wichtig, eine Platine zu haben, welche einen geringen Bauraum aufweißt und wirklich Plug and Play ins Motorrad eingebaut werden kann. Nach vielen Versionen ist am Ende eine Platine entstanden
die dem Motorrad eine Abgasklappe simuliert und welche über die Nachrichten welche über das Can-Bus gesendet werden gesteuert werden kann. 

## Features

Durch den lesenden Zugriff auf das Can-Bus ist das Modul in der Lage auf jede Einstellung im Dashboard zu reagieren und die Abgasklappe zu fahren. Unterschieden kann das Verhalten der Abgasklappe in zwei Modi. Der 
Standardmodus wo die Klappe wie im Standard des jeweiligen Motorrades gefahren wird und der offene Modus. Im offenen Modus ist die Auspuffklappe permanent offen, unabhängig von weiteren Gegebenheiten.

Durch diese Freiheit ist man in der Lage abhängig der Situation die Klappe im Standardmodus oder im offenen Modus zu verwenden. Hierbei denke ich primär an Rennstrecke (offen) oder Stadtdurchfahrten (standard).

Zu bedenken ist, dass ein Motorrad auf den Gegendruck der Abgasklappe abgestimmt und programmiert worden ist. Jede Abweichung der Abgasklappe zur vorgesehenen Stellung stellt eine Veränderung der Abgaswerte dar und ist nicht im Straßenverkehr zugelassen. Desweiteren kann es bei bestimmten Umständen zu einem Motorschaden führen.

## Motor

Wie bereits erwähnt kann es unter bestimmten Umständen zu einem Motorschaden führen. Die beigefügte Erklärung basiert auf einer Yamaha R1 RN65, gilt jedoch bestimmt auch für andere Motorräder von Yamaha.

In folgender Erklärung gehen wir von einer Abgasklappe aus, welche immer offen ist. 

Situation 1: Umdrehungen im Bereich wo die Klappe im Standard offen wäre -> Keinen unterschied zum Standard daher keine veränderung der Abgaswerte

Situation 2: Umdrehung mit geschlossener Klappe und unter 50% Gas -> Unter 50% wird das Abgasgemisch anhand der Lamda angepasst -> Abgaswerte sind in Ordnung

Situation 3: Umdrehung mit geschlossener Klappe und über 50% Gas -> Über 50% wird eine feste Einspritztabelle genommen wodurch der Motor zu mager oder zu fett läuft. In dieser Situation könnte ein Motorschaden auftreten, jedoch ist zu bedenken, dass ein Motor in dieser Situation, durch schnelle erhöhung der Drehzahl und erreichen der Situation 1, nie lange betrieben werden kann. 

## Konfiguration

Damit das Modul weiß welche Can-Bus Nachricht für Ihn relevant ist, muss diese vor dem Programmieren definiert werden. Grundsätzlich kann gesagt werden, dass jede Einstellung aus dem Dashboard zum Steuern des Modul möglich ist. 

z.B.

PWR 1-2 -> Klappen offen
PWR 3 -> Standard

oder 

TCS 0-3 -> Klappen offen
Rest -> Standard

usw. usw.
