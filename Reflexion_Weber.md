# Reflexion zur CI/CD-Pipeline

## Überlegungen zum Aufbau der Pipeline

Die Pipeline in mehrere Jobs unterteilt, um die Aufgaben klar zu trennen.

Der **Linting-Job** prüft den Code-Stil
Der **Testing-Job** würde Junit Tests durchführen doch aufgrund von error missing scripts als Kommentar
Der **Build-Job** erstellt die Anwendung
Der **Deployment-Job** simuliert das Deployment.

Abhängigkeiten:
Build passiert nur wenn der Linting und Testing-Job erfolgreich war.
Deployment passiert nur wenn der Build-Job erfolgreich war.

Verbesserungsvorschläge:
Setup Job einrichten um nicht immer die gleichen Schritte in jedem Job zu wiederholen.
Integration von Docker Hub um das Image zu pushen.