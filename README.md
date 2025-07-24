# Gourmet-Genie 🍽️

Eine elegante Web-App, die aus Ihren vorhandenen Zutaten raffinierte Gourmet-Rezepte zaubert.

## ✨ Features

- **Zutateneingabe**: Geben Sie Ihre verfügbaren Zutaten ein
- **Optionale Wünsche**: Zusätzliche Anforderungen (Küchenstil, Schwierigkeit, Diät-Präferenzen)
- **KI-generierte Rezepte**: 3 kreative Gourmet-Rezeptvorschläge powered by DeepSeek AI
- **Detaillierte Anleitungen**: Schritt-für-Schritt Kochanweisungen mit Profi-Tipps
- **Einkaufsliste**: Automatische Liste für fehlende Zutaten
- **Apple-Design**: Modernes, responsives Interface im Apple-Stil

## 🚀 Schnellstart

1. **DeepSeek API Key besorgen**
   - Registrieren Sie sich bei [DeepSeek Platform](https://platform.deepseek.com)
   - Erstellen Sie einen API Key

2. **App starten**
   ```bash
   # Öffnen Sie index.html in Ihrem Browser mit API Key Parameter
   file:///pfad/zur/index.html?apikey=sk-xxxxxxxxxx
   ```

3. **Zutaten eingeben und Rezepte generieren**

## 🛠️ Technische Details

### Architektur
- **Single-Page Application**: Alles in einer HTML-Datei
- **Keine Dependencies**: Selbständige Anwendung ohne externe Bibliotheken
- **DeepSeek Integration**: Nutzt DeepSeek Chat API für Rezeptgenerierung

### Projekt-Struktur
```
rezept/
├── index.html          # Hauptanwendung (HTML + CSS + JS)
├── prompt.md          # Ursprüngliche Anforderungen
├── CLAUDE.md          # Entwickler-Dokumentation
└── README.md          # Diese Datei
```

### API Integration
- **Endpoint**: `https://api.deepseek.com/v1/chat/completions`
- **Model**: `deepseek-chat`
- **Authentifizierung**: Bearer Token via URL Parameter

## 🎨 Design

Das Interface folgt Apples Designsprache mit:
- Glassmorphism-Effekten
- Sanften Animationen
- Modernen Farbverläufen
- Responsivem Layout

## 📱 Nutzung

1. **API Key Setup**: Fügen Sie Ihren DeepSeek API Key als URL-Parameter hinzu
2. **Zutaten eingeben**: Listen Sie Ihre verfügbaren Zutaten auf
3. **Wünsche spezifizieren (optional)**: Geben Sie zusätzliche Anforderungen ein wie:
   - Küchenstil (z.B. "französische Küche", "italienisch")
   - Schwierigkeit (z.B. "einfach", "schnell")
   - Diät-Präferenzen (z.B. "vegetarisch", "vegan")
   - Gang-Art (z.B. "Vorspeise", "Hauptgang", "Dessert")
4. **Rezepte generieren**: Klicken Sie "Rezepte generieren"
5. **Rezept auswählen**: Wählen Sie eines der 3 vorgeschlagenen Rezepte
6. **Kochen**: Folgen Sie der detaillierten Anleitung

## 🔧 Entwicklung

Da es sich um eine Single-File-Anwendung handelt:
- **Kein Build-Prozess** erforderlich
- **Direkt im Browser** ausführbar
- **Einfache Bereitstellung** durch Kopieren der HTML-Datei

### Lokale Entwicklung
```bash
# Einfach die index.html im Browser öffnen
open index.html
```

## 🌟 Beispiel-URL
```
index.html?apikey=sk-1234567890abcdef
```

## 📄 Lizenz

Dieses Projekt ist für persönliche und kommerzielle Nutzung frei verfügbar.