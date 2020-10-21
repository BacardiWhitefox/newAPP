# newAPP
Some APP
Checkliste LAP 
Anforderungen 

1.	Technische Anforderungen, bevor Programmieren 
•	Festplatte mit SATA-Kabel verbinden 
•	Monitor, Netzwerkkabel, Stromkabel & Tastatur mit PC verbinden 

2.	Virtuelle Maschine (VirtualBox) einrichten 
•	Image (CentOS) vorhanden und importieren 
•	SSH Verbindung herstellen 
•	Evtl. Desktop Environment installieren für einfachere Handhabung 

Motor Verein Forum ist ein webbasiertest File-exchangeForum.  
ReadMe: eine neue Website erstelle. Motor-Club Verein
	Es gibt 3 Rollen: Admin, Administrator, User
	Es gibt Admin Panel
	Es gib User Portal (User/Administrator) geben
	Es gibt 3 Sektionen/Themen: Autos, Motorräder, Oldtimer
	Es gibt User Login Seite
	Es gibt Admin Login Seite
	Es gibt Admin Panel:
-	Header (mit User Name)
-	Es gibt Seite „Sektionen“
-	Es gibt Seite „Users“
-	Es gibt Seite „Posts“
	Es gib User Portal
-	Header (mit Username, Logout Button)
-	Es gibt Seite „Sektion“ hier werden alle Posts zu diesem Thema angezeigt
	In Sektionen user kann neue Posts erstellen
	User kann ein File in Post hinzufügen

	Admin kann:
-	login/logout
-	neue User anlegen
-	Alle User sehen/verwalten
-	Alle Sektionen sehen/verwalten
-	Alle Posts sehen/verwalten

	Administrator hat/kann: 
	alle Sektionen zugeordnet/sehen
-	register/login/logout
-	alle Beiträge/Files alle Sektionen sehen
-	neue Posts/Files in alle Sektionen erstellen
-	eigene Beiträge/Files bearbeiten/löschen

	User hat/kann: 
	nur zu eine Sektion zugeordnet/sehen
-	register/login/logout
-	alle Beiträge/Files seine Sektion sehen
-	neue Beiträge/Files in seine Sektion erstellen
-	eigene Beiträge/Files bearbeiten/löschen
 
3.	Datenbank erstellen 
•	Aufzeichnen Datenbankmodell (ER-Diagramm) 
TOOL: https://dbdiagram.io/d/5cf6c2f41f6a891a6a6594c8 
HILFE: https://erdplus.com/#/edit-diagram/941470 
•	Normalformen einhalten 
•	Datenbank erstellen  
Tables: 
1.	Users
a.	ID (PK, AI, not Null)
b.	fname (varchar 80, nicht Null)
c.	lname (varchar 80, Null)
d.	email (varchar 124, nicht Null)
e.	password (varchar, nicht Null)
f.	address_id (int, 11, Null)
g.	role_id (int, 11, not Null)
h.	section_id (int, 11, NULL)

2.	Roles
a.	ID (PK, AI, not Null)
b.	title (varchar 80, nicht Null)

3.	Sections
a.	ID (PK, AI, not Null)
b.	title (varchar 80, nicht Null)

4.	Files
a.	ID (PK, AI, not Null)
b.	title (varchar, 255, not Null)
c.	description (memo)
d.	user_id (int, 11, not null)
5.	Address
a.	ID (PK, AI, not Null)
b.	street (varchar, 255, not null)
c.	city (varchar 80, nicht Null)
d.	plz (int 11, not Null)
	


4.	Struktur erstellen
•	Ordner Struktur (MVC achitectural pattern)
Beispiel: https://www.codeproject.com/Articles/1080626/Code-Your-Own-PHP-MVC-Framework-in-Hour    
•	Files (index.php, Forms, Start Seite…)

5.	In PHP die Datenbankverbindung mit Linux Server erstellen 
•	Objektorientiert (Class DB)
•	mySQLi 
 
6.	PHP Login Skript erstellen 
•	Loginseite für User (Class User)
•	Loginseite für Admin (Class Admin)
•	Passwort muss gehasht sein 
•	MySQLi prepare Statements verwenden
 
 
7.	PHP User/Administrator Portal erstellen  
•	User Login/Logout 
•	Header/Navigationsleiste mit Namen von User (use Session)
•	Sektion/-s
	Sektion name (in Header)
	Posts Liste
	CRUD eigene Posts 
Example image upload : https://www.codexworld.com/upload-store-image-file-in-database-using-php-mysql/ 
 
8.	PHP Admin Panel erstellen 
•	Login/Logout
•	Header/Navigationsleiste mit Namen von User
•	User-Liste (alle User)
•	Sektionen-Liste (alle Sektionen)
•	CRUD Sektionen
•	CRUD Users
	Wenn neuer User angelegt/geändert wird, Check der PLZ mittels JS, sodass das Formular nicht neu geladen wird 

Prüfung Dauer 
Start 8:00 
Vorwort - 5-10 min
Computer einrichten - 10-15 min
Installieren einrichten Code Editor -10-15 min
Image auf VM einspielen
Netzwerkbrücke Einstellungen prüfen
SSH konnection erstellen (WinSCP)
Debug script starten (Putty)
{    tail -f /var/log/httpd/error_log   }
	Umsetzung Plan  (+zeit)
	Graphische ER Diagram von DB
	Verbindung zu ihre VM im Windows erstellen
	Eine „Hello World“ Datei erstellen und in Win Browser aufrufen (code anzeigen)
	Eine PHP Server Einstellungen Info anzeigen ( phpinfo(); )
PHP Info Site
V1.: in index.php (after db connect) 
phpinfo();
V2.
nano /var/www/html/info.php
<?php
phpinfo();
?>
Doku erstellen
Abgabe um 10:00 
Teil 1 Umsetzung:
Es existier eine Web Seite einen Verein „Klub“
Es existiert 3 Interessenbereiche:
	Moto
	Auto
	LKW  
Administrator kann User Konten erstellen. Mit die der User kann sich dann in der Webseite anzumelden.
Beim User anlegen, soll eine Anlegung-Überprüfung erstellt (nur Ziffern, nicht lehr) mit Warnung Info. Aber trotzdem speichern fordern. 
User und Admin habe separate Login Seiten.

 
Erstelle eine Datenbank (phpmyadmin (nicht vergessen user und db enstellungen ändern)
Ordner Struktur anlegen
Erstellen eine „mysqli“ Verbindung zu Datenbank (Object oriented)
Erstellen eine Login Funktion (Classe erstellen und verwenden)
Es soll 2 separate login pages für User und Admin geben
Check Browser.
Login als Start Seite
Admin Bereich erstellen
	Wo Admin neue User anlegen und bearbeiten kann
	Und Download Berreich
User kann nur einen Interesantesbereich zugewiesen werden
Und Users könne alle Dateien den Bereich ansehen und herunterladen können
Logout für User und Admin
Mittagspause 12:00 bis 12:45
Teil 1 Abgabe - 13:45
Fachgespräch (20 min)
Teil 2 Umsetzung:
Benutzer Bereich
Logout
Darstellung sollte in IE11 & Firefox ident sein
Überschriften und Tabellen
Seite mit Dokus mit Titels und so 
Kennwort ändern

Admin Bereich 
Logout
All Users
All Leiter
Download Bereich
Interessentenbereiche neue anlegen
Eine Funktion für Administrator, mit den click auf User ins seinen Ansicht zu wechseln

Benutzer Hand Buch erstellen
Kurze Anleitung für End User über die Funktionen von Plattform 
Teil 2 Abgabe – 16:00
Abbau 16:00




 


10
Bevor Umsetzung:
Arbeits plan mit zeut shetzungen (gesammt Zeit)
