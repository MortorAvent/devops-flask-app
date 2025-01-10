1. Wprowadzenie
To prosta aplikacja webowa napisana w Pythonie z wykorzystaniem frameworka Flask. Projekt demonstruje podstawy:

Lokalne uruchamianie aplikacji w środowisku Python,

Konteneryzację z wykorzystaniem Dockera.



2. Instrukcje uruchamiania

2.1 Lokalne uruchomienie (bez Dockera)
Sklonuj repozytorium

git clone https://github.com/MortorAvent/devops-flask-app.git

cd devops-flask-app

(Opcjonalnie) Utwórz wirtualne środowisko:

Jak utworzyć środowisko w Pythonie:

Windows:

python -m venv env

env\Scripts\activate

Linux/Mac:

python3 -m venv env

source env/bin/activate

Zainstaluj zależności

pip install -r requirements.txt

Jeśli nie masz pliku requirements.txt, zainstaluj manualnie:

pip install flask

Uruchom aplikację:

python run.py


Sprawdź w przeglądarce

Otwórz stronę: http://127.0.0.1:5000 .


2.2 Uruchomienie w kontenerze Docker

Zbuduj obraz w głównym katalogu projektu, gdzie znajduje się plik Dockerfile, uruchom:

docker build -t devops-flask-app .

Uruchom kontener

docker run -p 5000:5000 devops-flask-app

Dzięki opcji -p 5000:5000 port kontenera jest mapowany na lokalny port 5000.

Sprawdź w przeglądarce

Otwórz http://127.0.0.1:5000. Aplikacja powinna działać tak, jak przy lokalnym uruchomieniu.

