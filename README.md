Uruchomienie stack i phpMyAdmin: ```docker compose up -d```.

Utworzenie testowej bazy danych: ```docker exec <nazwa_kontenera> mysql --execute="CREATE DATABASE <nazwa_bazy_danych>" --user=<nazwa_uzytkownika> --password=<haslo_uzytkownika>```, w moim przypadku: ```docker exec zadanie2-mysql-1 mysql --execute="CREATE DATABASE test" --user=root --password=password```.

Generowanie pliku ilustrującego strukturę projektu: ```docker container run --rm -it --name mgraph -v $(pwd):/input pmsipilot/docker-compose-viz render -m image docker-compose.yaml```, wynik w moim przypadku:
![docker-compose.png](https://github.com/Owjeczka/zadanie2/blob/master/docker-compose.png)