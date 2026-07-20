# websocket-demo

A simple WebSocket server built with the `ws` library that broadcasts messages to all connected clients in real time.

## How It Works

The server listens on `ws://localhost:8080`. When a client connects and sends a message, the server broadcasts it to **every** connected client (including the sender) prefixed with `Server Broadcast:`.

## Running the Server

```bash
npm run dev
```

This uses `node --watch server.js` which auto-restarts the server on file changes.

## Connecting a Client with wscat

Install `wscat` globally if you don't have it:

```bash
npm install -g wscat
```

Connect to the server:

```bash
wscat -c ws://localhost:8080
```

Once connected, type a message and press Enter. Every connected client will see the broadcasted message in real time. Open multiple terminals with `wscat` to see multi-client messaging live.
