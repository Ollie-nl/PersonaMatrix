# JSON Architectuur Uitleg

Hieronder staat een heldere uitleg van de architectuur die gebruikt wordt in de JSON-structuur, geoptimaliseerd voor gebruik met GenAI-tools zoals ChatGPT.

## Structuur en Terminologie

### 📁 `group`
Het hoogste niveau, bevat een bredere verzameling van verwante kenmerken of thema's.
- **Voorbeeld:** "Demografisch & Cultureel".

### 📋 `category`
Elke groep bevat specifieke categorieën. Een categorie representeert één kenmerk of attribuut waarop gebruikers of doelgroepen worden beoordeeld.
- **Voorbeeld:** "Leeftijd", "Genderidentiteit", "Seksuele oriëntatie".

### `id`
Deze id is een unieke identifier voor de categorie.
- **Voorbeeld:** "leeftijd".

### `label`
Deze label is een duidelijke korte beschrijving van de categorie.
- **Voorbeeld:** "Leeftijd van een inwoner".

### 📐 `scale`
Binnen een categorie worden meetbare niveaus of scores (zoals 1 tot 5) gedefinieerd. Dit toont in hoeverre een eigenschap aanwezig is.
- **Voorbeeld:** schaal 1 (laag) tot 5 (hoog).

### 🏷️ `title`
Een kort, duidelijk trefwoord dat elk niveau binnen de schaal omschrijft, bedoeld voor snelle herkenning en duidelijkheid.
- **Voorbeeld:** "Zeer jong", "Jongvolwcategorye", "Middelbare leeftijd", "Oudere volwcategorye", "Senior".

### 📝 `description`
Een uitgebreide toelichting die gedetailleerd aangeeft wat elk niveau betekent. Dit is handig voor documentatie, uitleg en communicatie met stakeholders.
- **Voorbeeld:** "Zeer jong (kind/jongere)", "Jongvolwcategorye", "Middelbare leeftijd", "Oudere volwcategorye", "Senior (pensioenleeftijd)".

## Voorbeeld van Complete Structuur

```json
{
    "group": "Demografisch & Cultureel",
    "category": [
      {
        "id": "leeftijd",
        "label": "Leeftijd",
        "scale": {
          "1": {"title": "Zeer jong", "description": "Zeer jong (kind/jongere)"},
          "2": {"title": "Jongvolwcategorye", "description": "Jongvolwcategorye"},
          "3": {"title": "Middelbare leeftijd", "description": "Middelbare leeftijd"},
          "4": {"title": "Oudere volwcategorye", "description": "Oudere volwcategorye"},
          "5": {"title": "Senior", "description": "Senior (pensioenleeftijd)"}
        }
      }
      ]
} 
```

Deze structuur zorgt voor duidelijke communicatie, eenvoudige integratie met GenAI-tools en goede documentatie voor toekomstig gebruik.