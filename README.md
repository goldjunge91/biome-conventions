# Biome.js Dateinamenskonventionen

## Regel: useFilenamingConvention

Diese Biome-Regel überprüft die Namenskonventionen von Dateien. Sie entspricht der `filename-case` Regel aus eslint-plugin-unicorn.

### Konfiguration in biome.json

```json
{
  "linter": {
    "rules": {
      "style": {
        "useFilenamingConvention": {
          "level": "error"
        }
      }
    }
  }
}
```

Mit benutzerdefinierten Optionen:

```json
{
  "linter": {
    "rules": {
      "style": {
        "useFilenamingConvention": {
          "level": "error",
          "options": {
            "format": ["camelCase", "kebab-case"]
          }
        }
      }
    }
  }
}
```

### Unterstützte Formate

Die folgenden Formate werden unterstützt:
- `camelCase`: myComponent.js
- `kebab-case`: my-component.js
- `snake_case`: my_component.js
- `pascalCase`: MyComponent.js

### Spezielle Dateinamen
- Dateien können mit einem Punkt oder Pluszeichen beginnen: `.filename.js`, `+filename.js`
- Präfixe und Suffixe mit Unterstrichen sind erlaubt: `__filename__.js`, `.__filename__.js`
- Das Pluszeichen-Präfix wird von Frameworks wie SvelteKit und Vike verwendet

### Vergleich mit ESLint Unicorn

| ESLint Unicorn | Biome | Beschreibung |
|----------------|-------|--------------|
| filename-case | useFilenamingConvention | Erzwingt eine konsistente Namensgebung für Dateien |

## Standardverhalten

- Die Regel prüft standardmäßig auf `kebab-case`
- Mehrere Formate können in den Optionen angegeben werden
- Die Regel befindet sich in der Kategorie "style"

## Quick Reference

| Format     | Beispiel     | Anmerkung |
|------------|--------------|-----------|
| kebab-case | my-file.js   | Standard  |
| camelCase  | myFile.js    | Optional  |
| snake_case | my_file.js   | Optional  |
| pascalCase | MyFile.js    | Optional  |