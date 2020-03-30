---


---

<h1 id="modul-300--lb02">Modul 300 | LB02</h1>
<h2 id="vowort">Vowort</h2>
<p>Das Thema in diesem Modul ist <em>plattformübergreifende Dienste in ein Netzwerk integrieren</em><br>
Wir lernen wie man Programme ausführt die nicht auf dem eigenen Rechnern installiert sind sonder auf einem anderen Rechner, der aus der Ferne (remote) aufgerufen wird.</p>
<h1 id="umgebungen">Umgebungen</h1>
<p>Die Umgebungen basieren auf Linux. Linux ist ein Open Source Betriebssystem der auf Unix basiert. Diese kann weltweit von Firmen und Privatpersonen entwickelt und verbessert werden.</p>
<h2 id="github">Github</h2>
<p>Github bietet allen  Benutzer plattformübergreifende Dienste die nicht auf dem eigenen Rechner installiert werde müssen, sondern  aus der Ferne (remote) aufgerufen werden.</p>
<p><strong>K2: Eigene Lernumgebung (PLE) ist eingerichtet</strong></p>
<ul>
<li>GitHub oder Gitlab-Account ist erstellt</li>
<li>Git-Client wurde verwendet</li>
<li>Dokumentation ist als Mark Down vorhanden</li>
<li>Markdown-Editor ausgewählt und eingerichtet</li>
<li>Mark down ist strukturiert</li>
<li>Persönlicher Wissenstand im Bezug auf die wichtigsten Themen sind dokumentiert</li>
<li>Wichtige Lernschritte sind dokumentiert</li>
</ul>
<h2 id="github-account">Github Account</h2>
<ol start="4">
<li>Repositories hochladen</li>
</ol>
<p>Diesen Befehl exekutiert man, wenn man offline Änderungen gemacht hat und diese dann wieder hochladen möchte.</p>
<pre><code> $ git commit -m "Mein Kommentar"
 $ git push
</code></pre>
<ol start="5">
<li>SSH-Key erstellen</li>
</ol>
<p>Man muss Git/Bash  (<a href="https://git-scm.com/download/win">https://git-scm.com/download/win</a>) installieren um dann darauf Befehle auszuführen.</p>
<p>Nun führt man folgenden Code aus um ein SSH Key zu erstellen.</p>
<pre><code> $ ssh-keygen -t rsa -b 4096 -C "beispiel@beispiel.com"
</code></pre>
<p>Nun fragt man wohn man den Schlüssen speichern soll. Um den Standard zu wählen klickt man einfach auf Enter.</p>
<pre><code> Enter a file in which to save the key (~/.ssh/id_rsa):
</code></pre>
<p>Nun fragt es nach einem Passwort, dieser kann man setzen, für dieses Projekt habe ich kein Passwort gesetzt. Für “kein Passwort” klickt man einfach auf Enter.</p>
<p>Um dann den SSH Key dem SSH Agent hinzuzufügen kopiert man die Datei %HOME%/.ssh/id_rsa.pub oder $HOME/.ssh/id_rsa.pub und besucht daraufhin die Website <a href="http://www.github.com/">www.github.com</a><br>
Dort öffnet man Settings &gt; SSH Keys und erstellt ein neuer SSH Key unter “New SSH key” und gibt die kopierte Datei von der Zwischenablage ein. Sobald der SSH Key erkannt wird ist dieser eingerichtet und erledigt.<br>
<img src="https://raw.githubusercontent.com/naiarabarzola1/Modul300/master/Unbenannt1.PNG" alt="enter image description here"></p>
<h2 id="git-client">Git-Client</h2>
<p>Der Git-Client ist ein kommandozeilenbasierendes Tool, womit man GitHub Repositories bedienen kann. Es kann mit dem Linux Bash verglichen werden, da sie im Prinzip gleich arbeiten. Dies kann man auf der offiziellen Website herunterladen und installieren.<br>
<a href="https://git-scm.com/downloads">https://git-scm.com/downloads</a></p>
<ol>
<li>
<p>Client konfigurieren</p>
<p>$ git config --global <a href="http://user.name">user.name</a> “&lt; username &gt;”<br>
$ git config --global user.email “&lt; e-mail &gt;”</p>
</li>
<li>
<p>Repositories importieren</p>
</li>
</ol>
<p>Mit diesem Befehl werden Online Repositories im gewünschten Ordner  heruntergeladen.</p>
<pre><code> $ cd Wohin\auch\immer
 $ git clone git@github.com:&lt;Ihr Name&gt;/my_M300.git
</code></pre>
<ol start="3">
<li>Repository herunterladen</li>
</ol>
<p>Mit dem folgenden Befehl holt man alle Daten die auf dem Online Service sind herunter in dem lokalen Ordner</p>
<pre><code>$ git pull
</code></pre>
<p>Ich habe ein Test durchgeführt der auf der Cloud unter Test zu finden ist.</p>
<p>Bei der Ausführung dieses Kommandos wird der Repository mit dem Master auf Github verglichen. Falls der Master eine aktuellere Version als der lokale Repository hat wird auch dieser aktualisiert.</p>
<p><strong>Wir arbeiten von nun an grundsätzlich mit dem Git-Client</strong></p>
<h2 id="virtualisierung---virtual-box">Virtualisierung - Virtual Box</h2>
<p>Dei Virtualisierung kommt zum Einsatz sobald man mit weniger Infrastruktur vieles erreichen möchte. Es ist eine effektive Methode um Hardware zu sparen. Man kann anhand einer Maschine viele Server oder Arbeitsplätze ersetzen. Auf der Maschine wird die Virtualisierungssoftware installiert (unterschieden zwischen Typ1/2). Anhand dieser Software kann man Server, Clients oder sogar Netze installieren.</p>
<p>Die Virtualisierungssoftware die für dieses Projekt gebraucht wird ist Virtual Box. Die Installation von VIrtualbox wird mit Hilfe der offiziellen Website gemacht. Ein großer Vorteil der Benutzung von Virtual Box ist die Komptabilität mit Vagrant.</p>
<p>Um Virtual Box zu <strong>installieren</strong> besucht man den folgenden Link &gt;<a href="https://www.virtualbox.org/">Download</a>. Die Installation ist GUI-basiert. Man geht nach Standard ein und ist bereit für das <strong>Herunterladen der ISO-Datei</strong>.</p>
<p>Man benötigt ein Image File. In unserem Fall suchen wir <em>Ubuntu Desktop 16.04.05</em> Dieses kann man beispielsweise aus dem Internet herunterladen, <a href="https://ubuntu.com/#download">Download aus dem Internet</a><br>
Praktischer und schneller ist es, wenn ein Mitschüler diese schon heruntergeladen hat, dieser kann die ISO Datei auf einem USB-Stick kopieren und übergeben. In wenigen Minuten wird diese hinüberkopiert werden.</p>
<p>Für das<strong>Erstellen der VMs</strong> haben wir durch die Toolumgebung die richtigen Einstellungen gekannt.<br>
Die Erstellung und Einrichtung war somit einfach zu machen .</p>
<h2 id="vagrant">Vagrant</h2>
<p><img src="https://images.g2crowd.com/uploads/product/image/social_landscape/social_landscape_1489710078/vagrant.png" alt="See the source image"></p>
<p>Anhand von Vagrant kann man nun virtuelle Maschinen erstellen. Die Vagant Box und das Vagrantfile werden dafür gebraucht, Diese beinhalten wichtige Daten wie die virtuelle Festplatte der VM, Name, Ram Grösse, CPU, Anzahl Prozessoren etc.</p>
<p><strong>Netzwerkplan</strong></p>
<p><img src="https://raw.githubusercontent.com/naiarabarzola1/Modul300/master/1netzwerkplan.PNG" alt="enter image description here"></p>
<p><strong>K3: Vagrant</strong></p>
<ul>
<li>Bestehende VM aus Vagrant-Cloud einrichten</li>
<li>Kennt die Vagrant-Befehle</li>
<li>Eingerichtete Umgebung ist dokumentiert (Umgebungsvariablen, Netzwerkplan gezeichnet)</li>
<li>vorgefertigte VM auf eigenem Notebook aufgesetzt</li>
<li>Projekt mit Git und Mark Down dokumentiert</li>
<li></li>
</ul>
<p>Die Befehle werden auch mit dem Git-Client gemacht. Dazu öffnet man erneut Git Bash.</p>
<ol>
<li>Neues Vagrantfile erstellen</li>
</ol>
<p>Mit diesem Befehl wird ein Verzeichnis und das Vagrant File erstellt</p>
<pre><code>  $ cd gewünschter/Pfad
  $ vagrant init ubuntu/xenial64
</code></pre>
<p><img src="https://raw.githubusercontent.com/naiarabarzola1/Modul300/master/vagrant%20init.PNG" alt="enter image description here"></p>
<ol start="2">
<li>VMs erstellen</li>
</ol>
<p>Wechsel zum Verzeichnis wo das Vagrantfile erstellt wurde</p>
<pre><code> $ cd Zum\Vagrantfile						#Wechseln zum ensprechenden Verzeichnis
 $ vagrant up --provider virtualbox			#Erstellen der VM
</code></pre>
<p><img src="https://raw.githubusercontent.com/naiarabarzola1/Modul300/master/vagrant%20up.PNG" alt="https://drive.google.com/file/d/1m3DBeN-eNYBEVp2X0XyGFRG8XZIzRl19/view?usp=sharing"></p>
<ol start="3">
<li>VM Verbindung mit SSH</li>
</ol>
<p>Nun hat man die Virtuelle Maschine erstellt und möchte sich verbinden.<br>
$ cd Zur\VM<br>
$ vagrant ssh<br>
Diese wenige Schritte waren nötig um auf eine Vagrant Virtuelle Maschine zuzugreifen.<br>
Um eine VM herunterzufahren und auch zu löschen benutzt man die folgenden Befehle. Dies muss in dieser Reihenfolge geschehen damit die Löschung der Maschine stattfinden kann.</p>
<p><img src="https://raw.githubusercontent.com/naiarabarzola1/Modul300/master/vagrant%20ssh.PNG" alt="https://drive.google.com/file/d/10jMuxi7ke3Mq5WQQ1gCTfhnZwlFhsEFy/view?usp=sharing"></p>
<pre><code>   $ Vagrant halt
   $ Vagrant destroy
</code></pre>
<p>Das wäre schon alles was man wissen muss um ein Vagrant Maschine zu installieren und zu verwalten.</p>
<p>Die Maschine ist nun auch in der Virtual Box sichtbar</p>
<p><img src="https://raw.githubusercontent.com/naiarabarzola1/Modul300/master/Virtual%20Box.PNG" alt="Meine Vagrant Maschine"></p>
<h2 id="visual-studio-code">Visual Studio Code</h2>
<p><img src="https://germanpowershell.com/wp-content/uploads/2019/04/visualstudio_code-card.png" alt="Bildergebnis für visual studio code logo"><br>
Visual Studio Code ist eine Software auf welche man verschiedene Programmier und Scriptsprachen editieren kann. Es werden sehr viele Datei-Typen unterstützt, die durch Plug Ins erweitert werden können. Wir müssen folgende Plug Ins installieren</p>
<ul>
<li>Markdown All in One</li>
<li>Vagrant Extension</li>
<li>vscode-pdf Extension</li>
</ul>
<h1 id="sicherheit">Sicherheit</h1>
<p><strong>K4: Sicherheitsaspekte sind implementiert</strong></p>
<ul>
<li>Firewall eingerichtet inkl. Rules</li>
<li>Reverse-Proxy eingerichtet</li>
<li>Benutzer- und Rechtevergabe ist eingerichtet</li>
<li>Zugang mit SSH-Tunnel abgesichert</li>
<li>Sicherheitsmaßnahmen sind dokumentiert</li>
<li>Projekt mit Git und Mark Down dokumentiert</li>
</ul>
<h2 id="ssh-key">SSH Key</h2>
<p>Da mit Github eine Verbindung mit dem Online Repository erstellt werden muss um Exporte/Importe von Daten zu machen braucht es eine sichere Verbindung. Da kommt SSH zum Einsatz, durch SSH werden die Verbindungen verschlüsselt, damit nicht mitgelesen werden kann.</p>
<h2 id="firewallrules">Firewallrules</h2>
<p>Bei der Firewall müssen zwei wichtige Ports geöffnet werden.</p>
<ul>
<li>Port 22</li>
<li>Port 80</li>
</ul>
<p>Port 22 wird geöffnet damit man eine SSH Verbindung zum Server machen kann. Port 80 wird geöffnet damit man schlussendlich auch auf den Webserver zugreifen kann.</p>
<h2 id="dokumentation-der-testfälle">Dokumentation der Testfälle</h2>

<table>
<thead>
<tr>
<th>ID</th>
<th>Beschreibung</th>
<th>Erwartetes Ergebnis</th>
<th>Tatsächliches Ergebnis</th>
<th>Bewertung</th>
<th>Kommentar</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Firewall eingerichtet + Rules</td>
<td>Port 80/22 sind aktiv</td>
<td><img src="https://raw.githubusercontent.com/naiarabarzola1/Modul300/master/firewall.PNG" alt="enter image description here"></td>
<td>Dies wurde wie gewünscht durchgesetzt.</td>
<td>Ich habe zu Beginn die falsche IP Adresse angegeben und konnte nicht mehr auf den Server zugreifen</td>
</tr>
<tr>
<td>2</td>
<td>Reverse Proxy eingerichtet</td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>3</td>
<td>Vagrant Cloud eingerichtet</td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>4</td>
<td>Vagrant VM installiert und online</td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>5</td>
<td>Vagrant VM</td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table><h1 id="schlusswort--fazit">Schlusswort &amp; Fazit</h1>
<p>Das Modul 300 ist im Prinzip ein spannendes Modul. Ich habe spät gemerkt um was es sich eigentlich handelt in diesem Modul. Die ganze Situation mit dem Virus und mit dem “Home Schooling” macht es nicht einfacher. Trotzdem bin ich mit meiner Dokumentation zufrieden, und wünsche mir das dies auch für Dritte hilfreich sein kann.</p>

