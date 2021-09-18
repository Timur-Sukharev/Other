**1.Запуск контейнера**
docker run -p 8888:8888 jupyter/scipy-notebook:33add21fab64


**2.Попасть внутрь контейнера**
docker exec -it <id_container> bash 

**2.Скопировать файл во внутрь контейнера**
docker cp foo.txt mycontainer:/foo.txt
docker cp games.csv 77cc983af67b:/home/jovyan/work/games.csv

**3.Связь докера с локальной дирректорией**
docker run -v /home/timur/files_docker/ju_pgsql_docker:/home/jovyan/ -p 8888:8888 jupyter/scipy-notebook:33add21fab64

**4.Запуск из докерфайла**
docker build . | docker build -t my_notebook .

docker run -v /home/timur/files_docker/ju_pgsql_docker:/home/jovyan/ -p 8888:8888 my_notebook

**5.Запуск docker-compose**
docker-compose up
docker-compose up --build
