# Express.js: Missing Response in Request Handler

This repository demonstrates a common error in Express.js applications: forgetting to send a response to the client in a request handler.

## Bug

The `bug.js` file contains an Express.js server that logs a message when a request is received but fails to send any response back to the client.  This results in the client receiving a timeout error or hanging indefinitely.

## Solution

The `bugSolution.js` file shows the corrected code, which properly sends a response using `res.send()`.

## How to reproduce

1. Clone this repository.
2. Run `node bug.js`.
3. Try making a request to `http://localhost:3000/` using a tool like `curl` or your browser. Note the lack of response. 
4. Run `node bugSolution.js`.
5. Make another request to the same URL. Observe the response this time.

This example highlights the importance of always sending a response to the client in Express.js request handlers to avoid unexpected behavior.