Go
version: 1.22.4
Port: 8080

Req: postgress

- Dev:

  - run: go run cmd/journey/journey.go

- Prod - dockerfile:

  - build: go build cmd/journey/journey.go
  - run: go run cmd/journey/journey.go

- docker commands:
  - docker image ls
  - docker ps
  - docker logs
  - docker build -t api-journey-v2 .
  - docker run -d -p 8080:8080 api-journey-v2
