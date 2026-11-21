# Country Race

A live two-player race to name every country in the world, inspired by country quizzes. Both players type at the same time. Each player has their own strong color, and a country both players named gets a separate shared color, so the map always shows who has what. A scoreboard shows each player's count, their share of the world and who is ahead, and your own list of countries stays on screen next to the input while you type.

Play: https://scriblesean.github.io/country-race-game/

## How to play

1. Open the page and press **Race a friend**. You get a short game code.
2. Press **Copy link** and send it to the other player, or tell them the code to type into **Join**.
3. Each player picks a color (two players can't hold the same one), sets the time limit, and presses **Ready**. The game starts after a 3-second countdown.
4. Type country names. A name counts as soon as it is complete. If it is also the start of a longer name (for example "Niger" and "Nigeria"), it counts after a short pause or when you press Enter.
5. Press **Give up** twice to stop early. The game ends when time runs out or both players are done.
6. Countries too small to see on the map (microstates and small islands) have a round marker that fills in like any other country. **Names** and **Markers** on the map turn the country names and those markers on or off; your choice is remembered. Pinch, scroll or use the + and − buttons to zoom.
7. When the round ends you see the winner, then a review of every country: filter by who found it (all, mine, theirs, both, nobody), by region, or search. Pick a country in the list to see it on the map, or pick it on the map to see it in the list.
8. Press **Rematch** to play again with the same colors; the next round starts when both players have pressed it.

You can also play alone: open the page and press **Play solo**.

If a player reloads the page or loses the connection, opening the same link again rejoins the same game.

## How it works

The page is static and runs in the browser. The two browsers connect directly with WebRTC through [PeerJS](https://peerjs.com/). PeerJS's public server is used to find the other browser, and PeerJS's public relay carries the game when the two networks can't connect directly. The host's browser keeps the game state. Your color, your map options, the name you type (optional, shown to the other player), an anonymous player id, and your guesses for the current game are saved in your browser's local storage. There are no accounts and no analytics.

## Map data

- Country shapes: [Natural Earth](https://www.naturalearthdata.com/) (public domain), via [world-atlas](https://github.com/topojson/world-atlas) (ISC license).
- Drawing: [D3](https://d3js.org/) and [topojson-client](https://github.com/topojson/topojson-client).

## License

MIT. See [LICENSE](LICENSE).
