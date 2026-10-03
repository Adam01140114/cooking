# Short Order

A 3D diner cooking game built with [three.js](https://threejs.org/). Run the line through a three-minute lunch rush, cooking either **burgers** or **pizza**, and earn the biggest till.

## Modes

- **Solo**: one cook, one shift. Your best score is saved in the browser.
- **Couch versus**: the game plays on one screen (hook it up to a TV). Each player scans a QR code with their phone, and the phone becomes that cook's station pad.
- **Online versus**: send a link, and your rival plays their own kitchen from another computer. Both kitchens get the same ticket sequence, and the higher till wins.

## How to play

1. Read the tickets on the rail. The bar under each ticket is the customer's patience.
2. Grab food from the crates. Chop or roll it on a board. Grill patties or bake pizzas, and pull them before they burn.
3. Build the order on a plate or tray and serve it at the pass. Fast service earns bigger tips.

## Running it

Open `index.html` in a browser. Solo mode works anywhere.

The versus modes use the Claude artifact `room` capability for real-time multiplayer, so they only work in the hosted version on claude.ai, and every player has to be signed in with access to the artifact.
