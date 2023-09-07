# Lernziele Schriftlicher Teil

## 1. Verzeichnisdienst: Grundlagen
### Funktionsweise und Einsatz eines AD-Dienstes
Ein Verzeichnisdienst ist ein System, das Ressourcen (Geräte, Gruppen und Benutzer) speichert und übersichtlich bereitstellt. Ein AD erleichtert die Verwaltung von Ressourcen in einer Domäne. Ein AD-Server muss auf einem DC aufgesetzt werden.
### Kennen die folgenden Eigenschaften eines Verzeichnisdienstes:
* Skalierbarkeit: Die Fähigkeit mit dem Wachstum der Ressourcen umzugehen
* Erweiterbarkeit: Die Möglichkeit neue Attribute und Objektklassen hinzuzufügen
* Sicherheit: Die Gewährleistung der Sicherheit des Zugriffs auf die Ressourcen
* Verfügbarkeit: Die beständige Verfügbarkeit des Dienstes
* Performance: Die Leistung, die der Dienst erweist, um Informationen Effizient Abzurufen
### Welche Standards werden im MS AD verwendet und was sind Ihre Aufgaben?
* X.500: Definiert die Struktur Namensgebung im Verzeichnisdienst
* DNS: Dient zur Auflösung des Domänenname in IP-Adressen
* LDAP: Protokoll zur Kommunikation und Abfrage des Verzeichnisdienstes

## 2. X.500 Standard
### Welche Eigenschaften beinhaltet dieser Standard? Die Lernenden verstehen die Zusammenhänge der Namensbildung (DN, RDN), den Schemaaufbau mit den Objektklassen und die Eigenschaften der Attribute  
* Namensbildung(DN und RDN): Distinguished und Relative Distinguished Name für die Identifikation der Objekte im Dienst 
* Schemenaufbau mit Objektklassen: Definition mit Objektklassen und deren Attribute
* Eigenschafften der Attribute: Beschreibung der der Eigenschaften von Objekten
### Sie sind in der Lage anhand von Screenshots im AD-Schema-Editor oder Attribut-Editor Begriffe (Objektbezeichnung, Objektklasse, Attributbezeichnung und Attributwert) zu erklären.
Übung
### Welche Eigenschaften definieren Klassen und Attribute. Erklären Sie die Unterschiede. 
Klassen definieren Objekttypen, während Attribute Eigenschaften von Objekten Beschreiben.
### Was ist eine OID? Wo wird sie überall verwendet? 
Objekt Identifier ist eine Eindeutige Nummer zur Identifikation von Objekten und Attributen im X.500 Standard. Sie werden in verschiedenen IT-Bereichen verwendet, einschliesslich Sec. Zertifikaten und SNMP-MIBs.
### Was sind Replikationsmodelle im X.500 Standard
* Singlemaster: Ein Server der für eine Bestimmte änderungen verantwortlich
* Multi-Master: Mehrer Server können Änderungen vornehmer

## 3. Domain Name System (DNS)
### Hierarchischer Aufbau und Eigenschaften
Das Domain Name System (DNS) hat einen hierarchischen Aufbau, der aus mehreren Ebenen besteht. An oberster Stelle steht die Root-Domain, die von einer begrenzten Anzahl von Root-Servern verwaltet wird. Darunter befinden sich Top-Level-Domains (TLDs), wie .com, .org und Länderkennungen wie .de. Diese TLDs sind wiederum in Subdomains unterteilt, die von verschiedenen Organisationen oder Unternehmen verwaltet werden. Schließlich stehen unter den Subdomains die eigentlichen Domain-Namen, die IP-Adressen und andere DNS-Einträge verweisen. Dieser hierarchische Aufbau ermöglicht die effiziente Auflösung von Domain-Namen in IP-Adressen im gesamten Internet.
###Zonentypen im DNS
* Primärzone: Die Ursprüngliche Quelle für DNS-Daten
* Sekundärzone: Eine Kopie der Primärzone zu Redundanz-Zwecken
* Subzone: Enthält verweise auf DNS-Server anderer Domänen
* AD-Integrierte Zone: Speichert DNS-Zonendaten im AD

## 4. Domäne und Standort

### 4.1	Domänenmodell. Sie kennen die grafische Darstellung von Domänen und erklären die Eigenschaften (Sicherheitsgrenzen, Schutzschema, DC Empfehlungen, Replikation DC, RODC). 
* #### Logische Sicht
* Mit Dreiecken dargestellt
* Grundsätzlich nur eine Domäne
* Zwei DCs Pro Domäne einzeichnen
* Weiter Domänen nur bei:
  * Schemaschutz
  * Autonome, eigenständige Verwaltung
  * Bei ‘Eigenen’ Sicherheitsbereich
* #### Physische Sicht
  * Durch Ovale Kreise dargestellt
  * Bei üblicher WAN-Verbindung -> 1 DC pro Standort.
  * Bei Hochgeschw. 1 DC für alle Standorte.
### Eigenschaften von Domänen
* Sicherheitsgrenzen -> Domänengrenzen
* Der Admin einer übergeordneten Domäne hat nicht automatisch alle Rechte-
* Die Objekte werden durch ein einheitliches Namenskonzept schnell gefunden.
* Schutzschema
* DC-Empfehlungen
* Zwei DCs für Redundanz -> Ausfall Sicherheit
* Replikation DC
* Vermeidung eines SPOF
* DCs kopieren sich gegenseitig.
* Jeder DC enthält alle Objekte der Domäne
* RODC -> Read Only DC
  * Nicht alle Objekte werden repliziert.

### 4.2	Welche Strukturierungsmöglichkeiten bietet die Organisational Unit (OU). Nennen Sie Praxisbeispiele zu den Themen «Abbilden der Firmenstruktur», «Verwaltungstätigkeiten», «Gruppenrichtlinien» und «Sichtbarkeit».
* #### Eigenschaften OUs:
  * OUs bieten Unterteilung der Domäne in eigene Unternehmen/Abteilungen an
  * OUs könne verschiedene Objekte beinhalten.
* #### Strukturierungsmöglichkeiten mit OUs 
  * Abbilde den Firmenstruktur durch OUs.
  * Zuweisung von Verwaltungstätigkeiten durch einen Admin.
  * Gruppenrichtlinien anwenden 
  * Sichtbarkeit: nur User mit Leseberechtigung sehen für OUs sehen den OU-Inhalt.

### 4.3	Sie kennen die Unterschiede zwischen Einzeldomäne, Domänenstruktur (Tree), Gesamtstruktur (Forest) und Mehrgesamtstruktur (Multi-Forest).
Einzeldomänen (Single Domain)
Geeignet für die meisten Fälle
Einzelne DC
Beinhalte alle Netzwerk Ressourcen
 
Tree (Baum)
Nur nötig bei:
Unabhängiger Verwaltung
Wenn Stammdomäne keine Produktionsobjekt enthalten soll.
Dinge können auf Domänen ebenen getrennt werden.

#### Forest

Multiple Forest
Mehrer Stammdomänen -> unterschiedliche Schemas.
Domänen sind parallel zueinander.
Zwei verbundene ADs
 


