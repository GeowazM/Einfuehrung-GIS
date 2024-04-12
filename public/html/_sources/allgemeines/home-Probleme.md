# Was tun bei Problemen?  
Im Rahmen eurer Arbeiten mit der GIS Software kann es zu Problemen verschiedenster Art kommen:  
* Euch wird eine Fehlermeldung angezeigt
* Werkzeuge funktionieren nicht oder frieren während der Durchführung ein
* QGIS stürzt wiederholt ab
* Ihr könnt eine bestimmte Funktion oder ein Werkzeug nicht finden
* Ihr habt Verständnisfragen zu Aufgabenstellungen
* ...

In diesem Kapitel erfahrt ihr, wie mit solchen Komplikationen umzugehen ist. Der wichtigste Tipp aber gleich zu Beginn: **Plant bei eurem Zeitmanagement das Auftreten von Problemen ein!** Wer erst ein oder zwei Tage vor der Deadline mit der Aufgabe beginnt, muss sich nicht wundern wenn er bei einem Problem nicht mehr rechtzeitig Hilfe bekommt.

## Probleme selbstständig lösen
Euch stehen eine Reihe an Möglichkeiten bereit, mit denen ihr eure Probleme selbstständig in den Griff bekommen könnt.   

**1) Das Wiki**  
Eure erste Anlaufstelle. Aus den Erfahrungen der letzten Semester lässt sich sagen, dass etwa zwei Drittel aller Fragen, die im Rahmen der Issues und den Übungsgruppen an die TutorInnen gestellt wurden, bereits mit den Informationen aus dem Wiki beantwortet werden konnten. Seitdem wurde das Wiki nochmals erneut überarbeitet, sodass nun noch mehr Fehlerquellen und Fragestellungen abgedeckt werden.

**2) Bestehende Issues**  
Sollte auch nach intensiver Recherche im Wiki keine Lösung für euer Problem zu finden sein, könnt ihr einen Blick in die bestehenden [Issues](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/issues) werfen. Beachtet dabei, dass es neben der Kategorie [open](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/issues?scope=all&utf8=%E2%9C%93&state=opened) (Problemlösung noch nicht abgeschlossen) auch noch eine Kategorie [closed](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/issues?scope=all&utf8=%E2%9C%93&state=closed) (Problemlösung abgeschlossen) gibt.

**3) Internetforen & Videotutorials**  
Solltet ihr auch in den bereits vorhandenen Issues nicht fündig geworden sein, lohnt sich eine Internetrecherche. Zu vielen Themengebieten gibt es Videotutorials oder Foreneinträge. Hierher beziehen auch die TutorInnen hauptsächlich ihre Lösungen zu komplizierteren Problemfällen - und das könnt ihr auch! Tipp: Es empfiehlt sich auf Englisch zu recherchieren.

Bei Fragen zu Funktionsweisen von Tools oder Schaltflächen finden sich außerdem auch ausführliche Informationen in den Online-Dokumentationen von QGIS (https://www.qgis.org/en/docs/index.html) und ArcGIS (https://desktop.arcgis.com/de/arcmap/).

## Hilfe bei Problemen einholen  
Solltet ihr es nicht schaffen, euer Problem selbstständig zu lösen, könnt ihr euch Hilfe von den TutorInnen oder anderen Studierenden holen. Dies kann auf zwei Arten geschehen. Beide haben ihre eigenen Vor- und Nachteile.  

**1) TutorInnen in den Übungsgruppen fragen**  
In den wöchentlich stattfindenden Übungsgruppen wird euch immer die Zeit eingeräumt, Fragen zu stellen. Wenn ihr ein Problem also möglichst schnell lösen müsst, ist der Besuch des Tutoriums zu empfehlen. Beachtet, dass ihr keiner festen Übungsgruppe zugewiesen seit und somit in jeder Gruppe eure Fragen stellen könnt. Die Uhrzeiten aller Übungsgruppen findet ihr im LSF.  
Seid euch jedoch bewusst, dass den TutorInnen im Rahmen der Übungsgruppe nur begrenzt Zeit zur Verfügung steht, um auf euer Problem einzugehen. Auch ein/e Tutor/in ist nicht allwissend und muss sich gegebenenfalls erst selbst über einen Lösungsansatz informieren. Auch ist zu beachten, dass im Tutorium nur ein kleiner Anteil eurer KommilitonInnen die Möglichkeit hat, von euren Fragen zu profitieren. Dadurch kann es oft vorkommen, dass in mehreren Übungsgruppen die gleichen Probleme geschildert werden. Um dies zu verhindern, kann euch ein/e Tutor/in nach der Behebung eures Problems bitten, ein Issue mit dem Lösungsweg für alle zu erstellen.

**2) Neues Issue verfassen**  
Alternativ zu den Übungsgruppen könnt ihr eure Fragen auch in einem Issue formulieren. Dadurch können alle KommilitonInnen von der Problemlösung profitieren und die TutorInnen haben bei Bedarf die Möglichkeit, selbst zu recherchieren bevor sie euch antworten. Zumindest unter der Woche ist gewährleistet, dass die TutorInnen das GitLab täglich auf neue Issues überprüfen, ihr solltet also in einem angemessenen Zeitrahmen eine Antwort erhalten (Das soll nicht heißen, dass es nicht möglich ist auch am Wochenende eine Antwort zu bekommen). Wie gewinnbringend die Antworten auf Issues ausfallen können, ist stark abhängig von deren Qualität. Je mehr Informationen ihr von Beginn an bereitstellt, desto weniger Nachfragen müssen getätigt werden und desto schneller kann euer Problem gelöst werden. Eine genaue Anleitung zum Erstellen eines Issues findet ihr im folgenden Kapitel.

**Hinweis:**  
Bitte beschränkt euch zwecks Problemlösungen auf diese beiden Wege der Kommunikation. Whatsapp-Gruppen, Emails an die TutorInnen oder Ähnliches sind nicht für alle KommilitonInnen einzusehen und erzeugen somit einen Mehraufwand, da eine Fragestellung so unter Umständen mehrmals beantwortet werden muss. Auch die Kommunikation zwischen euch Studierenden kann über die Issues in GitLab verlaufen. Damit unterstützt ihr eure KommilitonenInnen, sowie die TutorInnen gleichermaßen.

## Anleitung zum Erstellen eines Issues  
**Checkliste:**  
Bevor ihr ein neues Issue verfasst, vergewissert euch erneut alle Punkte auf folgender Checkliste erfüllt zu haben:  
* Es wird eine [vom Wiki empfohlene Version](/content/gis/allgemeines/qgis-Installation) von QGIS verwendet.
* Alle [Hinweise](/content/gis/allgemeines/Hinweise) wurden berücksichtigt.
* Das Problem ist nicht in den [häufigen Fragen](home-Häufige Fragen und Fehlerquellen) zu finden und alle darin genannten Fehlerquellen wurden überprüft.
* Alle Wiki-Artikel zu dem jeweiligen Themengebiet wurden gelesen (Die Themengebiete sind immer der Exercise zugeordnet in denen sie zuerst verwendet wurden).
* Es wurde sich zum Zeitpunkt des Verfassens des Issues erneut vergewissert, dass nicht bereits ein Issue zur bestehenden Problematik existiert (Nur die Überschriften scannen ist nicht ausreichend! Es müssen mindestens die Inhalte aller Issues zur jeweiligen Exercise/Abgabe inspiziert werden.).

**_New Issue_-Interface**  
![gitlab_new_issue_interface](https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/3fe93f58711c16ca2c9e853d5c9bbaf0/New_Issue.JPG)

**1) Titel**  
Wählt einen kurzen und prägnanten Titel für euer Issue aus mit der euer Problem ersichtlich und von KommilitonInnen leicht gefunden werden kann. Im Titel muss nicht die Abgabe/Exercise genannt werden. Die Zuordnung geschieht über die Labels (siehe unten).

**2) Template**  
Im Dropdown-Menü mit der Aufschrift 'Choose a template' wählt ihr 'Informationen Checkliste' aus. Dadurch wird euch im _Description_-Fenster ein voreingestellter Text angezeigt, der als Leitfaden für die Erstellung des Issues dient.

**3) Description**  
In diesem Fenster sollt ihr eure Problematik möglichst genau beschreiben. Je mehr Informationen ihr bietet und desto genauer ihr das Problem eingrenzen könnt, desto effizienter kann euch geholfen werden. Orientiert euch an den Leitfragen des Templates. Die Überschriften des Templates können für eine bessere Gliederung beibehalten werden. Der sonstige Text dient jedoch nur für euch als Erinnerung und soll durch eure Beschreibungen ersetzt bzw. gelöscht werden, bevor ihr das Issue veröffentlicht.

**4) Attach a file**  
"Manche Bilder sagen mehr als tausend Worte". Über diese Schaltfläche könnt ihr Bilder/Screenshots in euer Issue implementieren. Nach dem Hochladen wird im Eingabefeld eine Codezeile erzeugt. Diese könnt ihr im Anschluss markieren, ausschneiden und an der gewünschten Stelle in eurem Text einfügen. Achtet darauf, die Bilder in guter Auflösung und Größe hochzuladen, sodass man möglichst viele Informationen erkennen kann. Fasst nicht mehrere Bilder als PDF zusammen, sondern ladet jedes Bild einzeln hoch. Ansonsten muss man umständlich die PDF öffnen, statt direkt die Bilder im bzw. unter dem Text sehen zu können.

**5) Labels**  
In diesem Dropdown-Menü könnt ihr euer Issue mit Labeln versehen. Diese werden in der Auflistung aller Issues unter eurem Titel angezeigt und ermöglichen dadurch eine schnellere Suche. Man kann sogar direkt nach bestimmten Labels suchen. Verpflichtend sind die Label 'Abgabe X' bzw. 'Exercise X' um die Zugehörigkeit eures Issues zu einer Aufgabenstellung zu kennzeichnen, sowie das Label 'QGIS' bzw. 'ArcGIS' um anzugeben, mit welchem GIS Programm ihr gearbeitet habt.

**6) Preview**  
Bevor ihr euer Issue absendet, könnt ihr euch in der Preview das derzeitige Layout eures Textes, wie er nachher von anderen gesehen wird, ansehen. In diesem Schritt sollte auch nochmals abschließend überprüft werden, ob alle Leitfragen und Hinweise des Templates entfernt wurden. Die Beschreibung eures Issues ist in _Markdown_ geschrieben. Die dazugehörige Syntax lässt sich zum Beispiel [hier](https://www.markdownguide.org/basic-syntax/) in wenigen Minuten erlernen (Es reicht ja nur die Abschnitte des Guides zu lesen, die für euer Layouting-Wünsche benötigt werden). Der Aufwand lohnt sich, ein übersichtlicheres Issue kann deutlich leichter und schneller bearbeitet werden.

## Beispiel zum Erstellen eines Issues
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/5138b315a80fa43e49ef24ef97b24592/Issue_erstellen_Beispiel.mp4"></video>

* Beim Eintippen des Titels ist im Video zu sehen, dass Issues mit ähnlichen Titeln angezeigt werden. Dies bietet einem erneut die Möglichkeit Themendopplungen zu vermeiden.
* Die Beschreibung im Beispiel ist sehr minimalistisch. In diesem Fall geht das in Ordnung, da eine Fehlermeldung als Screenshot zur Verfügung gestellt werden konnte, sowie der Zeitpunkt des Auftretens dieser Fehlermeldung genau bestimmt ist.
* Aufmerksame Leser der [Hinweise](/content/gis/allgemeines/Hinweise) können zudem feststellen, dass das Erstellen des Issues nicht gerechtfertigt ist, da die Befolgung des Hinweises zu [GRASS Anwendungen](/content/gis/allgemeines/Hinweise.md#grass-anwendungen) das Problem bereits beheben würde.

## Nach erfolgreicher Problemlösung
Solltet ihr für euer Problem eine Lösung gefunden haben (entweder selbstständig oder durch eine Antwort in eurem Issue), dann teilt diese Lösung unbedingt als neuen Kommentar in eurem Issue mit. Dadurch können KommilitonInnen mit dem gleichen Problem sofort nachlesen, welcher Lösungsweg funktioniert hat. Gleichzeitig dient euer Kommentar mit dem Lösungsweg auch als Feedback für die TutorInnen, dass ein Issue vollständig behoben wurde und somit geschlossen werden kann.  
Sollte von euch keine Rückmeldung zu einem vorgeschlagenen Lösungsweg mehr kommen, werden die TutorInnen nach etwa einer Woche das Issue als erledigt ansehen und schließen. Auch wenn ihr den Lösungsweg im Rahmen einer einer Übungsgruppe erarbeitet, seid bitte so nett und ergänzt euer Issue um einen kurzen Kommentar, um eure KommilitonInnen zu unterstützen.
