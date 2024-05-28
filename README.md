# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


Docker command

# To build docker image
  docker build . -t rails_docker:2

# To run docker image

	docker run -p 3000:3000 rails_docker:2

# To create network(postgres)
	docker network create rails_postgres

	docker run --network rails_postgres --name postgres -d -e POSTGRES_PASSWORD=postgres postgres:latest

# Run docler with postgres
 docker run --network rails_postgres --name rails_7 -p 3000:3000 rails_docker:2
 docker exec rails_7 rails db:create