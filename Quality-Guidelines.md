# Richtlinien für Qualitätssicherung im Softwareprojekt (Scrum-basiert)

## Zielsetzung
Wir streben an, ein qualitativ hochwertiges, getestetes und wartbares Softwareprodukt zu entwickeln. Um dies zu erreichen, setzen wir auf verbindliche Regeln, Tools und kontinuierliche Kontrolle innerhalb des Scrum-Prozesses.

---

# Qualitätsrichtlinien

## 1. Codequalität sicherstellen
- **Pull Requests (PRs) sind verpflichtend.**
  - Jeder PR muss mindestens **von einem Teammitglied reviewed** werden (empfohlen: zwei Reviewer).
- **Code muss Best Practices entsprechen:**
  - Namenskonventionen, strukturierte Architektur, verständlicher Code.
- **Pre-Commit Hooks verwenden:**
  - Automatisches Ausführen von Linters und Tests vor jedem Commit.

- **Linters und Formatter verwenden:**
  - Linter prüfen Stil und Syntax (z.B. ESLint für JS/TS, flake8 für Python).
  - Formatter sorgen für einheitliche Formatierung (z.B. Prettier, Black).

## 2. Testing ist Pflicht
- **Unit Tests**, **Integrationstests** und bei Bedarf **End-to-End-Tests** schreiben.
- **Testabdeckung ≥ 80%** auf neuem Code erreichen.
- Testabdeckung wird durch automatisierte Tools überprüft (z.B. Jest Coverage, pytest-cov, JaCoCo).

## 3. Automatisierte Qualitätssicherung
- **Continuous Integration (CI) Workflows** bauen und testen bei jedem PR automatisch.
- **SonarQube** (bzw. **SonarCloud** oder **CodeClimate**) wird eingesetzt:
  - Statische Codeanalyse (Bugs, Code Smells, Security Issues).
  - Qualitätsschwelle ("Quality Gate") muss eingehalten werden.

- **Optional**: Tools wie Dependabot, Renovate, Snyk für Dependency- und Security-Management.

## 4. Scrum Prozess-Integration
- **Definition of Done (DoD)**:
  - Code reviewed
  - Tests vorhanden und erfolgreich
  - Keine kritischen Findings in SonarQube
  - Dokumentation aktualisiert

- **Sprint Review**:
  - Qualität wird mit präsentiert (z.B. Testergebnisse, Coverage Reports).

- **Sprint Retrospektive**:
  - Qualitätsthemen regelmäßig reflektieren.

## 5. Weiterbildung im Team
- Regelmäßige kurze Schulungen (z.B. Testing, Code Review Best Practices).
- Pair Programming wird aktiv gefördert.
- Wiki/Beispiele für guten Code, gute Tests und Reviews.

---

# To-Do-Liste für die Vorbereitung

## Projektstruktur anlegen

| Bereich         | Aufgabe                                                                                      |
|-----------------|---------------------------------------------------------------------------------------------|
| **PR-Template** | Datei `.github/pull_request_template.md` anlegen mit der bereitgestellten Vorlage            |
| **Coding Guidelines** | Dokumentation zu Namenskonventionen, Struktur und Best Practices erstellen (z.B. im Wiki) |
| **Pre-Commit Hooks** | Tools wie [Husky](https://typicode.github.io/husky/) oder [pre-commit](https://pre-commit.com/) einrichten |
| **Linters/Formatter** | Linter (z.B. ESLint, flake8) und Formatter (Prettier, Black) konfigurieren |
| **CI/CD-Workflow** | Setup für automatisiertes Testing, Linting, Build (z.B. GitHub Actions, GitLab CI) |
| **SonarQube/SonarCloud** | Instanz aufsetzen oder Anbindung konfigurieren |
| **Test Frameworks** | Testing-Frameworks einrichten (Jest, Pytest, JUnit etc.) |

---

## 🔹 Tools & Techniken einsetzen

| Zweck                  | Tool-Vorschläge                         |
|-------------------------|----------------------------------------|
| Versionskontrolle       | Git, GitHub/GitLab                     |
| Code Reviews            | Pull Requests mit verpflichtenden Reviews |
| Linters                 | ESLint, flake8, Rubocop                |
| Formatter               | Prettier, Black, gofmt                 |
| Pre-Commit Checks       | Husky, pre-commit                      |
| Testing                 | Jest, Pytest, JUnit                    |
| E2E-Tests               | Cypress, Playwright, Selenium          |
| CI/CD                   | GitHub Actions, GitLab CI/CD, Jenkins  |
| Statische Codeanalyse   | SonarQube, SonarCloud, CodeClimate     |
| Security & Dependencies | Snyk, Dependabot, OWASP Dependency-Check |

---

# Kurze Checkliste zum Mitnehmen

- [ ] `.github/pull_request_template.md` anlegen
- [ ] Coding Guidelines dokumentieren (Wiki, Readme)
- [ ] Pre-Commit Hooks einrichten
- [ ] Linter und Formatter im Projekt integrieren
- [ ] CI/CD-Pipeline konfigurieren (mit Tests, Linting und Build)
- [ ] SonarQube/SonarCloud anbinden
- [ ] Testing Frameworks installieren und konfigurieren
- [ ] Quality Gate Regeln definieren
- [ ] Definition of Done im Team offiziell festlegen
- [ ] Scrum-Termine anpassen: Qualitätsthemen in Planning, Review, Retrospektive einbinden

---

# Zusammenfassung in einem Satz:
> Wir bauen Qualität von Anfang an ein, sichern sie automatisch ab und machen sie zu einem selbstverständlichen Bestandteil unserer Entwicklungskultur.

