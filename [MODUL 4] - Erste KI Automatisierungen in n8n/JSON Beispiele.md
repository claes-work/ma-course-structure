```json
{
  "name": "Anna"
}
```

```json
{
  "name": "Anna",
  "email": "anna@beispiel.de"
}
```

```json
{
  "betreff": "Bewerbung als Projektmanagerin",
  "text": "Sehr geehrtes Team, hiermit bewerbe ich mich auf die ausgeschriebene Stelle.",
  "anhaenge": [
    "lebenslauf.pdf",
    "zeugnis.pdf"
  ]
}
```

```json
{
  "betreff": "Bewerbung als Projektmanagerin",
  "text": "Sehr geehrtes Team, hiermit bewerbe ich mich auf die ausgeschriebene Stelle.",
  "anhaenge": [
    {
      "datei": "lebenslauf.pdf",
      "groesse": "245 KB"
    },
    {
      "datei": "zeugnis.pdf",
      "groesse": "180 KB"
    }
  ]
}
```

```json
{
  "name": "Tech Solutions GmbH",
  "gruendungsjahr": 2015,
  "mitarbeiter": "13"
  "adresse": {
    "strasse": "Hauptstraße",
    "hausnr": "12",
    "postleitzahl": "10115",
    "stadt": "Berlin"
  }
}
```

```json
$json.name
$json.email
$json.adresse.strasse
$json.anhaenge[0]
$json.anhaenge[1]
```
