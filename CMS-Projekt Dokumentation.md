# CMS-Projekt Dokumentation

## 1. Motivation für das CMS

### Zielgruppe

Das CMS wird für eine **Bildungseinrichtung** (z. B. eine Schule oder Universität) entwickelt. Ziel ist es, das sich die Schüler und Lehrer über Lehrinhalte austauschen können.

### Mehrwerte für die Organisation

- **Effiziente Verwaltung von Inhalten**: Lehrer und Schüler können Notizen und Dokumente zentral speichern.  
- **Benutzerfreundliche Oberfläche**: Einfache Navigation und Suchfunktionen.  
- **Zugriffskontrolle**: Unterscheidung zwischen Lehrern (Redakteure) und Schülern (Leseberechtigung).  
- **SEO-Optimierung**: Inhalte sind gut auffindbar.  
- **Mehrsprachigkeit**: Unterstützung für mehrere Sprachen.  

---

## 2. Begründung für die Wahl des Systems

**Gewähltes CMS:** **WordPress mit Custom Plugins**  

- **WordPress**: Benutzerfreundlich, große Community, viele Plugins verfügbar.  
- **Docker**: Ermöglicht eine einfache lokale Entwicklung und Bereitstellung.  

---

## 3. Lokal lauffähiges CMS mit Beispielinhalten

**Technische Umsetzung**  

- WordPress läuft in einem Docker-Container.  
- Beispielinhalte: Lehrer- und Fachlisten, Beispiel-Mitschriften.  
- 

## 4. Installationsdokumentation

```markdown
# Installation des CMS-Systems  

## Voraussetzungen  
- Docker & Docker Compose  
- Git  
- Node.js (für Hugo)  

## WordPress mit Docker starten  
1. **Repository klonen**  
   ```bash
   git clone https://github.com/dein-repo/cms-projekt.git
   cd cms-projekt
```
# Technische Umsetzung

## 2. Technologie
- **CMS**: WordPress
- **Forum & Authentifizierung**: WPForo
- **Plugins**:
  - The Events Calendar (Kalender)
  - Ad Inserter (Werbung)

## 3. Umsetzung
- **Theme**: Kostenloses WordPress-Theme mit WPForo-Anpassung.
- **Forum**: WPForo als zentrale Funktion.
- **Authentifizierung**: Über WPForo.
- **Event-Kalender**: The Events Calendar.
- **Werbung**: Ad Inserter.

## 4. Hosting
- **VPS** mit dedizierten Ressourcen für hohe Performance.
- **Zentrale Instanz** ermöglicht einfache Kollaboration ohne lokale Installationen.
- **Flexibilität** durch Root-Zugriff für Anpassungen und Optimierungen.
- **Skalierbarkeit** je nach Nutzerwachstum erweiterbar.

## 5. Herausforderungen
- Theme-Anpassung an WPForo.
- Werbung mit Ad Inserter optimieren.
- VPS-Performance verbessern.

WPForo als Kern macht die Plattform funktional und benutzerfreundlich. Der VPS sorgt für Stabilität, Flexibilität und einfachere Zusammenarbeit.


