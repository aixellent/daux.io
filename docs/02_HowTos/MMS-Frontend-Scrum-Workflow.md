# MMS Frontend Scrum Workflow

## Grundidee und Probleme
Bisher sind die abstrakten Arbeitsaufgaben des UI/UX Projekts in Epen sowie in darin beinhaltete Aufgaben unterteilt. Diese Einteilung ist zwar grundsätzlich in Ordnung, jedoch ist diese recht lose definiert.  Problematisch daran ist, dass man nur schwer konkret sagen kann wo man sich gerade befindet und wie der konkrete Ausblick ist. Aus diesem Grund ist eine feinere Einteilung der Aufgaben in Unteraufgaben notwendig um so konkrete Meilensteine und einen konkreteren Projektstatus definieren zu können. 

## Lösungsidee
Der JIRA-Workflow für die Ticketbearbeitung ist bereits von Scrum entlehnt und auf dieser Grundidee soll auch unser Verfahren basieren. Die Epen werden bei uns zu Meilensteinen, diese bilden auch alle Elemente die im [Atomic Design Pattern](http://patternlab.io/) definiert sind ab (Atome, Moleküle....etc). 
Da der Workflow des Atomic Design Patterns bereits in Etappen definiert ist (Atoms → Molecules → Organisms → Templates → Pages) kann dieser grundsätzlich für die Definition der Epen adaptiert werden.

![Atomic Design Steps](https://c4.staticflickr.com/8/7659/17177400400_8168a2e788_b.jpg)

**Definition Epos / Pakete von Unteraufgaben**
Hierbei sollte ein Epos in einem kurzen Satz beschrieben werden können, für die Atome bspw. "Wir wollen alle Atome / Einzelkomponenten die wir für die Umsetzung des neue UI benötigen umgesetzt erstellen" usw. 
Diese Beschreibung ist natürlich sehr abstrakt, um nun einen konkreten Fortschritt tracken zu können muss der Epos in logische Pakete zerteilt werden (in Scrum nennt man dies dann "UserStory"). Diese logischen Pakete sollten dann in einem gewissen Zeitrahmen (ein Sprint bei Scrum) abgearbeitet werden. Wie lange dieser Zeitraum ist kann von uns definiert werden und lehnt sich dabei am Aufwand der umzusetzenden Aufgaben an (bei Scrum ~1-2 Wochen pro Sprint aber maximal 4 Wochen). Am Ende eines Sprints sollte nun ein messbares Ergebnis stehen und sagt in der Theorie auch aus ob ein Sprint erfolgreich war oder nicht. Aufgaben die wider erwarten nicht geschafft worden sind, werden dann in einem der folgenden Sprints mitgenommen und im Rahmen dessen bearbeitet.
Dieser Zyklus setzt sich nun so lange fort bis alle Unteraufgaben eines Epos abgearbeitet sind und der Epos damit erfüllt ist.

Der Workflow sieht wie folgt aus:

![Scrum process](http://upload.wikimedia.org/wikipedia/commons/thumb/5/58/Scrum_process.svg/2000px-Scrum_process.svg.png)

## Der konkrete Workflow 

1. Sprintplanung Um nun abschätzen zu können was wir in einem Sprint schaffen, müssen wir vor jedem Sprint besprechen _"Wer schafft was in welchem Zeitraum"_. Nach dieser Besprechung werden dann die Pakete, sowie der Zeitrahmen geplant in dem diese fertig sein sollten.

2. Arbeitsablauf Sind die Pakete dann geschnürt, beginnt die Arbeit. Jeder arbeitet dann konkret nur an den Tickets / Aufgaben die ihm im Rahmen des aktuellen Sprints zugeordnet wurden und an sonst nichts anderem.

3. Tägliches Statusmeeting Es wird ein kurzes tägliches Statusmeeting zu Beginn des Tages geben (10-15 Minuten mehr nicht) in dem der jeweilige Entwickler einen kurzen Status zu 3 Kernfragen gibt:

  … mit Blick auf das Ziel des aktuellen Sprints …
  1. … habe ich erreicht …
  1. … will ich als Nächstes auch erreichen …
  1. … behindert mich … 

4. Abschluß eines Sprints Ist nun die abgeschätzte Zeit eines Sprints vorbei, ist auch der Sprint beendet. Es wird dann in einem Meeting folgendes analysiert:
  1. Wurden alle abgeschätzten Aufgaben geschafft (zu viel oder zu wenig workload)?
  1. Woran hat dies gelegen (keine Kritikrunde, reine Fehleranalyse)?

Dahingehend kann man am Verhältnis von geschätztem zu geschafften Workload den Arbeitsfortschritt erkennen. Ferner kann man anhand der Ergebnisse Lehren für folgende Sprints ziehen, um Arbeitsumfänge und somit die zukünftigen Entwicklungszyklen noch genauer abschätzen zu können.

