# Datenschutzerklärung — Vontik

**Stand: 2. September 2026**

---

## 1. Verantwortlicher

Niko Korez, Wien, Österreich
E-Mail: niko.korez22@gmail.com

Vontik befindet sich derzeit in einer geschlossenen Testphase und wird nicht kommerziell
angeboten. Mit der Veröffentlichung im App Store wird an dieser Stelle eine ladungsfähige
Geschäftsanschrift ergänzt.

## 2. Der Grundsatz

Vontik ist so gebaut, dass deine Belege so weit wie möglich auf deinem Gerät bleiben.
Texterkennung, die Auswertung von Belegen, die Berechnung von Fristen und die Erinnerungen
laufen **vollständig auf dem iPhone**. Nichts davon benötigt einen Server.

Daten verlassen dein Gerät nur in zwei Fällen, die beide von dir abhängen: wenn du die
Cloud-Synchronisierung aktivierst, und wenn du für schwer lesbare Belege die
Cloud-Unterstützung einschaltest. Beides ist standardmäßig aus bzw. erfordert deine
ausdrückliche Entscheidung.

## 3. Was auf dem Gerät verarbeitet wird

| Daten | Zweck | Wo |
| --- | --- | --- |
| Fotos, Scans und PDFs deiner Belege | Nachweis deines Kaufs | Nur auf dem Gerät, verschlüsselt |
| Erkannter Text aus Belegen | Händler, Datum, Betrag, Produkt ermitteln | Nur auf dem Gerät |
| Kaufdaten (Produkt, Preis, Datum, Seriennummer) | Deine Übersicht, Fristen | Nur auf dem Gerät |
| Berechnete Fristen | Erinnerungen | Nur auf dem Gerät |
| Nutzungszähler (Anzahl erfasster Käufe) | Produktverbesserung | **Nur auf dem Gerät, wird nicht übertragen** |

Belegdateien werden mit der Dateisystem-Verschlüsselung von iOS geschützt
(`completeFileProtection` bzw. `completeUntilFirstUserAuthentication` für geteilte
Dokumente).

### Aus anderen Apps geteilte Dokumente

Wenn du eine PDF-Rechnung, einen Screenshot oder ein Foto über das Teilen-Menü an Vontik
schickst, legt die Erweiterung die Datei in einem gemeinsamen Bereich der App auf deinem
Gerät ab (`group.me.korez.niko.Vontik`). Die Erweiterung selbst wertet nichts aus und
sendet nichts.

Die Datei bleibt dort liegen, bis du den Kauf in der App gesichert hast, und wird dann
gelöscht. Brichst du die Erfassung ab, bleibt sie erhalten und wird beim nächsten Öffnen
wieder angeboten. Sie verlässt dein Gerät dabei nicht.

### Beschädigte Daten

Kann Vontik einzelne gespeicherte Einträge nicht mehr lesen, legt es eine unveränderte
Kopie der betroffenen Datei neben deinem Tresor ab
(`assets-v1.unreadable-<Zeitstempel>.json`), damit nichts überschrieben wird. Diese Kopie
bleibt lokal, wird nicht übertragen und kann über „Alle lokalen Daten löschen" entfernt
werden.

## 4. Texterkennung und künstliche Intelligenz

**Standardmäßig auf dem Gerät.** Vontik nutzt Apples Vision-Framework für die Texterkennung
und, sofern dein Gerät es unterstützt, Apple Intelligence für die Strukturierung. Beides
läuft lokal; Apple erhält dabei keine Belegdaten von uns.

**Optionale Cloud-Unterstützung (nur mit Vontik Pro und nur nach deiner Zustimmung).**
Wenn ein Beleg auf dem Gerät nicht lesbar war, kann Vontik den **erkannten Text** an einen
von uns betriebenen Server senden, der ihn an das Sprachmodell *Claude Haiku* von
**Anthropic PBC** weitergibt.

Dabei gilt:

- Übertragen wird **nur der erkannte Text**, niemals das Bild oder das PDF.
- Vor der Übertragung werden personenbezogene Stellen automatisch entfernt: E-Mail-Adressen,
  IBANs, Telefonnummern, Kunden- und Kartennummern sowie Zeilen hinter Bezeichnungen wie
  „Kunde", „Lieferadresse" oder „Rechnungsadresse".
- Es werden höchstens 120 Zeilen bzw. 7.500 Zeichen übertragen.
- Der Aufruf erfolgt **nur**, wenn die Auswertung auf dem Gerät eine konkrete Angabe nicht
  ermitteln konnte.
- Die Anzahl dieser Anfragen ist **pro Monat und Konto begrenzt** (derzeit 60). Ist das
  Kontingent aufgebraucht, fragt die App gar nicht mehr an und die Auswertung läuft
  wieder ausschließlich auf dem Gerät.
- Unser Server speichert den Belegtext **nicht**. Er zählt lediglich die Anzahl der
  Anfragen pro Konto und Monat.
- **Rechtsgrundlage:** deine Einwilligung, Art. 6 Abs. 1 lit. a DSGVO. Du kannst sie
  jederzeit in den Einstellungen widerrufen; die App funktioniert dann vollständig weiter.
- **Drittland:** Anthropic PBC hat seinen Sitz in den USA. Die Übermittlung erfolgt auf
  Grundlage deiner Einwilligung sowie der vertraglichen Zusicherungen des Anbieters.

## 5. Konto und Cloud-Synchronisierung (optional)

Vontik funktioniert vollständig ohne Konto. Wenn du die Synchronisierung aktivierst,
verwenden wir **Firebase** (Google Ireland Limited) für Anmeldung, Datenbank und
Dateispeicher.

Dabei werden verarbeitet:

- eine anonyme oder mit Apple bzw. E-Mail verknüpfte Nutzer-ID,
- deine E-Mail-Adresse, falls du dich damit anmeldest,
- deine Kaufdaten und die zugehörigen Belegdateien.

Deine Daten liegen in einem nach Nutzer-ID getrennten Bereich; die Sicherheitsregeln lassen
Zugriff ausschließlich für dein eigenes Konto zu.

**Rechtsgrundlage:** Vertragserfüllung, Art. 6 Abs. 1 lit. b DSGVO.

## 6. Mitteilungen

Erinnerungen an ablaufende Fristen werden **auf deinem Gerät** geplant und ausgelöst. Es
wird kein Server verwendet und es werden keine Daten dafür übertragen. Du erteilst die
Erlaubnis dafür beim ersten Kauf mit einer Frist und kannst sie jederzeit in den
iOS-Einstellungen widerrufen.

## 7. Käufe

Vontik Pro wird über Apples In-App-Kauf abgewickelt. Wir erhalten von Apple **keine**
Zahlungsdaten. Ob ein Abonnement aktiv ist, ermittelt die App über StoreKit auf dem Gerät.

## 8. Analyse und Tracking

**Vontik enthält kein Tracking, keine Werbe-IDs und keine Analyse-SDKs.** Nutzungszähler
(zum Beispiel wie viele Käufe erfasst wurden) werden ausschließlich lokal gespeichert und
nicht übertragen. Inhalte von Belegen werden dabei technisch nicht erfasst.

Deine Daten werden nicht verkauft und nicht für Werbung verwendet.

## 9. Speicherdauer

- **Auf dem Gerät:** bis du die Daten löschst oder die App entfernst.
- **Geteilte, noch nicht erfasste Dokumente:** bis der zugehörige Kauf gesichert ist. Bis
  dahin liegen sie im gemeinsamen Bereich der App auf deinem Gerät.
- **In der Cloud (falls aktiviert):** bis du sie löschst. Die App bietet dafür „Kontodaten
  löschen" und „Alle lokalen Daten löschen".
- **Beim Server für die Cloud-Unterstützung:** der Belegtext wird nicht gespeichert; der
  monatliche Zähler wird nach etwa 70 Tagen automatisch gelöscht.

## 10. Deine Rechte

Dir stehen nach DSGVO Auskunft (Art. 15), Berichtigung (Art. 16), Löschung (Art. 17),
Einschränkung (Art. 18), Datenübertragbarkeit (Art. 20) und Widerspruch (Art. 21) zu.
Eine erteilte Einwilligung kannst du jederzeit widerrufen.

Wende dich dafür an niko.korez22@gmail.com.

Du hast außerdem das Recht auf Beschwerde bei einer Aufsichtsbehörde. In Österreich:
**Österreichische Datenschutzbehörde**, Barichgasse 40–42, 1030 Wien, dsb.gv.at

## 11. Kinder

Vontik richtet sich nicht an Kinder unter 16 Jahren und erhebt nicht wissentlich Daten
von ihnen.

## 12. Änderungen

Wesentliche Änderungen dieser Erklärung werden in der App bekannt gegeben. Das Datum oben
zeigt den jeweils aktuellen Stand.
