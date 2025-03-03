# **Dokumentation: WordPress als CMS für eine Schulwebseite**

## **1. Motivation für die Wahl eines CMS**

Für eine **Schulwebseite** ist ein Content-Management-System (CMS) ideal, da es eine einfache Verwaltung von Inhalten ermöglicht. Lehrer, Schüler und Administratoren können Inhalte veröffentlichen, ohne technisches Wissen zu benötigen.

### **Mehrwerte für die Schule**

✅ **Einfache Verwaltung**: Lehrer und Admins können Inhalte schnell aktualisieren.  
✅ **Flexibilität**: Erweiterbar durch Plugins für News, Kalender, Formulare, etc.  
✅ **Responsives Design**: Optimiert für PC, Tablet und Smartphone.  
✅ **Benutzerverwaltung**: Unterschiedliche Berechtigungen für Admins, Lehrer und Schüler.

---

## **2. Wahl des CMS: WordPress**

### **Warum WordPress?**

✔ **Benutzerfreundlich**: Einfache Bedienung ohne Programmierkenntnisse.  
✔ **Große Community**: Viele kostenlose Plugins und Themes.  
✔ **Erweiterbar**: Unterstützt Funktionen wie News, Anmeldeformulare, Kalender und Social-Media-Integration.  

---

## **3. Installation von WordPress (lokal mit Docker)**

### **Schritt 1: Docker installieren**

Lade Docker Desktop herunter und installiere es.

### **Schritt 2: WordPress mit Docker starten**

Erstelle eine `docker-compose.yml`-Datei mit folgendem Inhalt:



```yaml
version: '3.1'
services:
  wordpress:
    image: wordpress
    restart: always
    ports:
      - "8080:80"
    environment:
      WORDPRESS_DB_HOST: db
      WORDPRESS_DB_USER: user
      WORDPRESS_DB_PASSWORD: password
      WORDPRESS_DB_NAME: wordpress
  db:
    image: mysql:5.7
    restart: always
    environment:
      MYSQL_DATABASE: wordpress
      MYSQL_USER: user
      MYSQL_PASSWORD: password
      MYSQL_ROOT_PASSWORD: rootpassword

```

`docker-compose up -d`

Danach kannst du WordPress unter `http://localhost:8080` aufrufen.

---

## **4. Anpassen der Schulwebseite**

### **4.1 Neues Theme einbinden**

1. Gehe zu `Design → Themes → Neues Theme hinzufügen`.
2. Suche nach einem Schul-Theme (z. B. „Education Hub“).
3. Installieren & aktivieren.

### **4.2 Menüführung erstellen**

1. Gehe zu `Design → Menüs`.
2. Erstelle zwei Menüs:
   - **Hauptmenü** (Startseite, News, Lehrer, Fächer, Kontakt)
   - **Footer-Menü** (Impressum, Datenschutz, Sitemap)

### **4.3 Bilder und Medien verwalten**

1. Gehe zu `Medien → Neu hinzufügen`.
2. Lade Bilder für Newsbeiträge, Schulveranstaltungen und Lehrerprofile hoch.

### **4.4 Beiträge und Kategorien verwalten**

1. Erstelle Kategorien für Inhalte (`Beiträge → Kategorien`).
   - News
   - Schulprojekte
   - Lehrer-Interviews

---

## **5. Erweiterungen durch Plugins**

| Funktion                         | Plugin-Empfehlung          |
| -------------------------------- | -------------------------- |
| **Suchfunktion**                 | Relevanssi                 |
| **Kalender für Veranstaltungen** | The Events Calendar        |
| **Bannerwerbung**                | Ad Inserter                |
| **Kontaktformular**              | Contact Form 7             |
| **Newsfeed (RSS-Feed)**          | WP RSS Aggregator          |
| **Benutzerregistrierung**        | User Registration          |
| **Social-Media-Integration**     | Social Media Share Buttons |
| **SEO-Optimierung**              | Yoast SEO                  |
| **Sitemap erstellen**            | Google XML Sitemaps        |

### **5.1 Kontaktformular einrichten**

1. Installiere `Contact Form 7`.
2. Erstelle ein neues Formular unter `Contact → Neu hinzufügen`.
3. Füge den Shortcode `[contact-form-7 id="123" title="Kontakt"]` auf der Kontakt-Seite ein.

### **5.2 Social-Media-Buttons einfügen**

1. Installiere `Social Media Share Buttons`.
2. Konfiguriere Buttons für Facebook, Instagram und LinkedIn.

---

## **6. Benutzerverwaltung**

| Rolle                  | Berechtigung                                                  |
| ---------------------- | ------------------------------------------------------------- |
| **Administrator**      | Kann alles verwalten                                          |
| **Redakteur (Lehrer)** | Kann Beiträge schreiben, aber nicht veröffentlichen           |
| **Schüler (Autor)**    | Kann eigene Beiträge schreiben, aber keine anderen bearbeiten |

### **Benutzer anlegen**

1. Gehe zu `Benutzer → Neu hinzufügen`.
2. Wähle die entsprechende Rolle (Administrator, Redakteur, Autor).

---

## **7. Erweiterte Funktionen**

✅ **Mehrsprachigkeit (K2)**: Plugin „Polylang“ für verschiedene Sprachen.  
✅ **SEO-Optimierung (K4)**: Yoast SEO zur besseren Google-Platzierung.  
✅ **Analyse & Statistik (K5)**: Google Analytics über das Plugin „MonsterInsights“.  
✅ **Dokumentenmanagement (K6)**: WP Document Revisions zur Verwaltung von Dateien.

---

## **8. Präsentation & Fazit**

### **Stärken von WordPress als CMS für eine Schulwebseite**

✔ Einfache Nutzung für Lehrer und Schüler  
✔ Viele kostenlose Themes & Plugins  
✔ Gute Erweiterbarkeit & SEO-Optimierung

### **Schwächen**

❌ Sicherheit: Updates müssen regelmäßig durchgeführt werden  
❌ Performance: Viele Plugins können die Ladegeschwindigkeit verlangsamen

---

## **9. Fazit & Weiterentwicklung**

Mit WordPress kann eine **moderne Schulwebseite** umgesetzt werden, die **News, Lehrer-Profile, Stundenpläne und Veranstaltungen** enthält.  
Für die Zukunft könnte eine **App-Anbindung** oder ein **interner Mitgliederbereich** für Schüler hinzugefügt werden.
