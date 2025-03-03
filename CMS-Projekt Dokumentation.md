# CMS-Projekt Dokumentation

## 1. Motivation für das CMS

### Zielgruppe

Das CMS wird für eine **Bildungseinrichtung** (z. B. eine Schule oder Universität) entwickelt. Ziel ist es, Mitschriften, Protokolle und Lehrmaterialien strukturiert zu verwalten und schnell auffindbar zu machen.  

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
