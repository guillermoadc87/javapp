build:
	docker build --rm=true -t backbase .

up:
	docker run -d --name backbase -p 8080:8080 backbase

start:
	docker start backbase

stop:
	docker stop backbase

remove:
	docker container rm -f backbase

unit:
	docker exec -i backbase pytest -v -s tests/unit

integration:
	docker exec -i backbase pytest -v -s tests/integration

lint:
	docker exec -i backbase find . -type f -name '*.py' | docker exec -i backbase xargs pylint

tag:
	docker tag backbase:latest backbase:staging