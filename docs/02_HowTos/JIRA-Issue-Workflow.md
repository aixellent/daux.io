# JIRA Issue Workflow

## Basisworkflow

Der in JIRA konfigurierte Lebenszyklus / Workflow eines Tickets sieht wie folgt aus:

![JIRA Workflow](https://c4.staticflickr.com/8/7688/16894577373_bdf5cf9bc9_b.jpg)


Dieser kann mit detaillierteren Erklärungen in jedem Issue neben dem Status geöffnet werden:

![](https://c4.staticflickr.com/8/7686/17340134706_1d4efb27a0_b.jpg) 

## Die Ticketstatus

**OPEN**

Wird ein Ticket erstellt hat dieses initial den Status OPEN. Tickets in diesem Status können frei bearbeitet werden.


[>> Filter aller offenen Tickets](https://mehrkanal.atlassian.net/issues/?jql=project%20%3D%20UIUX%20AND%20issuetype%20in%20(Aufgabe%2C%20Unteraufgabe)%20AND%20assignee%20in%20(uiux-a-walter%2C%20v-kress%2C%20currentUser()%2C%20uiux-t-favetto%2C%20h-thesing%2C%20EMPTY)%20AND%20status%20%3D%20Open%20ORDER%20BY%20status%20DESC%2C%20summary%20ASC%2C%20assignee%20ASC)

***

**IMPLEMENTATION / UMSETZUNG**

Wenn ein Entwickler beginnt an einem Ticket zu arbeiten, setzt er den Status des Tickets mit dem Klick auf den Button "Implementation" auf IMPLEMENTATION bzw. UMSETZUNG. Dieser Status zeigt an das schon jemand an der Aufgabe arbeitet, was ggf. doppelte Arbeit verhindert.

***

**TO CONFIRM / BESTÄTIGUNG**

Hat der Entwickler eine Aufgabe fertig bearbeitet, setzt er den Status des Tickets mit dem Klick auf den Button "Implementation done" auf TO CONFIRM. Damit zeigt er dem Area Experten (hier Volker) an das dieser nun das Ergebnis reviewen kann.

***

**CLOSED**

Bearbeitete Issues müssen dann noch durch einen Area Experte gereviewed werden. Wurde alles zur vollen Zufriedenheit umgesetzt, wird das Issue mit dem Klick auf den button "Issue resolved" geschlossen.

[>> Filter der zu reviewenden Tickets](https://mehrkanal.atlassian.net/issues/?filter=14516)

***

## Exceptional Cases / Ausnahmefälle

**FEEDBACK REQUIRED**

Hat der Entwickler fragen und kann diese nicht direkt klären stellt er das Ticket in den Status "FEEDBACK REQUIRED" mit dem Klick auf den gleichnamigen Button und schreibt das zu klärende Problem kurz und bündig als Kommentar des Tickets nieder. Der Entwickler behält das Ticket aber bei sich, dieser Status ist lediglich eine Indikator für den Area Experten das Unklarheiten bestehen so dass er sich darum kümmern kann. 

Sind die Unklarheiten dann beseitigt, stellt entweder der Entwickler oder aber der Area Experte das Ticket mit dem Klick auf den Button "Start working" zurück in den Status "IN PROGRESS"

***

**REOPENED**

Hat der Area Experte das Arbeitsergebnis gereviewed und ist dieses nicht ausreichend, öffnet er das Ticket erneut mit einem klick auf den Button "Feedback given" und assigned es dem Entwickler der es bearbeiten soll. Der Status REOPENED ist von der Bedeutung adäquat mit dem Status OPEN.