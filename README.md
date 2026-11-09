# Gift Battle – Multiplayer-Prototyp

## Enthalten
- Mobiloptimierte Web-App (auf Android im Browser spielbar)
- 6-stellige private Räume, zufällige Warteschlange und zwei Spieler pro Match
- Serverseitig synchronisierter Countdown: 180 Sekunden
- Unbegrenzte Punktestände, vier Testgeschenke, sichtbare Effekte, Sieger und Verliereraufgaben
- Offline-Demo mit Bot (kein Server nötig)

## Online bereitstellen (ohne PC möglich)
1. ZIP auf dem Handy entpacken und die Dateien in ein neues privates GitHub-Repository hochladen (Ordnerstruktur beibehalten).
2. Bei einem Node.js-Hosting-Anbieter wie Render ein neues **Web Service** aus diesem Repository erstellen.
3. Build-Befehl `npm install`, Start-Befehl `npm start`, Node.js 20 oder neuer; einen Tarif wählen, der dauerhaft laufende WebSockets unterstützt.
4. Die vom Hosting-Anbieter bereitgestellte HTTPS-Adresse auf beiden Handys öffnen. Ein Handy erstellt einen Raum; das andere gibt den Code ein. Alternativ tippen beide auf „Gegner suchen“.
5. Auf Samsung in Chrome: Menü > Zum Startbildschirm hinzufügen > Installieren (falls angeboten). Dies ist eine installierbare Web-App, **keine native APK**.

## Lokal ausprobieren
Die Datei `public/index.html` im Handy-Browser öffnen und „Offline-Demo“ wählen. Je nach Android-Browser kann direktes Öffnen lokaler HTML-Dateien eingeschränkt sein.

## Wichtige Grenzen
- Keine TikTok-API oder automatische Geschenk-Erkennung. Alle Geschenke sind Testknöpfe.
- Keine TikTok-Konten, kein Login, keine Profilbilder, keine Echtgeld- oder Geschenkwerte.
- Nicht produktionsreif: keine Nutzerkonten, kein Missbrauchsschutz, keine dauerhafte Datenspeicherung, keine Skalierung über mehrere Serverinstanzen, keine Überwachung oder Moderation.
- Weltweites Matchmaking bedeutet aktuell eine gemeinsame Warteschlange aller verbundenen Nutzer auf **einer** Serverinstanz, nicht eine weltweit verteilte Infrastruktur.
- Bei Disconnect wird das Match beendet; kein Wiederbeitritt.
- Es ist ein Web-App-Prototyp und kein APK-Projekt.
