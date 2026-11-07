# ILLUMINA – Find your style

Ein responsiver, lokal funktionierender MVP für die visuelle Tattoo-Beratung. Entwickelt mit Next.js, React, TypeScript und Tailwind CSS.

## Voraussetzungen

- Node.js 20 oder neuer
- npm

## Lokal starten

```bash
npm install
npm run dev
```

Anschließend im Browser **http://localhost:3000** öffnen. Für einen iPad-Test im selben WLAN kann die lokale Netzwerkadresse des Entwicklungsrechners genutzt werden (ggf. `npm run dev -- --hostname 0.0.0.0`).

## Funktionsumfang

1. Startbildschirm mit ILLUMINA-Branding
2. Neue Beratung starten
3. Stilfilter auswählen
4. Karten mit Touch-Swipe oder Buttons bewerten
5. Überspringen und letzte Bewertung zurücknehmen
6. Favoriten ansehen, filtern und vergrößern
7. Freiwilligen Beratungsleitfaden ausfüllen
8. Zusammenfassung und Textdatei-Export
9. Lokale Speicherung im Browser (`localStorage`)

## Bildrechte

Alle sechs Grafiken unter `public/images` sind eigens erstellte **schematische Demoillustrationen** und ausdrücklich **keine Tattoo-Fotografien**. Sie dienen ausschließlich zum Testen der Oberfläche. Vor dem Einsatz mit echten Tattoo-Fotos müssen Einwilligungen und passende Nutzungsrechte dokumentiert werden.

## Demo-Bilder austauschen

1. Lizenzierte Bilder in `public/images/` ablegen.
2. `src/lib/tattoos.ts` öffnen.
3. Den jeweiligen `image`-Pfad und die Metadaten anpassen.
4. Die Demo-Kennzeichnung in `src/app/page.tsx` durch eine passende Künstler:innen- und Rechteangabe ersetzen.

## Test-Checkliste

- [ ] Start → Filter → Karten → Favoriten → Leitfaden → Zusammenfassung
- [ ] Links/rechts auf einem Touchscreen swipen
- [ ] Buttons als Swipe-Alternative benutzen
- [ ] Stilfilter wechseln
- [ ] Leere Favoritenliste testen
- [ ] Seite neu laden: Beratung bleibt erhalten
- [ ] Neue Beratung: alte Daten werden zurückgesetzt
- [ ] TXT-Datei exportieren
- [ ] Smartphone, iPad und Desktop prüfen

## GitHub und Veröffentlichung

1. Ein neues, leeres GitHub-Repository erstellen.
2. Die Dateien aus diesem Ordner in das Repository hochladen (ohne `node_modules` oder `.next`).
3. Bei [Vercel](https://vercel.com) anmelden und **Add New → Project** auswählen.
4. GitHub-Repository importieren; Framework **Next.js** automatisch erkennen lassen.
5. **Deploy** auswählen. Vercel stellt eine öffentliche HTTPS-Adresse bereit.

## Architektur und Einschränkungen

- `src/lib/tattoos.ts`: typisierte Demodaten und Fragen
- `src/app/page.tsx`: MVP-Beratungsablauf
- `src/app/globals.css`: Designsystem und Animationen
- `public/images/`: eigenständige grafische Platzhalter

Dies ist ein **lokaler Prototyp**. Es gibt keine Anmeldung, zentrale Datenbank, Kundenarchive, Bild-Uploads oder PDF-Exporte. Die Speicherung erfolgt ausschließlich im jeweiligen Browser und kann beim Löschen von Browserdaten verloren gehen. Auf gemeinsam genutzten Geräten keine personenbezogenen oder sensiblen Kundendaten eingeben. Für den produktiven Betrieb sind Authentifizierung, sichere Datenspeicherung, Rechteverwaltung und Datenschutzkonzept erforderlich.
