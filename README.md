# How to run reviews service

Reviews service has been developed on Gradle

## License
[MIT License](https://github.com/Bordee2000/itkmitl-bookinfo-reviews/LICENSE)

# How to run with docker

```bash
# Build Docker Image for reviews service
docker build -t ratings .

# Run reviews service on port 8082
docker run -d --name reviews -p 8082:9080 --link ratings:ratings -e 'RATINGS_SERVICE=http://ratings:8080' -e 'ENABLE_RATINGS=true' reviews
```
# How to run with docker-compose

```bash
# Run Docker Compose
docker-compose up
```

* Test with path `/reviews/1` and `/health`