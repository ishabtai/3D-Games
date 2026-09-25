# Roo Rescue

A 3D endless-runner across Australia. You play a kangaroo hopping through four stages:

1. **Uluru Outback**: red dirt, termite mounds, Uluru and Kata Tjuta on the horizon
2. **Blue Mountains**: gum forest and the Three Sisters
3. **Sydney Harbour**: sailboats, green-and-gold ferries, the Opera House, and a run under the Harbour Bridge
4. **Reef Coast**: beaches, palms, surfboards, a lighthouse and reef bommies

Rescue koalas sitting on the track, collect gum leaves, hop over logs, rocks and eskies, and dodge the tall stuff. After Reef Coast the stages loop and the game keeps getting faster.

## Play

Open `index.html` in any modern browser. It's one file with no build step. Three.js loads from cdnjs.

| Action | Keyboard | Touch |
| --- | --- | --- |
| Change lane | ← → or A D | Swipe left or right |
| Hop | ↑, W or Space | Tap or swipe up |
| Drop fast | ↓ or S | Swipe down |
| Pause / sound | P / M | Buttons in the bottom-right corner |

## Built-in money features

- **Gum leaves** are a soft currency, saved in the browser (`localStorage`).
- **Skins shop**: Grey Roo (150), Kip the Koala (400), Golden Roo (1200). This is where in-app purchases or leaf packs would plug in.
- **Second chance**: one revive per run. `requestRevive()` in `index.html` is the hook for a rewarded video ad. Call `revive()` only after the ad reports it was watched.
- **Akubra hat power-up**: absorbs one hit.

## Ways to earn from it

- **Web game portals** (CrazyGames, Poki, GameDistribution): upload the HTML5 build and integrate their SDK for ads (rewarded video for the revive, midroll between runs). They share ad revenue with you. Each portal has its own review and SDK requirements.
- **itch.io**: free with pay-what-you-want, or paid.
- **Mobile app**: wrap it with Capacitor or Cordova, add AdMob rewarded ads and in-app purchases for leaf packs and skins, then publish to Google Play and the App Store.

Before selling it commercially, check trademark rules on landmark names and images (the Sydney Opera House, for example, is a registered trademark), and change names or designs where needed.
