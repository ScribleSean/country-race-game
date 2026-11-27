# Country Race

A live race for up to six players to name every country in the world, inspired by country quizzes. Everyone types at the same time. Each player has their own color; a country two or more players named takes the color of whoever named it first, with a dark outline, so the map shows at a glance what only you found. A scoreboard shows each player's count, their share of the world and who is ahead, and your own list of countries stays on screen next to the input while you type.

Play: https://scriblesean.github.io/country-race-game/

## How to play

1. Open the page and press **Race a friend**. You get a short game code.
2. Press **Copy link** and send it to up to five other players, or tell them the code to type into **Join**.
3. Each player picks a color (two players can't hold the same one), sets the time limit, and presses **Ready**. The game starts after a 3-second countdown.
4. Type country names. A name counts as soon as it is complete. If it is also the start of a longer name (for example "Niger" and "Nigeria"), it counts after a short pause or when you press Enter.
5. Press **Give up** twice to stop early. The game ends when time runs out or every player still connected is done. On a phone, switch between **Map** and **List** under the input.
6. Countries too small to see on the map (microstates and small islands) have a round marker that fills in like any other country. **Names** and **Markers** on the map turn the country names and those markers on or off; your choice is remembered. Pinch, scroll or use the + and − buttons to zoom.
7. When the round ends you see the winner and a game-flow chart: each player's count over time, who was ahead and by how much, and the final margin. Then comes a review of every country: filter by who found it (all, each player, shared, nobody), by region, or search. Pick a country in the list to see it on the map, or pick it on the map to see it in the list.
8. Press **Rematch** to play again with the same colors; the next round starts when every connected player has pressed it.
9. Press **History** in the lobby to see your past rounds, your record against each named opponent, and the countries others named that you missed most.

You can also play alone: open the page and press **Play solo**.

If a player reloads the page or loses the connection, opening the same link again rejoins the same game.

## How it works

The page is static and runs in the browser. The browsers connect directly with WebRTC through [PeerJS](https://peerjs.com/). PeerJS's public server is used to find the other browsers, and PeerJS's public relay carries the game when the two networks can't connect directly. The host's browser keeps the game state. Your color, your map options, the name you type (optional, shown to the other player), an anonymous player id, your guesses for the current game, and a history of your finished rounds (date, names, colors and scores, and the countries you and others named) are saved in your browser's local storage. History stays in this browser and is not sent to other players. There are no accounts and no analytics.

## Map data

- Country shapes: [Natural Earth](https://www.naturalearthdata.com/) (public domain), via [world-atlas](https://github.com/topojson/world-atlas) (ISC license).
- Drawing: [D3](https://d3js.org/) and [topojson-client](https://github.com/topojson/topojson-client).

## License

MIT. See [LICENSE](LICENSE).
