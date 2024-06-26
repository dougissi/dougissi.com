![Wordle Replay + React + MUI](/assets/wordlereplay/wordlereplay_react_mui.png)

## Motivation:
In early 2022, I created the original version of WordleReplay.com as my _first_ web development project. I built it using [JQuery](https://jquery.com/) and [Bootstrap](https://getbootstrap.com/). For details on the original version, see my [previous blog post](/wordlereplay-original). Even though it was rough, by 2024 it was getting about 2,000+ daily active users and had seen 8.3 million guesses entered, which far exceeded what I could have ever imagined for the site.

Between 2022 and 2024, I had learned _a lot_ more web development, so I figured I owed it to those many Wordle Replay users to improve the site, and that's what I did. This updated version provides many new features and is written using [React](https://react.dev/) and [Material UI](https://mui.com/).

To play the latest version of the game, see [WordleReplay.com](https://wordlereplay.com). If you're also familiar with React web development, checkout the [wordle-replay-react](https://github.com/dougissi/wordle-replay-react) GitHub repository to contribute to the site.

All feedback is welcome.

## New Features

### User-Facing
* A much improved UI that scales better to different screen sizes
* Guesses are saved automatically, allowing users to return to previously unfinished puzzles without having to start all over
* Calendar view of which puzzles are solved, unfinished, or still to-do
* Hard Mode
* Color Blind mode
* View, filter, and delete history for all puzzles or each puzzle individually
* News blog that announces new updates/features in a single location


### Implementation Details
* Uses React and Material UI
  * better state management compared to JQuery
  * More consistent styling with Material UI compared to Bootstrap
  * Uses react-router-dom Link within Material UI Link (since react-router-dom Link is faster for inter-site linking)
* Unit tests: the previous version had no unit tests, and this version has extensive unit tests, which greatly reduces the likelihood of unexpected/incorrect behavior.
* Deployed to GitHub Pages via /docs folder on main branch instead of leveraging [gh-pages](https://www.npmjs.com/package/gh-pages) package.
* Uses IndexedDB instead of localStorage for saving guesses
* CNAME needed to be "wordlereplay.com" vs "www.wordlereplay.com" for history to carry over

## Competition: NYT Wordle Archive

In surprising timing, The _New York Times_ launched their own <a href="https://wordlearchive.com" target="_blank">Wordle Archive</a> in May 2024, just before I launched my new version. I'm both happy and sad to report that it's so full of full of advertisements that it's nearly unusable. It also used _a ton_ of memory, literally 1.3 GB, which is enough that could slow a user's whole computer down. Perhaps they'll improve it in the future.

Maybe they'll even glean some inspiration from WordleReplay.com?
