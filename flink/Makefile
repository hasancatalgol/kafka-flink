.PHONY: flink-up flink-sql

# Start Flink services and immediately run the SQL client in one command
flink-up:
	docker-compose up -d jobmanager taskmanager
	docker rm -f sql-client || true
	docker-compose run --name flink-sql --rm flink-sql

flink-sql:
	docker-compose run --name flink-sql --rm flink-sql