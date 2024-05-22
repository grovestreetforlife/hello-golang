# CI/CD в GithubActions.
Создаём рабочие процессы (workflow) для интеграции (CI) и развертывания (CD) на примере простейшего приложения и GithubActions.
Так же используем Docker для создания и публикации Docker-образа в Docker Hub.


- Собрать образ: docker build -t golang-hello:v1.0.0 .
- Запустите контейнер: docker run golang-hello:v1.0.0

Запустить deploy:
1. git tag v1.0.1
2. git push --tags

Запуск контейнер из DockerHub:
1. docker pull --platform linux/x86_64 <Ваш Docker ID>/hello-golang:1.0.0
2. docker run --platform linux/x86_64 <Ваш Docker ID>/hello-golang
