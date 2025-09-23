# Repository mit Upstream synchronisieren

Wenn du ein Repository geforkt hast, bekommst du nicht automatisch die neuesten Änderungen vom Original-Repository (Upstream).  
Hier sind die Schritte, um dein Fork aktuell zu halten:

---

## 1. Upstream-Remote hinzufügen
Diesen Schritt machst du nur einmal:

git remote add upstream git@github.com:saeedhei/Team-BerlinDevHub.git
Prüfen, ob es geklappt hat:

git remote -v
Du solltest upstream und origin sehen.

2. Neueste Änderungen holen
git fetch upstream

3. Änderungen in deinen Branch übernehmen
Falls dein Haupt-Branch main heißt:

Variante A – Merge (empfohlen für die meisten Teams):

git checkout main
git merge upstream/main

Führt die Änderungen aus upstream mit deinem Branch zusammen und erstellt einen Merge-Commit.
Die Historie bleibt vollständig nachvollziehbar.

Variante B – Rebase (Alternative für eine lineare Historie):

git checkout main
git rebase upstream/main

Deine lokalen Commits werden auf die neuesten Commits von upstream „oben drauf“ gesetzt.
Das Ergebnis ist eine saubere, lineare Git-Historie, aber bei Konflikten kann es aufwendiger werden.

4. Änderungen in deinen Fork pushen

git push origin main
Damit bleibt dein Fork immer auf dem neuesten Stand mit dem Original-Repository.
