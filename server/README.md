# Pocketful room server

`server.pck` is the compiled room server (rooms, private hands, reconnect, bots). The Dockerfile
runs it with the pinned Godot build, headless. It listens on `$PORT` (default 10000) and answers
`GET /health` on the same port that takes the WebSocket connections.

```
docker build -t pocketful-server .
docker run -p 10000:10000 pocketful-server
```
