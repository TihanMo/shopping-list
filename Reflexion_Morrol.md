# Reflexion

## Aufbau der Pipeline

Die Pipeline besteht aus 4 Jobs:
- Linting
- Testing
- Build
- Deployment

## Optimierung

- `needs` wurde genutzt, um Abhängigkeiten zwischen Jobs zu steuern
- Linting & Tests laufen parallel, um die Ausführungszeit zu reduzieren
- Caching für npm-Pakete wurde hinzugefügt, um npm install zu beschleunigen

## Herausforderungen
- Jest hat keine Tests gefunden → jest.config.js angepasst
- Fehlende ESLint-Konfiguration → .eslintrc.json erstellt
- Dadurch konnte ich die weiteren Jobs zunächst nicht testen

## Kritik und Verbesserungsvorschläge
Die Pipeline läuft stabil und automatisiert den gesamten Prozess. Eine Verbesserung wäre ein echtes Deployment anstelle einer Simulation. Ausserdem könnten Benachrichtigungen bei Fehlern hinzugefügt werden, um Probleme schneller zu erkennen.