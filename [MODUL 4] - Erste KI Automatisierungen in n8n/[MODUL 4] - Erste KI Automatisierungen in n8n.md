# [MODUL 4] Erste KI-Automatisierungen in n8n

## Ziel dieses Moduls
- Erste produktive Automatisierungen in n8n umsetzen  
- Realistische Büroanwendungsfälle verwenden  
- Microsoft 365 Dienste für DSGVO-konforme Workflows einsetzen  
- Ein KI-Modell für einfache Textaufgaben nutzen  
- Einen Hauptworkflow schrittweise erweitern  
- Klare Abgrenzung zu KI-Agenten treffen (Agenten folgen in Modul 5)  

---

## Überblick und Ergebnisvorschau
Kurzer Einstieg mit Zielbild und Demo des Endergebnisses.  
Am Ende dieses Moduls können Workflows eigenständig erstellt, erweitert, aktiviert und exportiert werden.  

**Beispiel-Usecase:**  
Bewerbungen automatisch erfassen, KI-gestützte Antworten versenden, Rückmeldungen klassifizieren und tägliche Zusammenfassungen im Teams-Chat bereitstellen.  

**Voraussetzungen aus Modul 3:**  
Grundbegriffe in n8n wie Workflow, Node, Trigger, Action, Credentials, Executions, Evaluations als Begriff.  
Zugriff auf Microsoft 365 für E-Mail, Teams und Tabellen. Angelegte Credentials in n8n für die genutzten Dienste.  

---

## Lektionen

1. **Einstieg und Zielbild – Was wir in Modul 4 bauen**  
   Einführung, Zieldefinition und Überblick über die Anwendungsfälle.  
   Kurze Demo des fertigen Endergebnisses.  
   **Ergebnis:** Motivation und Orientierung.

2. **Was ist ein Workflow – Das Grundprinzip von Automatisierung**  
   Erklärung des Workflows als Abfolge automatisierter Schritte.  
   Beispiele aus dem Büroalltag.  
   **Ergebnis:** Verständnis der Grundidee hinter n8n.

3. **Eigenen Workflow anlegen und Canvas bedienen**  
   Neues Projekt erstellen, Oberfläche verstehen, Navigation lernen.  
   - Canvas-Navigation mit Maus und Tastatur  
   - Nodes suchen, verbinden, löschen  
   - Workflow ausführen, aktiv/inaktiv schalten  
   - Executions-Ansicht kennenlernen  
   **Ergebnis:** Souveräne Bedienung der Canvas.

4. **Was sind Nodes – Die Bausteine deiner Workflows**  
   Einführung in die Node-Arten:  
   - Trigger-Nodes  
   - Action-Nodes  
   - Community-Nodes  
   **Ergebnis:** Verständnis, wie einzelne Bausteine eines Workflows funktionieren.

5. **Nodes hinzufügen und verbinden**  
   Praxisübung: Nodes suchen, hinzufügen, verbinden, benennen.  
   **Ergebnis:** Sicherheit im praktischen Aufbau.

6. **Anatomie einer Node – Input, Einstellungen und Output verstehen**  
   Aufbau und Funktionsweise im Detail.  
   - Input-Daten  
   - Konfigurationsbereich  
   - Output-Daten  
   Darstellung im Schema, in Tabellen und im JSON-Format.  
   **Ergebnis:** Verständnis, wie Daten in einer Node verarbeitet werden.

7. **JSON verstehen – So liest du die Daten in n8n**  
   Einführung in die Datenstruktur.  
   - Schlüssel-Wert-Paare  
   - Objekte `{}` und Arrays `[]`  
   - Typische Datentypen  
   - Bedeutung für n8n (z. B. Zugriff auf Felder in Expressions)  
   **Ergebnis:** Sicherheit beim Lesen von Node-Ausgaben.

8. **Ersten Trigger einrichten und ausführen**  
   Workflow starten, Execution-Ansicht öffnen, Output prüfen.  
   Erklärung des leeren Arrays und erste Bearbeitung des Outputs.  
   **Ergebnis:** Verstehen, wie Trigger-Daten in den Workflow fließen.

9. **Workflow skizzieren – Den Ablauf planen**  
   Kurze visuelle oder textliche Planung des Ablaufs.  
   **Ergebnis:** Klarheit über die Struktur vor der Umsetzung.

10. **Formular-Trigger mit Excel verbinden – Bewerbungen automatisch erfassen**  
    Erstellung eines Workflows mit Formulardaten, die in eine Microsoft-Tabelle geschrieben werden.  
    Typische Nodes: Webhook/Microsoft Forms Trigger + Excel Node.  
    **Ergebnis:** Strukturierte Datenerfassung ohne Medienbruch.

11. **Workflows aktivieren und deaktivieren**  
    Bedeutung der Aktivierung, Unterschiede zwischen manueller und geplanter Ausführung.  
    **Ergebnis:** Verständnis über Lebenszyklus eines Workflows.

12. **KI-gestützte Antwortmail mit Outlook versenden**  
    KI-Modell erzeugt eine personalisierte Antwort und versendet sie.  
    DSGVO-Hinweis: Nutzung nur mit Testdaten.  
    **Ergebnis:** Automatische Rückmeldung mit persönlicher Note.

13. **Daten pinnen und wiederverwenden**  
    Erklärung und Praxisbeispiel: Formular-Daten speichern und mehrfach nutzen.  
    **Ergebnis:** Effizienteres Arbeiten und API-Kosten reduzieren.

14. **E-Mail-Trigger und TextClassifier – Eingehende Bewerbungen automatisch erkennen**  
    Eingehende Bewerbungen werden erkannt, klassifiziert und in der Tabelle markiert.  
    **Ergebnis:** Automatische Erkennung und Zuordnung eingehender E-Mails.

15. **Teams-Benachrichtigung bei neuen Bewerbungen**  
    Automatische Teams-Nachricht bei neuer Antwort oder positiver Klassifizierung.  
    **Ergebnis:** Das Team bleibt informiert ohne Postfachchaos.

16. **E-Mails klassifizieren – Werbung, Newsletter und Systemmails erkennen**  
    Erweiterung der Logik, sichere Trennung von wichtigen und unwichtigen Mails.  
    **Ergebnis:** Ordnung im Posteingang.

17. **Unwichtige E-Mails löschen und wichtige labeln**  
    Aufbau auf vorheriger Lektion, Regeln für automatisches Handling.  
    **Ergebnis:** Gesteuerte Inbox-Automatisierung.

18. **Workflow-Historie verstehen und Fehler finden**  
    Nutzung der Execution History, Fehlersuche und Optimierung.  
    **Ergebnis:** Verständnis für Debugging und Nachvollziehbarkeit.

19. **Workflows exportieren, importieren und duplizieren**  
    Projektübertragung und Sicherung.  
    **Ergebnis:** Workflows weitergeben und wiederverwenden.

20. **Ausblick – Workflow für E-Mail-Zusammenfassungen planen**  
    Vorstellung des nächsten Zielbilds: tägliche Zusammenfassungen erstellen.  
    **Ergebnis:** Vorbereitung auf finale Automatisierung.

21. **Geplante Workflows mit Schedule Trigger erstellen**  
    Einführung in geplante Workflows (z. B. täglich um 8 Uhr).  
    **Ergebnis:** Zeitbasierte Automatisierung verstehen.

22. **Felder bearbeiten – Inputdaten aufräumen und anpassen**  
    Felder gezielt bearbeiten, um saubere Datengrundlagen zu schaffen.  
    **Ergebnis:** Verständnis für Datenhygiene in Workflows.

23. **Expressions verstehen – Dynamische Daten mit Formeln steuern**  
    Einführung in Expressions mit Praxisbeispielen (z. B. Datum -24 h).  
    **Ergebnis:** Dynamische Workflows durch Variablen und Logik.

24. **E-Mails der letzten 24 Stunden automatisch abrufen**  
    Anwendung von Expressions in Verbindung mit Zeitsteuerung.  
    **Ergebnis:** Dynamische Eingrenzung von Datensätzen.

25. **Items in n8n verstehen – Wie Daten durch den Workflow fließen**  
    Erklärung des Item-Konzepts mit anschaulicher Analogie (Umzugskarton).  
    **Ergebnis:** Fundamentales Verständnis, wie n8n Daten strukturiert verarbeitet.

26. **Items zusammenfassen – KI-basierte E-Mail-Zusammenfassungen erstellen**  
    Nutzung von LLMs, um mehrere Items (E-Mails) zu verdichten.  
    Inklusive Prompting-Leitfaden:  
    - Ziel definieren  
    - Eingaben präzisieren  
    - Struktur und Stil festlegen  
    - Grenzen und Länge setzen  
    **Ergebnis:** Automatische, strukturierte Zusammenfassungen.

27. **E-Mail-Zusammenfassungen automatisch an Teams senden**  
    Finaler Schritt: Ergebnisse als Teams-Nachricht.  
    **Ergebnis:** Tägliche Übersicht mit allen relevanten Informationen.

28. **Modulabschluss – Recap und Ausblick auf KI-Agenten (Modul 5)**  
    Zusammenfassung der wichtigsten Erkenntnisse:  
    - Workflows und Nodes verstanden  
    - Trigger, Tabellen, Mails und Teams integriert  
    - KI-Komponenten getestet  
    - Daten pinnen gelernt  
    - Klassifikationen und Zusammenfassungen umgesetzt  
    **Ergebnis:** Fertige End-to-End-Automatisierung als Grundlage für Modul 5.  

---

## Assets zum Download
- Formularbeispiel Bewerbungen (Excel)  
- E-Mail-Template für automatisierte Antworten  
- Prompt-Snippets für Klassifizierung und Zusammenfassung  
- Beispiel-E-Mails zur Übung  
- Checkliste für sichere Automatisierungen  

---

## Didaktische Hinweise
- Theorie und Praxis sind klar getrennt, aber eng verzahnt  
- Jede Lektion liefert ein sichtbares Ergebnis  
- Daten pinnen und Expressions werden als Schlüsselfunktionen hervorgehoben  
- Klassifizierungen starten konservativ, Regeln später erweitern  
- DSGVO-Hinweise klar kennzeichnen  
- Evaluations und KI-Agenten folgen in Modul 5  
