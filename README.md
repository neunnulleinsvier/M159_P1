#Lernziele Schriftlicher Teil

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

##Domain Name System (DNS)
### Hierarchischer Aufbau und Eigenschaften

###Zonentypen im DNS
* Primärzone: Die Ursprüngliche Quelle für DNS-Daten
* Sekundärzone: Eine Kopie der Primärzone zu Redundanz-Zwecken
* Subzone: Enthält verweise auf DNS-Server anderer Domänen
* AD-Integrierte Zone: Speichert DNS-Zonendaten im AD
