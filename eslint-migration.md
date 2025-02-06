# ESLint Migration Dokumentation

## Aktuelle ESLint Konfiguration

### DevDependencies zu entfernen
```json
{
  "devDependencies": {
    "eslint-plugin-react-hooks": "5.1.0",
    "eslint": "9.18.0",
    "eslint-config-next": "15.1.6",
    "eslint-config-prettier": "10.0.1",
    "eslint-plugin-format": "^1.0.1",
    "eslint-plugin-import": "2.31.0",
    "eslint-plugin-jsx-a11y": "6.10.2",
    "eslint-plugin-react": "7.37.4",
    "@eslint/compat": "1.2.5",
    "@typescript-eslint/eslint-plugin": "8.21.0",
    "@typescript-eslint/parser": "8.21.0",
    "@eslint/eslintrc": "3.2.0",
    "@antfu/eslint-config": "^4.1.1",
    "@eslint/js": "9.18.0",
    "eslint-plugin-react-refresh": "^0.4.18",
    "eslint-plugin-unicorn": "^56.0.1",
    "@eslint-react/eslint-plugin": "^1.26.2",
    "@next/eslint-plugin-next": "15.1.6"
  }
}
```

### Scripts zu entfernen
```json
{
  "scripts": {
    "lint": "NODE_OPTIONS='--max-old-space-size=4096' eslint .",
    "lint:fix": "NODE_OPTIONS='--max-old-space-size=4096' eslint . --fix",
    "lint:dry": "NODE_OPTIONS='--max-old-space-size=4096' eslint . --fix-dry-run -f stylish > 'eslint_$(date +%Y%m%d_%H%M%S).log' 2>&1>",
    "lint:testing": "NODE_OPTIONS='--max-old-space-size=4096' eslint . --debug --fix-dry-run > .logs/eslint_$(date +%Y%m%d_%H%M%S).log 2>&1"
  }
}