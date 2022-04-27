# Server sent events (SSE)

Server-Sent Events (SSE) is a technology based on HTTP. On the client-side, it provides an API called EventSource (part of the HTML5 standard) that allows us to connect to the server and receive updates from it.

Before making the decision to use server-sent events, we must take into account two very important aspects:

1. It only allows data reception from the server (unidirectional)

2. Events are limited to UTF-8 (no binary data)

![Server Sent Events](sse.PNG?raw=true)

## Headers
Headers are required to keep the connection open. The Content-Type header is set to **'text/event-stream'** and the Connection header is set to **'keep-alive'**. The Cache-Control header is optional, set to **'no-cache'**. Additionally, the HTTP Status is set to 200 - the status code for a successful request.
