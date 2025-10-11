# [MODUL 5] Dein erster KI Agent

## Ziel dieses Moduls
- Verständnis, was ein KI Agent ist und wie er sich von herkömmlicher Automatisierung unterscheidet  
- Den ersten funktionsfähigen KI Agenten in n8n erstellen  
- Systemnachrichten und Rollen verstehen  
- Memory für Kontext und Verlauf einbinden  
- Einfache Tools mit dem Agenten verbinden (z. B. Excel)  
- Erste Subagents aufbauen und das Prinzip modularer Agenten kennenlernen  

---

## Überblick und Ergebnisvorschau
In diesem Modul entsteht dein erster eigener KI Agent. Du lernst, wie er denkt, reagiert, sich erinnert und Tools nutzt.  
Vom simplen Text-Agent bis zum mehrschichtigen System mit Subagents baust du schrittweise einen Agenten, der Aufgaben versteht, Entscheidungen trifft und eigenständig handelt.  
Voraussetzungen aus Modul 4: Grundkenntnisse in n8n, Verständnis für Workflows, Nodes, JSON Daten und die Nutzung externer Services (z. B. Microsoft 365 oder OpenAI Credentials).

---

## Lektionen

1. **Einstieg und Zielbild für Modul 5**  
   Inhalt: Vorstellung des Zielbilds – was ein KI Agent ist, wie er sich von klassischen Workflows unterscheidet und was du in diesem Modul baust. Kurze Demo des fertigen Agenten (z. B. Office Assistant, der Anfragen beantwortet und Daten in Excel schreibt).  
   Ergebnis: Verständnis des Gesamtziels und Motivation durch ein klares Endbild.  

2. **Minimales Agenten Konzept – Das Grundgerüst**  
   Inhalt: Aufbau eines simplen Agenten mit minimalen Bausteinen.  
   Schwerpunkte:  
   - Der AI Agent Node als Zentrale  
   - Ein LLM als „Brain“ des Agenten  
   - Input, Denken, Output – wie Daten durch den Agenten fließen  
   Praxis: Einen minimalen KI Agenten erstellen, der auf Eingaben reagiert.  
   Ergebnis: Funktionierender Basis-Agent mit Textausgabe.  

3. **System- und User-Messages verstehen**  
   Inhalt: Einführung in die Struktur von Nachrichten im Agenten-Kontext.  
   Schwerpunkte:  
   - Unterschied zwischen System, User und Assistant Message  
   - Wie Systemnachrichten Verhalten und Persönlichkeit steuern  
   - Beispiele für verschiedene Stile: professionell, kreativ, direkt  
   - Kurze Übung: Eigenen Systemprompt anpassen und Wirkung testen  
   Ergebnis: Verständnis, wie man das Denken und Verhalten des Agenten gezielt formt.  

4. **Memory – dein Agent bekommt ein Gedächtnis**  
   Inhalt: Grundlagen des Gedächtnisses für KI Agenten.  
   Schwerpunkte:  
   - Unterschied zwischen Kurzzeit- und Langzeit-Memory  
   - Nutzung des Chat Memory Nodes in n8n  
   - Wie sich der Agent an vorherige Eingaben erinnert  
   - Einfaches Testbeispiel: Name merken und wiedererkennen  
   Ergebnis: Agent mit funktionierendem Kurzzeitgedächtnis.  

5. **Tools anbinden – der Agent lernt zu handeln**  
   Inhalt: Erste Anbindung externer Tools.  
   Schwerpunkte:  
   - Was Tools sind und wann sie aufgerufen werden  
   - Beispiel 1: Excel-Tool einbinden, Kontakte speichern und abrufen  
   - Entscheidungslogik des Agenten – wann er ein Tool nutzt  
   - Grenzen und Fehlerquellen (fehlende Credentials, falsche Formate)  
   Ergebnis: Der Agent kann eigenständig auf externe Daten zugreifen und Aktionen ausführen.  

6. **Prompt Feinschliff – bessere Steuerung bei mehreren Tools**  
   Inhalt: Grundprinzipien eines guten Prompts, sobald mehrere Tools im Spiel sind.  
   Schwerpunkte:  
   - Struktur eines klaren Prompts (Ziel, Kontext, Format, Grenzen)  
   - Beispiel: „Wenn du etwas nicht weißt, frage nach“  
   - Stilrichtlinien: kurz, präzise, reproduzierbar  
   - Hinweis auf das separate Prompting Modul für vertiefte Techniken  
   Ergebnis: Mehr Kontrolle über das Verhalten des Agenten ohne komplexes Prompt Engineering.  

7. **Subagents – spezialisierte Helfer aufbauen**  
   Inhalt: Einführung in Subagents als Erweiterung des Hauptagenten.  
   Schwerpunkte:  
   - Prinzip: Hauptagent als Manager, Subagent als Spezialist  
   - Beispiel: „Finder Felix“ (Recherche) und „Analyse Anna“ (Auswertung)  
   - Aufbau in n8n: Subagent Node hinzufügen, Kommunikation testen  
   Ergebnis: Verständnis, wie komplexe Agentensysteme modular und skalierbar werden.  

8. **Abschluss und Integration – dein erster vollwertiger KI Agent**  
   Inhalt: Zusammenführung aller Bausteine in einem Workflow.  
   Schritte:  
   - Agent Node + Systemnachricht + Memory + Tool + Subagent  
   - Testlauf: Agent beantwortet eine Anfrage, speichert ein Ergebnis und ruft Helfer auf  
   - Kurze Reflexion: Was du bisher gebaut hast und wie du es erweitern kannst  
   Ergebnis: Vollwertiger KI Agent mit eigenem Gedächtnis, Tools und Grundlogik.  

---

## Assets zum Download
- Beispielworkflow „Minimaler Agent“  
- Beispielworkflow „Agent mit Excel Tool“  
- Prompt-Beispiele für Systemnachrichten  
- Memory Beispielkonfiguration  
- Subagent-Vorlage mit Finder Felix und Analyse Anna  

---

## Didaktische Hinweise
- Jede Lektion ergänzt die vorherige, der Agent wird schrittweise erweitert  
- Fokus auf Verständnis der Kernbausteine, nicht auf Perfektion des Prompts  
- Hands-on Charakter: Jede Lektion hat ein sichtbares, funktionierendes Ergebnis  
- Memory wird bewusst früh integriert, um spätere Fehlerquellen zu vermeiden  
- Subagents werden eingeführt, aber noch nicht automatisiert trainiert oder evaluiert  
- Modul endet mit einem echten, lauffähigen KI Agenten – Motivation und Stolz-Moment  

---

## Abschluss und Mini Quiz

Beispielfragen  
1. Was unterscheidet einen klassischen Workflow von einem KI Agenten  
   a) Der Agent kann eigenständig Entscheidungen treffen ✔  
   b) Der Agent läuft nur manuell  
   c) Der Agent hat keine Tools  

2. Welche Rolle spielt die Systemnachricht  
   a) Sie definiert Persönlichkeit und Verhalten ✔  
   b) Sie startet den Workflow  
   c) Sie löscht alte Daten  

3. Warum ist Memory wichtig  
   a) Damit der Agent vergangene Eingaben versteht ✔  
   b) Um API Kosten zu erhöhen  
   c) Um Tools zu deaktivieren  

4. Was sind Tools im Agentenkontext  
   a) Externe Funktionen, die der Agent selbstständig aufrufen kann ✔  
   b) Nur interne Nodes  
   c) Promptbefehle ohne Wirkung  

5. Was ist der Vorteil von Subagents  
   a) Spezialisierte Teilaufgaben durch eigene Mini-Agenten ✔  
   b) Schnellere API Calls  
   c) Weniger Arbeitsspeicherbedarf  
# [MODUL 5] Dein erster KI Agent
