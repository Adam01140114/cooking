# Short Order

A 3D diner cooking game built with [three.js](https://threejs.org/). Run the line through a three-minute lunch rush, cooking either **burgers** or **pizza**, and earn the biggest till.

## Modes

- **Solo**: one cook, one shift. Your best score is saved in the browser.
- **Couch versus**: the game plays on one screen (hook it up to a TV). Each player scans a QR code with their phone, and the phone becomes that cook's station pad, connected straight to the TV over your Wi-Fi.
- **Online versus**: send a link, and your rival plays their own kitchen from another computer, through the game server. Both kitchens get the same ticket sequence, and the higher till wins.

## How to play

1. Read the tickets on the rail. The bar under each ticket is the customer's patience.
2. Grab food from the crates. Chop or roll it on a board. Grill patties or bake pizzas, and pull them before they burn.
3. Build the order on a plate or tray and serve it at the pass. Fast service earns bigger tips.

## Running it

```
npm install
npm start
```

Then open http://localhost:6969. `server.js` serves the game and runs its
multiplayer rooms (Node, Express and socket.io).

- **Couch versus**: open the game on the computer hooked up to the TV and pick
  Couch versus. Both players scan the code. When the game is opened on
  localhost, the code uses the computer's Wi-Fi address so phones can reach it.
  Each phone then opens a direct WebRTC link to the TV over your own Wi-Fi, so
  pad taps don't make a round trip to a server; the pad's Link box shows
  "⚡ Direct". If that link can't open, taps go through the server instead.
- **Online versus**: send the link. Online matches run through the server, so
  for play over the internet host it somewhere public, such as Render.
- **Solo** needs no server; opening `index.html` directly still works.

The game still runs as a Claude artifact too: there, the versus modes use the
artifact's `room` capability instead of `server.js`.

## Hosting on Render

`render.yaml` describes the service. In the Render dashboard choose
New > Blueprint and pick this repository; Render installs it, runs
`node server.js`, and redeploys on every push to `main`. Anyone can then open
the game at its onrender.com address and play couch or online versus.
