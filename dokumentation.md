# Installationsdokumentation: WordPress-Schulwebseite

## Einleitung
WordPress wurde als CMS für die Schulwebseite gewählt, weil es einfach zu bedienen ist und viele Funktionen bietet. Lehrer, Schüler und Administratoren können Inhalte ohne Programmierkenntnisse verwalten.

Das Hosting erfolgt auf einem eigenen Server. Dadurch ist die Zusammenarbeit einfacher, da alle Beteiligten direkten Zugriff auf die Webseite haben.

---

## Installation mit Docker

### Voraussetzungen
- Docker und Docker Compose sind installiert.

### WordPress mit Docker starten
1. Erstelle eine `docker-compose.yml`-Datei mit folgendem Inhalt:

```yaml
services:
  db:
    image: mariadb:10.6.4-focal
    command: '--default-authentication-plugin=mysql_native_password'
    volumes:
      - db_data:/var/lib/mysql
    restart: always
    environment:
      - MYSQL_ROOT_PASSWORD=${MYSQL_ROOT_PASSWORD}
      - MYSQL_DATABASE=${MYSQL_DATABASE}
      - MYSQL_USER=${MYSQL_USER}
      - MYSQL_PASSWORD=${MYSQL_PASSWORD}
    expose:
      - 3306
      - 33060
  wordpress:
    image: wordpress:latest
    volumes:
      - wp_data:/var/www/html
    ports:
      - 80:80
    restart: always
    environment:
      - WORDPRESS_DB_HOST=${WORDPRESS_DB_HOST}
      - WORDPRESS_DB_USER=${WORDPRESS_DB_USER}
      - WORDPRESS_DB_PASSWORD=${WORDPRESS_DB_PASSWORD}
      - WORDPRESS_DB_NAME=${WORDPRESS_DB_NAME}
volumes:
  db_data:
  wp_data:
```

2. Führe `docker-compose up -d` aus.
3. Rufe die Seite unter `http://localhost:8080` auf.

---

## Anpassung der Schulwebseite

### Theme installieren
1. Gehe zu `Design → Themes → Neues Theme hinzufügen`.
2. Suche nach einem passenden Schul-Theme.
3. Installiere und aktiviere das Theme.

### Menüstruktur anlegen
1. Gehe zu `Design → Menüs`.
2. Erstelle ein Hauptmenü (z. B. Startseite, News, Lehrer, Kontakt).
3. Erstelle ein Footer-Menü (z. B. Impressum, Datenschutz).

### Bilder und Medien verwalten
1. Gehe zu `Medien → Neu hinzufügen`.
2. Lade Bilder für News, Veranstaltungen und Lehrerprofile hoch.

### Beiträge und Kategorien verwalten
1. Gehe zu `Beiträge → Kategorien`.
2. Lege Kategorien an (z. B. News, Schulprojekte, Interviews).

---

## Unsere Plugins

| Funktion                         | Plugin                     |
|----------------------------------|----------------------------|
| Kalender für Veranstaltungen     | The Events Calendar        |
| Kontaktformular                  | Contact Form 7             |
| Social-Media-Integration         | Social Media Share Buttons |
| Mehrsprachigkeit                 | TranslatePress             |
| News-Widgets                     | WP News and Scrolling Widgets |
| Forum                             | wpForo                     |
| SEO-Optimierung                   | Yoast SEO                  |

### Kontaktformular einrichten
1. Installiere `Contact Form 7`.
2. Erstelle ein neues Formular.
3. Füge den Shortcode `[contact-form-7 id="123" title="Kontakt"]` auf der Kontakt-Seite ein.

### Social-Media-Buttons einbinden
1. Installiere `Social Media Share Buttons`.
2. Füge Buttons für Facebook, Instagram und LinkedIn hinzu.

---

## Unsere Rollen

| Rolle                  | Berechtigung                                       |
|------------------------|---------------------------------------------------|
| Administrator          | Kann alles verwalten                             |
| Redakteur (Lehrer)     | Kann Beiträge schreiben, aber nicht veröffentlichen |
| Schüler (Autor)       | Kann eigene Beiträge schreiben                   |

### Benutzer anlegen
1. Gehe zu `Benutzer → Neu hinzufügen`.
2. Wähle eine Rolle (Administrator, Redakteur, Autor).

---

## Stärken und Schwächen von WordPress

### Vorteile
- Einfache Bedienung für Lehrer und Schüler
- Viele kostenlose Themes und Plugins
- Gute Erweiterbarkeit und SEO-Optimierung

### Nachteile
- Regelmäßige Updates notwendig
- Zu viele Plugins können die Geschwindigkeit beeinträchtigen

---
