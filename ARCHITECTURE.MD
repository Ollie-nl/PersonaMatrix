# JSON Architectuur Uitleg

Hieronder staat een heldere uitleg van de architectuur die gebruikt wordt in de JSON-structuur, geoptimaliseerd voor gebruik met GenAI-tools zoals ChatGPT.

## Structuur en Terminologie

### 📁 `group`
Het hoogste niveau, bevat een bredere verzameling van verwante kenmerken of thema's.
- **Voorbeeld:** "Skills & Accessibility", "Demographic & Cultural".

### 📂 `category`
Elke groep bevat specifieke categorieën. Een categorie representeert één kenmerk of attribuut waarop gebruikers of doelgroepen worden beoordeeld.
- **Voorbeeld:** "Digital Skills", "Physical Mobility", "Trust in Technology".

### 📏 `scale`
Binnen een categorie worden meetbare niveaus of scores (zoals 1 tot 5) gedefinieerd. Dit toont in hoeverre een eigenschap aanwezig is.
- **Voorbeeld:** schaal 1 (laag) tot 5 (hoog).

### 🏷️ `title`
Een kort, duidelijk trefwoord dat elk niveau binnen de schaal omschrijft, bedoeld voor snelle herkenning en duidelijkheid.
- **Voorbeeld:** "None", "Basic", "Expert".

### 📝 `description`
Een uitgebreide toelichting die gedetailleerd aangeeft wat elk niveau betekent. Dit is handig voor documentatie, uitleg en communicatie met stakeholders.
- **Voorbeeld:** "Not digitally skilled", "Expert in digital skills".

## Voorbeeld van Complete Structuur

```json
{
  "group": "Skills & Accessibility",
  "categories": [
    {
      "id": "digital_skill",
      "title": "Digital Skills",
      "scale": {
        "1": {
          "title": "None",
          "description": "Not digitally skilled"
        },
        "2": {
          "title": "Basic",
          "description": "Basic digital skills"
        },
        "3": {
          "title": "Average",
          "description": "Average digital skills"
        },
        "4": {
          "title": "Good",
          "description": "Comfortable with standard technology"
        },
        "5": {
          "title": "Expert",
          "description": "Expert in digital skills"
        }
      }
    }
  ]
}
```

Deze structuur zorgt voor duidelijke communicatie, eenvoudige integratie met GenAI-tools en goede documentatie voor toekomstig gebruik.