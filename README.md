# lab11v3
<hr/>
komenda do uruchomienia:<br/>
` 
docker compose up -d --build 
`
<hr/>
komenda do zatrzymania i usunięcia kontenerów:<br/>
` 
docker compose down 
`
<hr/>
Uruchomienie usług w przeglądarce:
Serwer nginx ze stroną:<br/>
` 
http://localhost:6666/  
`
<br/>
phpmyadmin: <br/>
` 
http://localhost:6001/ 
`
<hr/>
Port 6666 jest domyślnie zastrzeżony
Odblokowanie portu 6666:
https://thegeekpage.com/err-unsafe-port/

wyświetlana strona:<br/>
![image](https://github.com/VoiteckHeira/lab11v3/assets/91530837/561b9ca7-d8a8-4b5d-ba6d-25802b5e57f9)

<hr/>
dodany jest również wolumen z logami z kontenerów, głównie do testów
oraz wolumen data, w którym znajduje się plik index.php

Reprezentacja graficzna <br/>
https://blog.baslijten.com/how-to-visualize-your-docker-composition/ <br/>
komendę odpalamy znajdując się w folderze z docker-compose.yml
komenda:<br/>
`
docker run --rm -it --name dcv -v ${PWD}:/input pmsipilot/docker-compose-viz render -m image docker-compose.yml --output-file=tch_lab11_wizualizacja.png --force 
`
<br/>
wynik:<br/>
 ![tch_lab11_wizualizacja](https://github.com/VoiteckHeira/lab11v3/assets/91530837/efb7de20-fe80-4463-ba11-bd930e778cc9)
<hr/>

drzewo plików: <br/>
├── data <br/>
│   └── index.php<br/>
├── logs<br/>
├── mysql<br/>
│   └── Dockerfile<br/>
├── nginx<br/>
│   ├── default.conf<br/>
│   └── Dockerfile<br/>
├── php<br/>
│   └── Dockerfile<br/>
├── phpmyadmin<br/>
│   └── Dockerfile<br/>
│<br/>
└── docker-compose.yml<br/>
