## Repository zum Hanser-Buch *Machine Learning für Zeitreihen* (2021)
### Arbeiten mit dem Repository 
Die Ordner des Repositorys sind entlang der Kapitel des Buches organisiert. 
In den Kapiteln finden Sie jeweils die Codebeispiel als *Jupyter Notebooks* (\*.ipynb-Dateien). 
Sie können das komplette Repository entweder auf ihren Rechner herunterladen oder auf die Jupyter Notebooks direkt im Internet zugreifen 
und den Code und die Resultate einsehen.<br><br>
Wenn Sie das Repository herunterladen möchten, müssen Sie *git* auf ihrem Rechner installiert haben. Die Software ist kostenlos verfügbar
zum Beispiel unter *https://git-scm.com/downloads*. Wenn Sie die Software installiert haben, können Sie das komplette Repository
aus dem Terminal-Fenster mit folgendem Befehl lokal speichern:<br>
***git clone https://github.com/tplusone/hanser_ml_zeitreihen.git*** 
<br>
### Virtuelle Umgebung
Die Datei **requirements.txt** enthält alle Python-Bibliotheken, die zur Ausführung der Codebeispiele notwendig sind. 
Wenn Sie eine virtuelle Umgebung in Anaconda anlegen möchten, die diese Bibliotheken enthält, navigieren Sie über das Anaconda-Terminalfenster
(Anaconda Prompt) einfach in den Basisordner des Repositories (*hanser_ml_zeitreihen*) und geben 
dann folgenden Befehl unter Einfügung eines Namens für die env *<env_name>* ein:<br>
*conda create --name <env_name> --file requirements.txt* <br>
Nach Fertigstellung der Environment lässt sich die Umgebung mit *conda activate <env_name>* einfach aktivieren.<br>
Wenn Sie stattdessen mit *pip* arbeiten, können Sie die Bibliotheken auch mit folgendem Befehl in ihre Umgebung laden:<br>
*pip install -r requirements.txt* <br>
Alternativ können Sie die notwendigen Bibliotheken natürlich auch manuell installieren. Sie benötigen im Wesentlichen folgende Module:<br>
- python, Version=3.7.7
- statsmodels=0.11.1
- pandas, Version=1.1.1
- scikit-learn, Version=0.22.1
- tensorflow, Version=2.1.0
- seaborn, Version=0.10.1

### Kontakt bei Fragen und Problemen
Wenn Sie Fragen zum Code oder zum Buch haben, können Sie entweder hier auf *github* einen *Issue* eröffnen oder sich direkt per Mail
an *tplusone[at]posteo.de* wenden.
