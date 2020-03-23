    # Modul 300 | LB02

Vowort
-
Das Thema in diesem Modul ist *plattformübergreifende Dienste in ein Netzwerk integrieren*
  Wir lernen wie man Programme ausführt die nicht auf dem eigenen Rechnern installiert sind sonder auf einem anderen Rechner, der aus der Ferne (remote) aufgerufen wird.  

# Umgebungen
Die Umgebungen basieren auf Linux. Linux ist ein Open Source Betriebssystem der auf Unix basiert. Diese kann weltweit von Firmen und Privatpersonen entwickelt und verbessert werden. 

Github
-
Github bietet allen  Benutzer plattformübergreifende Dienste die nicht auf dem eigenen Rechner installiert werde müssen, sondern  aus der Ferne (remote) aufgerufen werden.

**K2: Eigene Lernumgebung (PLE) ist eingerichtet** 

-   GitHub oder Gitlab-Account ist erstellt
-   Git-Client wurde verwendet
-   Dokumentation ist als Mark Down vorhanden
-   Markdown-Editor ausgewählt und eingerichtet
-   Mark down ist strukturiert
-   Persönlicher Wissenstand im Bezug auf die wichtigsten Themen sind dokumentiert
-   Wichtige Lernschritte sind dokumentiert






Github Account
-
4. Repositories hochladen

Diesen Befehl exekutiert man, wenn man offline Änderungen gemacht hat und diese dann wieder hochladen möchte.

     $ git commit -m "Mein Kommentar"
     $ git push

5. SSH-Key erstellen

Man muss Git/Bash  ([https://git-scm.com/download/win](https://git-scm.com/download/win)) installieren um dann darauf Befehle auszuführen. 

Nun führt man folgenden Code aus um ein SSH Key zu erstellen. 

     $ ssh-keygen -t rsa -b 4096 -C "beispiel@beispiel.com"

Nun fragt man wohn man den Schlüssen speichern soll. Um den Standard zu wählen klickt man einfach auf Enter. 

     Enter a file in which to save the key (~/.ssh/id_rsa):

Nun fragt es nach einem Passwort, dieser kann man setzen, für dieses Projekt habe ich kein Passwort gesetzt. Für "kein Passwort" klickt man einfach auf Enter.

Um dann den SSH Key dem SSH Agent hinzuzufügen kopiert man die Datei %HOME%/.ssh/id_rsa.pub oder $HOME/.ssh/id_rsa.pub und besucht daraufhin die Website [www.github.com](http://www.github.com/)
Dort öffnet man Settings > SSH Keys und erstellt ein neuer SSH Key unter "New SSH key" und gibt die kopierte Datei von der Zwischenablage ein. Sobald der SSH Key erkannt wird ist dieser eingerichtet und erledigt.
![enter image description here](https://raw.githubusercontent.com/naiarabarzola1/Modul300/master/Unbenannt1.PNG)

Git-Client
-
Der Git-Client ist ein kommandozeilenbasierendes Tool, womit man GitHub Repositories bedienen kann. Es kann mit dem Linux Bash verglichen werden, da sie im Prinzip gleich arbeiten. Dies kann man auf der offiziellen Website herunterladen und installieren.  
https://git-scm.com/downloads

1. Client konfigurieren

     $ git config --global user.name "<username>"
     $ git config --global user.email "<e-mail>"
2. Repositories importieren

Mit diesem Befehl werden Online Repositories im gewünschten Ordner  heruntergeladen. 

     $ cd Wohin\auch\immer
	 $ git clone git@github.com:<Ihr Name>/my_M300.git
	 
3. Repository herunterladen	

Mit dem folgenden Befehl holt man alle Daten die auf dem Online Service sind herunter in dem lokalen Ordner

	$ git pull
	
Ich habe ein Test durchgeführt der auf der Cloud unter Test zu finden ist.

Bei der Ausführung dieses Kommandos wird der Repository mit dem Master auf Github verglichen. Falls der Master eine aktuellere Version als der lokale Repository hat wird auch dieser aktualisiert.


**Wir arbeiten von nun an grundsätzlich mit dem Git-Client**

Virtualisierung - Virtual Box
-
Dei Virtualisierung kommt zum Einsatz sobald man mit weniger Infrastruktur vieles erreichen möchte. Es ist eine effektive Methode um Hardware zu sparen. Man kann anhand einer Maschine viele Server oder Arbeitsplätze ersetzen. Auf der Maschine wird die Virtualisierungssoftware installiert (unterschieden zwischen Typ1/2). Anhand dieser Software kann man Server, Clients oder sogar Netze installieren. 

Die Virtualisierungssoftware die für dieses Projekt gebraucht wird ist Virtual Box. Die Installation von VIrtualbox wird mit Hilfe der offiziellen Website gemacht. Ein großer Vorteil der Benutzung von Virtual Box ist die Komptabilität mit Vagrant.

Um Virtual Box zu **installieren** besucht man den folgenden Link >[Download](https://www.virtualbox.org/). Die Installation ist GUI-basiert. Man geht nach Standard ein und ist bereit für das **Herunterladen der ISO-Datei**.  
 
Man benötigt ein Image File. In unserem Fall suchen wir *Ubuntu Desktop 16.04.05* Dieses kann man beispielsweise aus dem Internet herunterladen, [Download aus dem Internet](https://ubuntu.com/#download) 
Praktischer und schneller ist es, wenn ein Mitschüler diese schon heruntergeladen hat, dieser kann die ISO Datei auf einem USB-Stick kopieren und übergeben. In wenigen Minuten wird diese hinüberkopiert werden.

Für das**Erstellen der VMs** haben wir durch die Toolumgebung die richtigen Einstellungen gekannt. 
Die Erstellung und Einrichtung war somit einfach zu machen .

Vagrant
-
![See the source image](https://images.g2crowd.com/uploads/product/image/social_landscape/social_landscape_1489710078/vagrant.png)

Anhand von Vagrant kann man nun virtuelle Maschinen erstellen. Die Vagant Box und das Vagrantfile werden dafür gebraucht, Diese beinhalten wichtige Daten wie die virtuelle Festplatte der VM, Name, Ram Grösse, CPU, Anzahl Prozessoren etc. 

**Netzwerkplan**

![enter image description here](https://raw.githubusercontent.com/naiarabarzola1/Modul300/master/1netzwerkplan.PNG)


**K3: Vagrant**

-   Bestehende VM aus Vagrant-Cloud einrichten
-   Kennt die Vagrant-Befehle
-   Eingerichtete Umgebung ist dokumentiert (Umgebungsvariablen, Netzwerkplan gezeichnet)
-   vorgefertigte VM auf eigenem Notebook aufgesetzt
-   Projekt mit Git und Mark Down dokumentiert
- 
Die Befehle werden auch mit dem Git-Client gemacht. Dazu öffnet man erneut Git Bash.

1.   Neues Vagrantfile erstellen

Mit diesem Befehl wird ein Verzeichnis und das Vagrant File erstellt
 
      $ cd Wohin\auch\immer
      $ vagrant init ubuntu/xenial64

![enter image description here](https://raw.githubusercontent.com/naiarabarzola1/Modul300/master/vagrant%20init.PNG)

2. VMs erstellen

Wechsel zum Verzeichnis wo das Vagrantfile erstellt wurde

     $ cd Zum\Vagrantfile						#Wechseln zum ensprechenden Verzeichnis
     $ vagrant up --provider virtualbox			#Erstellen der VM

![https://drive.google.com/file/d/1m3DBeN-eNYBEVp2X0XyGFRG8XZIzRl19/view?usp=sharing](https://raw.githubusercontent.com/naiarabarzola1/Modul300/master/vagrant%20up.PNG)

3. VM Verbindung mit SSH
 
Nun hat man die Virtuelle Maschine erstellt und möchte sich verbinden.
      $ cd Zur\VM
      $ vagrant ssh
Diese wenige Schritte waren nötig um auf eine Vagrant Virtuelle Maschine zuzugreifen. 
Um eine VM herunterzufahren und auch zu löschen benutzt man die folgenden Befehle. Dies muss in dieser Reihenfolge geschehen damit die Löschung der Maschine stattfinden kann.

![https://drive.google.com/file/d/10jMuxi7ke3Mq5WQQ1gCTfhnZwlFhsEFy/view?usp=sharing](https://raw.githubusercontent.com/naiarabarzola1/Modul300/master/vagrant%20ssh.PNG)

       $ Vagrant halt
       $ Vagrant destroy

Das wäre schon alles was man wissen muss um ein Vagrant Maschine zu installieren und zu verwalten. 

Die Maschine ist nun auch in der Virtual Box sichtbar

![Meine Vagrant Maschine](https://raw.githubusercontent.com/naiarabarzola1/Modul300/master/Virtual%20Box.PNG)

 Visual Studio Code
- 
  ![Bildergebnis für visual studio code logo](https://germanpowershell.com/wp-content/uploads/2019/04/visualstudio_code-card.png)
Visual Studio Code ist eine Software auf welche man verschiedene Programmier und Scriptsprachen editieren kann. Es werden sehr viele Datei-Typen unterstützt, die durch Plug Ins erweitert werden können. Wir müssen folgende Plug Ins installieren

- Markdown All in One 
- Vagrant Extension
- vscode-pdf Extension 

# Sicherheit
**K4: Sicherheitsaspekte sind implementiert**

-   Firewall eingerichtet inkl. Rules
-   Reverse-Proxy eingerichtet
-   Benutzer- und Rechtevergabe ist eingerichtet
-   Zugang mit SSH-Tunnel abgesichert
-   Sicherheitsmaßnahmen sind dokumentiert
-   Projekt mit Git und Mark Down dokumentiert
 
SSH Key 
- 
Da mit Github eine Verbindung mit dem Online Repository erstellt werden muss um Exporte/Importe von Daten zu machen braucht es eine sichere Verbindung. Da kommt SSH zum Einsatz, durch SSH werden die Verbindungen verschlüsselt, damit nicht mitgelesen werden kann. 

Firewallrules
-
Bei der Firewall müssen zwei wichtige Ports geöffnet werden. 

- Port 22
- Port 80

Port 22 wird geöffnet damit man eine SSH Verbindung zum Server machen kann. Port 80 wird geöffnet damit man schlussendlich auch auf den Webserver zugreifen kann.



# Schlusswort & Fazit
Das Modul 300 ist im Prinzip ein spannendes Modul. Ich habe spät gemerkt um was es sich eigentlich handelt in diesem Modul. Die ganze Situation mit dem Virus und mit dem "Home Schooling" macht es nicht einfacher. Trotzdem bin ich mit meiner Dokumentation zufrieden, und wünsche mir das dies auch für Dritte hilfreich sein kann.

    
