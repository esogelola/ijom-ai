Running th application locally
docker-compose up --build (Builds the container and runs it)

docker-compose up for regular running

Stopping the application
docker-compose stop (to ensure containers are stopped correctly)

clear docker containers, docker-compose rm -f (if need to recursivley he has a metod in the video)

docker-compose exec <service_name> is for running commands in a docker container, aka tests commands


Running Tests
docker-compose exec website py.test ijom/tests


Running Test Coverage
docker-compose exec website py.test --cov-report term-missing --cov ijom

Running Flake8 (Linter) and excluding init files (modules files)
docker-compose exec website flake8 . --exclude __init__.py

* can also bash enter the docker container to execute commands directly ^


* Looks like instance/settings.py takes a higher precedence than config/settings.py