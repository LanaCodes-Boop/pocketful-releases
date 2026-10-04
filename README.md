# Pocketful

A cozy party board game with small wooden travelers. Keezen is its first game: play it solo against
bots, or online with friends and a room code.

## Get the game

1. Download **Pocketlauncher** from the [latest release](https://github.com/LanaCodes-Boop/pocketful-releases/releases/latest):
   - **Windows:** [`Pocketlauncher-Windows.zip`](https://github.com/LanaCodes-Boop/pocketful-releases/releases/latest/download/Pocketlauncher-Windows.zip)
   - **macOS:** [`Pocketlauncher-macOS.zip`](https://github.com/LanaCodes-Boop/pocketful-releases/releases/latest/download/Pocketlauncher-macOS.zip)
2. Unzip it and start Pocketlauncher.
3. Press **Install**, then **Play**. Every time it starts, the launcher looks for a new version and
   offers to update. Your settings and saved matches are kept.

The builds are not code-signed yet:

- Windows shows "Windows protected your PC". Choose *More info*, then *Run anyway*.
- On macOS, right-click Pocketlauncher and choose *Open* the first time.

## Play with friends

In the game choose **Play with friends**, then **Create a room** and share the five-character code,
or type the code a friend gave you. The room server rests when nobody is playing, so the first
connection can take up to a minute.

If your connection drops, your seat is kept: start the game again and choose **Rejoin**.

While you wait, everyone stands together on the lawn by the tea pavilion. Say hello with the emote
buttons in the corner (or the keys Z X C V B N M and comma); they work during the match too. After
the match everyone lines up for a group photo with the titles they earned, and you can save it.

A match opens with a short scene (any click or key skips it), captures play in slow motion and the
winning move gets a finale. Prefer a quicker table? Set **Film moments** to Short or Off under
Settings. The room also keeps the evening's score: crowns by your name for every match you won.

## What is in this repository

| | |
|---|---|
| [Releases](https://github.com/LanaCodes-Boop/pocketful-releases/releases) | Pocketlauncher, the game packages it installs, and the signed update manifest |
| `server/` | The room server as it is deployed: a Dockerfile and the compiled server pack |

How updates stay trustworthy: the launcher only accepts an update manifest that carries the
signature of the Pocketful release key, and it installs only the files that manifest lists, each
checked against its size and SHA-256. A new version is unpacked next to the old one and switched to
only when every file is right; the previous version stays on disk so you can go back.
