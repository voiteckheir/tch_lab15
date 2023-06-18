# lab15

polecam założyć na githubie i na dockerhubie repozytoria, oba nazwane tak samo np jak u mnie tch_lab15<br/>
należy pozmieniać nazwy w plikach docker-compose.yml i .github/workflows/main.yml na swoje<br/>

w lab 10 jest instrukcja jak i gdzie dodać sekrety, trzeba dodać 2 sekrety:<br/>
DOCKERHUB_USERNAME - nazwa użytkownika na dockerhub<br/>
DOCKERHUB_TOKEN - token do dockerhub<br/>

workflow_dispatch:      -to pozwala na ręczne uruchomienie workflow z poziomu githuba<br/>
push:
    branches: ["*"]     - uruchamia workflow przy każdym pushu do repozytorium<br/>


<hr/>
komenda do uruchomienia:<br/>
` 
docker compose up -d --build 
`

do uruchomienia z pobraniem obrazów z dockerhuba należy najspierw zalogować sie na dockerhuba na komputerze:<br/>
potem użyć komendy:<br/>
docker compose -f docker-compose2.yml up -d<br/>
lecz nie do końca to działa, wywala: 500 Internal Server Error

<hr/>

<hr/>
komenda do zatrzymania i usunięcia kontenerów:<br/>
` 
docker compose down 
`
<hr/>
Uruchomienie usług w przeglądarce:
Serwer nginx ze stroną:<br/>
` 
http://localhost:6005/  
`
<br/>
phpmyadmin: <br/>
` 
http://localhost:6001/ 
`
<hr/>


