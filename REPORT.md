# Отчет по практической работе №1
## Студент: ИМП
## Группа: БСБО-16
## Дата выполнения: 05.03.2026
### 1. Выполненные команды Docker
#### 1.1 Работа с образами
\`\`\`
kari@MIVCHUK:~/containers-lab-1$ docker images
REPOSITORY                 TAG               IMAGE ID       CREATED         SIZE
dhi.io/postgres            15-alpine3.22     d43d9028d0a0   7 days ago      289MB
postgres                   15-alpine         cd848ee12e8e   7 days ago      274MB
postgres                   latest            52ea5ef23f82   7 days ago      456MB
nginx                      latest            fd204fe2f750   9 days ago      161MB
jgraph/drawio              latest            cf96a61257e9   13 days ago     881MB
devprom/alm-app            latest            e761777db47f   3 weeks ago     1.75GB
nginx                      alpine            b76de378d572   4 weeks ago     62.1MB
alpine                     latest            a40c03cbb81c   5 weeks ago     8.44MB
plantuml/plantuml-server   latest            85b1c65e78ae   5 weeks ago     525MB
golang                     1.21-alpine3.20   c2321c7cf721   19 months ago   222MB
mariadb                    10.7              895b6c8829c3   2 years ago     396MB
devprom/math               latest            123cb19d61b0   6 years ago     970MB
\`\`\`
#### 1.2 Работа с контейнерами
\`\`\`
kari@MIVCHUK:~/containers-lab-1$ docker ps -a
CONTAINER ID   IMAGE             COMMAND                  CREATED          STATUS                      PORTS                                     NAMES
086612b9cfaf   nginx:latest      "/docker-entrypoint.…"   27 minutes ago   Up 27 minutes               0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   my-nginx
0182b8025e41   postgres:latest   "docker-entrypoint.s…"   27 minutes ago   Up 27 minutes               5432/tcp                                  my-postgres
dc82e836ecbb   alpine:latest     "sh"                     57 minutes ago   Exited (0) 56 minutes ago                                             test-alpine
\`\`\`
#### 1.3 Работа с томами
\`\`\`
kari@MIVCHUK:~/containers-lab-1$ docker volume ls
DRIVER    VOLUME NAME
local     1a5703fc0b4bdbba9e804c075650de66b772be04dc772b9d38bbb07e830b9ece
local     2ed6684635841373973b394a8bf0ebaaa30fe3b343a09438130897e2de2229d0
local     3e179ccb40c14ef9d1f0e5f1977b9db4c15dd2701933555f864b864aafc42f31
local     90d4b07fca1f037e8e5f6d12bd26b48a870b676d569c7e27c041ea5924ca4e16
local     c817a761adc6d6781f020c805d981c53fdf047b20cf31ca29da72ae7d354e272
local     docker_dbdata
local     my-app-data
local     nginx-static-volume
\`\`\`
### 2. Скриншоты работающего приложения
#### 2.1 Главная страница
![Главная страница](screenshots/main-page.png)
#### 2.2 Добавление пользователя
![Добавление пользователя](screenshots/add-user.png)
#### 2.3 Список пользователей в БД
![PostgreSQL](screenshots/postgres-data.png)
### 3. GitHub Actions
#### 3.1 Успешный запуск workflow
![GitHub Actions](screenshots/github-actions.png)
#### 3.2 Опубликованные образы в GHCR
![GHCR Packages](screenshots/ghcr-packages.png)
### 4. Выводы
В ходе работы я закрепил навыки работы с Docker, с которыми уже был знаком. Новым и полезным опытом стало освоение multi-stage сборки для оптимизации образов и настройка CI/CD пайплайна в GitHub Actions для автоматической публикации образов в GitHub Container Registry.
