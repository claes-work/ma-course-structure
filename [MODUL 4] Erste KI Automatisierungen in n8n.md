# [MODUL 4] Erste KI Automatisierungen in n8n

## Ziel dieses Moduls
- Erste produktive Automatisierungen in n8n umsetzen  
- Realistische Büroanwendungsfälle verwenden  
- Microsoft 365 Dienste für DSGVO konforme Workflows einsetzen  
- Ein KI Modell für einfache Textaufgaben nutzen  
- Einen Hauptworkflow schrittweise erweitern  
- Klare Abgrenzung zu KI Agenten treffen, KI Agenten folgen in Modul 5  

---

## Überblick und Ergebnisvorschau
Kurzer Einstieg mit Zielbild und Demo des Endergebnisses. Am Ende dieses Moduls werden Formulardaten strukturiert erfasst, passende Antworten generiert, Rückmeldungen erkannt, Benachrichtigungen in Teams verschickt, E Mails automatisch eingeordnet und regelmäßige Zusammenfassungen erzeugt.  
Voraussetzungen aus Modul 3: Grundbegriffe in n8n wie Workflow, Node, Trigger, Action, Credentials, Executions, Evaluations als Begriff. Zugriff auf Microsoft 365 für E Mail, Teams und Tabellen. Angelegte Credentials in n8n für die genutzten Microsoft Dienste.  

---

## Lektionen

1. **Einstieg und Zielbild für Modul 4**  
   Inhalt: Was in diesem Modul gebaut wird, welche Anwendungsfälle abgedeckt werden und wie die Lektionen aufeinander aufbauen. Kurze Demo des Endergebnisses.  
   Ergebnis: Klare Erwartung und technischer Rahmen.  

2. **Workflow anlegen und Canvas bedienen**  
   Inhalt: Neuen Workflow erstellen, Oberfläche der Canvas verstehen, Navigation und Bedienung.  
   Schwerpunkte:  
   - Canvas Navigation mit Maus und Tastatur, zoomen, pannen  
   - Nodes suchen und hinzufügen, Knoten verbinden, Verbindungen trennen  
   - Workflow ausführen, Unterschied zwischen aktiv und inaktiv  
   - Executions Ansicht kurz zeigen, wo Ausführungen später geprüft werden  
   - Historie orientieren, sinnvolle Benennung und Speichern  
   Ergebnis: Souveräne Bedienung der Canvas.  

3. **Anatomie einer Node**  
   Inhalt: Aufbau einer Node im Detail erklären.  
   Schwerpunkte:  
   - Input: welche Daten eine Node erwartet  
   - Konfigurationsbereich: Optionen und Einstellungen, die man in der Mitte vornimmt  
   - Output: welche Daten erzeugt oder weitergegeben werden  
   - Node Settings: wichtige Konfigurationsmöglichkeiten, die oft übersehen werden  
   Ergebnis: Verständnis für den universellen Aufbau jeder Node und Grundlage für den Praxisteil.  

4. **Trigger plus Tabelle, Bewerbungsformular in Microsoft 365 speichern**  
   Inhalt: Ein einfacher Workflow mit zwei Nodes. Ein Trigger erfasst Formulardaten und schreibt sie in eine Microsoft Tabelle in OneDrive oder SharePoint. Hinweis auf spätere Webhook Einbindung in Webseiten.  
   Ergebnis: Strukturierte Datenerfassung ohne Medienbruch.  
   Typische Nodes: Webhook oder Microsoft Forms Trigger, Microsoft Excel Tabellen Node.  
   Praxishinweise:  
   - Vor dem Aktivieren stets manuell ausführen und Daten prüfen  
   - Executions prüfen, um Fehler zu finden  
   - **Daten pinnen** als Technik merken, um nicht jedes Mal das Formular neu ausfüllen zu müssen (eigene Lektion folgt)  

5. **Automatische Antwortmail mit KI Unterstützung**  
   Inhalt: Erweiterung des Workflows aus Lektion 4. Ein KI Modell erzeugt einen einzigen personalisierten Satz, der in ein vorbereitetes E Mail Template eingefügt wird. Versand über Microsoft 365 Mail.  
   DSGVO Hinweis: Für diese Lektion wird die OpenAI Node genutzt, die **nicht DSGVO konform** ist. Deshalb arbeiten wir ausschließlich mit Beispiel E Mails oder Testaccounts, niemals mit echten personenbezogenen Daten. Die rechtssichere Variante (z. B. Azure gehostete Modelle) zeigen wir im Sondermodul „Rechtssicherer Einsatz“ und technisch umgesetzt in Modul 5 (KI Agenten).  
   Ergebnis: Konsistente Antwort mit persönlicher Note bei minimalem KI Einsatz.  
   Assets: E Mail Template als Download, Beispiel E Mails zur Übung.  
   Typische Nodes: LLM Textgenerator, Microsoft Outlook E Mail senden.  

6. **Sonderlektion: Daten pinnen und wiederverwenden**  
   Inhalt: Erklärung, warum Daten pinnen praktisch ist, und wie man es in n8n nutzt. Beispiel: Bewerbungsformular nicht jedes Mal neu ausfüllen, sondern mit gespeicherten Testdaten arbeiten. Anwendung auch für KI Nodes (z. B. OpenAI), damit keine unnötigen API Calls entstehen.  
   Ergebnis: Effizienteres Arbeiten, Zeit und Kosten sparen.  
   Typische Funktionen: Daten in Executions pinnen, gespeicherte Payloads wiederverwenden.  

7. **Antworten erkennen, E Mail Trigger plus TextClassifier**  
   Inhalt: Neuer Workflow. Eingehende E Mails werden empfangen und per TextClassifier als Antwort oder Nicht Antwort klassifiziert. Relevante Fälle werden in der Tabelle markiert oder mit Status versehen.  
   Ergebnis: Rückmeldungen werden verlässlich erkannt und dokumentiert.  
   Typische Nodes: Microsoft Outlook E Mail Trigger, KI Klassifizierer, Tabellen Update.  
   Praxishinweis: Executions nutzen, um Fehlklassifikationen zu finden und Prompts anzupassen.  

8. **Teams Benachrichtigung bei Antworten**  
   Inhalt: Aufbauend auf Lektion 7 wird bei positiver Klassifizierung eine Nachricht in einen Teams Kanal oder Chat gesendet, optional mit Deep Link zur Original E Mail oder zum Tabelleneintrag.  
   Ergebnis: Das Team bleibt ohne Postfach Chaos informiert.  
   Typische Nodes: Microsoft Teams Nachricht senden.  

9. **Weitere Klassifizierungen, Werbung, Newsletter, Systemmails**  
   Inhalt: Erweiterung der Klassifizierungslogik. Kategorien wie Werbung und Newsletter werden erkannt. Festlegung eines sicheren Handlings, zum Beispiel Label setzen, in Ordner verschieben oder ignorieren.  
   Ergebnis: Entlasteter Posteingang bei erhaltener Kontrolle.  
   Hinweis: Zuerst labeln und prüfen, danach Regeln schrittweise verschärfen.  

10. **E Mail Zusammenfassungen pro Kategorie inklusive Prompting Leitfaden**  
    Inhalt: Für ausgewählte Kategorien werden kompakte Zusammenfassungen erstellt. Fokus auf gutes Prompting für verlässliche Summaries.  
    Ergebnis: Schnellere Orientierung und einheitliche Qualität der Zusammenfassungen.  
    Typische Nodes: LLM Zusammenfasser, Aggregation über mehrere E Mails.  
    Prompting Leitfaden:  
    - Ziel definieren, welche Entscheidung oder Aktion nach der Zusammenfassung möglich sein soll  
    - Eingaben präzisieren, Betreff, Absender, Zeitfenster, Liste der Mails oder zuvor extrahierte Felder übergeben  
    - Struktur anfordern, kurze Stichpunkte plus Ein Satz Fazit und optional ein Next Step  
    - Stil festlegen, neutral und prägnant  
    - Grenzen setzen, keine Annahmen außerhalb der E Mail Inhalte, Unsicherheiten kennzeichnen  
    - Länge begrenzen, zum Beispiel maximal 120 Wörter oder maximal 5 Bulletpoints  
    - Format erzwingen, zum Beispiel Markdown Liste mit festen Schlüsseln oder kompaktes JSON für Weiterverarbeitung  
    - Sensible Daten nur anzeigen, wenn unbedingt erforderlich  

11. **Tägliche Teams Übersicht mit Zusammenfassungen**  
    Inhalt: Geplante Ausführung, zum Beispiel jeden Morgen. Bündelung der Ergebnisse aus Lektion 10 und Versand einer Teams Übersicht mit den wichtigsten Punkten und Links zu Originalmails.  
    Ergebnis: Einheitlicher Tagesstart mit relevanten Informationen.  
    Typische Nodes: Zeitplaner, Tabellen Abfrage, LLM Zusammenfasser, Microsoft Teams Nachricht.  

12. **Recap und Abschluss von Modul 4**  
   Inhalt: Zusammenfassung der wichtigsten Inhalte und Erfolge aus diesem Modul.  
   - Canvas und Node Grundlagen verstanden  
   - Erster Workflow mit Formular und Tabelle erstellt  
   - KI gestützte Antwortmail gebaut (mit DSGVO Hinweis)  
   - Daten pinnen gelernt, um effizienter zu arbeiten  
   - Eingehende Antworten erkannt und klassifiziert  
   - Teams Benachrichtigungen eingerichtet  
   - Weitere Klassifizierungen für E Mails umgesetzt  
   - Zusammenfassungen erstellt und in Teams verteilt  

   Ergebnis: Alle Teilnehmer haben nun ein klares Verständnis dafür, wie n8n Workflows aufgebaut werden und wie sich erste Automatisierungen im Arbeitsalltag einsetzen lassen. Dieses Modul legt die Grundlage, um in Modul 5 auf das nächste Level zu gehen: KI Agenten.  

   Didaktischer Hinweis: Motivation aufgreifen, kurze Reflexion ermöglichen („Was war dein größtes Aha Erlebnis?“), Ausblick auf Modul 5 geben.  

---

## Assets zum Download
- Formularbeispiel Bewerbungen als Excel Vorlage  
- E Mail Template für die automatisierte Antwort  
- Prompt Snippets für Klassifizierung und Zusammenfassung  
- Beispiel E Mails und Beispiel Outlook Account  
- Checkliste für sichere Automatisierung im E Mail Kontext inklusive Fallback Regeln  

---

## Didaktische Hinweise
- Ein Hauptworkflow wird schrittweise erweitert und um einen zweiten Workflow für eingehende Antworten ergänzt  
- Jede Lektion liefert ein sichtbares Ergebnis, das sofort nutzbar ist  
- Klassifizierungen starten konservativ, erst markieren, dann automatisches Verschieben  
- Canvas Grundlagen und Node Aufbau werden vor den ersten praktischen Workflows vermittelt  
- Daten pinnen wird als eigene Lektion hervorgehoben, da es zentral für effizientes Arbeiten ist  
- DSGVO Hinweis wird klar gekennzeichnet, rechtssichere Umsetzung folgt in späteren Modulen  
- Evaluations zur Qualitätsmessung werden später eingeführt, der Einstieg bleibt leicht  

---

## Abschluss und Mini Quiz

Beispielfragen  
1. Was unterscheidet einen aktiven von einem inaktiven Workflow  
   a) Aktiv bedeutet bereit für automatische Auslösung ✔  
   b) Aktiv bedeutet schreibgeschützt  
   c) Inaktiv bedeutet schnellere Ausführung  

2. Welche Teile gehören zur Anatomie einer Node  
   a) Input, Konfiguration, Output ✔  
   b) Nur Output  
   c) Trigger, Tabelle, E Mail  

3. Warum ist Daten pinnen in n8n nützlich  
   a) Es spart Zeit und API Kosten ✔  
   b) Es aktiviert den Workflow automatisch  
   c) Es macht Workflows hübscher  

4. Welche Kombination speichert strukturierte Formulardaten in einer Tabelle  
   a) Trigger allein  
   b) Trigger plus Tabellen Node ✔  
   c) Teams Nachricht  

5. Was ist ein sicherer erster Schritt bei automatischer E Mail Klassifizierung  
   a) Sofort alles löschen  
   b) Zuerst labeln oder markieren und prüfen ✔  
   c) Alles ungelesen lassen  

6. Was verbessert die Qualität einer E Mail Zusammenfassung am stärksten  
   a) Ein langer offener Prompt  
   b) Ein klarer Zielsatz plus feste Struktur und Längenlimit ✔  
   c) Viele Emojis  
