
include ./.env

up:
	docker-compose -p ${PROJECT_NAME} up -d
build:
	docker-compose -p ${PROJECT_NAME} up -d --build
stop:
	docker-compose stop
app:
	docker-compose -p ${PROJECT_NAME} exec app bash
