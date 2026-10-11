# Tatami Duel

Judo as an installable web app (PWA). Take a grip, pull and push to break your opponent's balance (kuzushi), then throw. If the throw doesn't finish it, the fight goes to the ground, where you can pin. A referee calls every throw, score and penalty in Japanese with the IJF hand signals.

**Play:** https://matdata-eu.github.io/game-judo-duel/

## Modes
- **Bot**: you (white, left) against a bot (blue, right) on Easy, Medium or Hard. Harder bots react faster, block and counter more often, fight harder for the grip and wait for real kuzushi before they throw.
- **2 Players**: two people on one device. Keyboard: White `A D` step, `W` grip, `S` throw, `E` sweep, `Q` superpower. Blue `← →` step, `↑` grip, `↓` throw, `/` or right `Shift` sweep, `.` or `Enter` superpower. Against the bot, the arrows, `Space` (sweep) and `F` (superpower) work for you too. On a touchscreen each player gets buttons on their side.
- **Belts**: pick a belt for each judoka, from white to black, or the red and white belt of 6th to 8th dan. It's for looks only.
- **Contest**: 2, 3 or 4 minutes (4 is the official senior time). If the score is level at the bell, golden score follows: no time limit, the first score wins.

## Moves
| Control | Technique | Works when |
|---|---|---|
| Grip | Take a grip on the gi; press again to break the opponent's grip | you are within reach |
| Throw while stepping back (pulling) | Seoi-nage, shoulder throw | the opponent is pulled forward |
| Throw standing still | Uchi-mata, inner thigh throw | the opponent is pulled forward |
| Throw while stepping in (pushing) | O-soto-gari, major outer reap | the opponent is pushed backward |
| Sweep | De-ashi-barai, advanced foot sweep | the opponent has just started a step |
| Throw while the opponent turns in | Counter: Ura-nage, O-soto-gaeshi or Tsubame-gaeshi | you are balanced and have a grip |

Who owns the grip matters as much as the balance: a throw against an opponent with a full grip of their own often fails or scores nothing. Defend by stepping away from the throw's direction (sitting back against a forward throw, leaning in against the reap), or counter it.

On the ground, press Grip or Throw to pin (osaekomi). The one underneath escapes by pressing any button fast; the one on top presses to hold on.

## Scoring and the referee
- **Ippon** ends the contest: a clean throw with force and control, a 20-second hold, or two waza-ari (waza-ari awasete ippon).
- **Waza-ari**: a throw that lands well but not perfectly, or a 10-second hold.
- **Shido** (penalty): stepping out of the contest area, forcing the opponent out, or not attacking for 25 seconds. Shido don't decide the contest; a third shido is hansoku-make and loses it.
- The referee calls Rei, Hajime, Matte, the technique, Waza-ari, Ippon, Osaekomi, Toketa, Shido, Hansoku-make and Sore-made, and shows the signals: arm straight up for ippon, sideways for waza-ari, pointing down over the pair for osaekomi, waving for toketa, a finger for shido, a raised hand for matte.

## Superpowers
Each judoka can pick a tongue-in-cheek national superpower (or none): one use in a 2 or 3 minute contest, two in a 4 minute one. Press `Q` (White) or `.` (Blue), or the ★ button.

| Nation | Superpower | When | What happens |
|---|---|---|---|
| Belgium | Belgian compromise | a score goes against you | After long negotiations it's level: one waza-ari each. |
| Italy | Protesta! | a score or shido goes against you | You protest at length. Half the time the referee cancels the call (torikeshi); otherwise you get a shido. |
| Japan | Textbook ippon | during the contest | For 8 seconds every throw that scores is ippon, and it can't be countered. |
| Georgia | Bear hug | during the contest | For 7 seconds your grip can't be broken and every pull and push counts double. |
| Brazil | Jiu-jitsu | during the contest | The next ground fight is yours: an instant pin nobody can escape for 10 seconds, or, if you're underneath, you slip straight out. |
| Great Britain | Tea time | during the contest | Your opponent politely accepts a cup of tea, lets go of the grip and stops for a moment. |

The bot uses its superpower too.

## Install
Open the game in Chrome, Edge or Safari and choose "Install" or "Add to Home Screen". After the first load it works offline.

## Run locally
No build step. Serve the folder over `localhost` or HTTPS, for example:

```sh
python3 -m http.server 8000
```

Files: `index.html` (the whole game), `manifest.webmanifest`, `sw.js` (offline cache), `icons/`. Pushes to `main` deploy to GitHub Pages through `.github/workflows/pages.yml`.

## Support
Found a bug or have an idea? [Open an issue](https://github.com/Matdata-eu/game-judo-duel/issues).

## Credits
- Game, graphics and sound effects: made from scratch in code (canvas drawing, Web Audio), no third-party assets. The referee's voice uses your browser's built-in Japanese speech when available, and reads the calls in romaji otherwise.
- Fonts: [Bungee](https://fonts.google.com/specimen/Bungee) by David Jonathan Ross and [Barlow Condensed](https://fonts.google.com/specimen/Barlow+Condensed) by Jeremy Tribby, both under the SIL Open Font License, loaded from Google Fonts.
- Rules follow the IJF refereeing rules in simplified form (for example, the passivity time is shortened).
- Built by [Matdata](https://matdata.eu) with [Claude Code](https://claude.com/claude-code).

## License
[MIT](LICENSE)
