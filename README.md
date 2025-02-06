# Biome.js Dateinamenskonventionen

Diese Dokumentation enthält die wichtigsten Regeln für Dateinamen in Biome.js Projekten.

## Die Regel `use-filenaming-convention`

Diese Regel stellt sicher, dass Dateien nach bestimmten Konventionen benannt werden.

### Standardkonfiguration

```json
{
  "filenaming": {
    "format": "kebab-case"
  }
}
```

### Unterstützte Formate

- `kebab-case`: Wörter durch Bindestriche getrennt (z.B. `my-component.tsx`)
- `snake_case`: Wörter durch Unterstriche getrennt (z.B. `my_component.tsx`)
- `camelCase`: Wörter beginnen mit Großbuchstaben, erster Buchstabe klein (z.B. `myComponent.tsx`)
- `PascalCase`: Alle Wörter beginnen mit Großbuchstaben (z.B. `MyComponent.tsx`)

### Beispiel für biome.json Konfiguration

```json
{
  "linter": {
    "rules": {
      "correctness": {
        "useFilenamingConvention": {
          "level": "error",
          "options": {
            "format": "kebab-case"
          }
        }
      }
    }
  }
}
```

## Tipps zur Verwendung

1. Wählen Sie ein Format und bleiben Sie dabei konsistent
2. Kebab-case ist der Standard und wird häufig in Web-Projekten verwendet
3. PascalCase wird oft für React-Komponenten verwendet
4. Die Regel kann pro Projektordner anders konfiguriert werden

## Quick Reference

| Format     | Beispiel        | Typische Verwendung    |
|------------|-----------------|------------------------|
| kebab-case | my-component    | Allgemeine Dateien     |
| PascalCase | MyComponent     | React-Komponenten      |
| camelCase  | myComponent     | JavaScript-Module      |
| snake_case | my_component    | Backend-Dateien        |