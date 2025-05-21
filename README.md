# winuiwithkiosk
## Problemstellung
Es soll eine WinUI 3 packaged App auf einem Win 11 Tablet gestartet werden und das am besten so, dass die User keinen Zugriff auf etwaige andere installierte Apps oder Windowsfunktionen haben. Also einen sehr restriktiven Kioskmodus.
Das Problem ist, dass eine App die sich nicht im Microsoft Store befindet nicht als App für den Windows Kioskmodus ausgewählt werden kann. Es wurde zwar eine Lösung gefunden mit Hilfe des Windows Configuration Designers (WCD), bei dieser kann einiges gesperrt werden und es steht im Prinzip "nur" der Start Screen zur Verfügung für den User. Am Windows Startscreen kann dann die App per Kachel gestartet werden.
Gewünscht wäre allerdings eine Lösung bei der der User nur automatisch eingeloggt wird und anschließend schon die App startet. Ohne Möglichkeit andere Programme zu starten oder Windows Einstellungen zu ändern.
Ein weiterer Vorteil der packaged App ist nämlich, dass sie sich selber updaten kann. Das ist derzeit aufgrund des Setups bei uns nicht möglich (eigenes VPN Netz mit beschränkten Rechten + .exe Programm).
## Derzeitige Lösung
Im Moment läuft eine Executable (.exe) Version der App auf den Tablets. Diese lässt sich durch eine Einstellung im WCD über den Shelllauncher im angegeben Account starten. Das funktioniert soweit gut, allerdings muss die App dann aufgrund unseres Setups immer händisch geupdatet werden. Das ist in Zukunft zeitlich ein zu großer Aufwand.
## UWP Lösung
Vor der jetzigen .exe Lösung hatten wir eine UWP App. Diese ließ sich ganz einfach im Windows Kiosk wie jede andere Windows App auswählen auswählen. Das ist aber anscheinend nicht mit einer WinUI3 App möglich.
## Gewünschte Lösung
Am liebsten wäre uns die einfache Lösung des Problems mit Hilfe der Windows Kiosk Methode. Sollte eine Lösung über den WCD gefunden werden, welche der des Windows Kiosk gleich kommt, ist das auch akzeptabel.
Die wichtigsten Punkte:
1. Automatisches einloggen
2. Keine Interaktion mit anderen Programmen/Funktionen möglich
3. Automatische Updates der App (zB bei Start der App)
4. Im Fehlerfall sollte die App neu starten und nicht auf einem schwarzen Bildschirm oder ähnlichem hängen bleiben.
5. Kein Must-Have, aber wünschenswert -> Remote Zugriffsmöglichkeit gegeben.
