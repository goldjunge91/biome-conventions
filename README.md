# Biome.js Dateinamenskonventionen

## Regel: useFilenamingConvention

Diese Biome-Regel ist inspiriert von der `filename-case` Regel aus eslint-plugin-unicorn. Sie stellt sicher, dass Dateien nach bestimmten Konventionen benannt werden.

### Konfiguration in biome.json

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

### Unterstützte Formate

- `kebab-case`: Wörter durch Bindestriche getrennt (z.B. `my-component.tsx`)
- `snake_case`: Wörter durch Unterstriche getrennt (z.B. `my_component.tsx`)
- `camelCase`: Wörter beginnen mit Großbuchstaben, erster Buchstabe klein (z.B. `myComponent.tsx`)
- `PascalCase`: Alle Wörter beginnen mit Großbuchstaben (z.B. `MyComponent.tsx`)

## Vergleich mit ESLint Unicorn

| ESLint Unicorn Rule | Biome Rule |
|-------------------|------------|
| filename-case | useFilenamingConvention |

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