# Gumleaf Dash

> **New:** [`mr-not-fair/`](mr-not-fair/) has *Mr. Not Fair: The Biscuit Tin*, the first episode of a no-reading series for ages 4–7.

A 3D endless runner across Australia. You play a kangaroo (or a quokka or koala, once unlocked) hopping through four stages that loop and keep getting faster:

1. **Red Desert** at golden hour: mesas, spinifex, windmills, hot-air balloons
2. **Misty Ranges**: gum forest, tree ferns, a waterfall and a rainbow
3. **Harbour City** at night: city lights, fireworks, a big wheel, and a run under a suspension bridge
4. **Coral Coast**: beach, palms, dolphins, a lighthouse and a breaching whale

## Play

Open `index.html` in a modern browser. It's a single file with no build step. Three.js r160 loads from jsDelivr.

| Action | Keyboard | Touch |
| --- | --- | --- |
| Change lane | ← → or A D | Swipe left or right |
| Hop (double hop with Super hop) | ↑, W or Space | Tap or swipe up |
| Duck / drop fast | ↓ or S | Swipe down |
| Pause / sound | P / M | Buttons in the bottom-right corner |

## What's in it

- **Three kinds of obstacle**: hop over low ones (logs, rocks, coolers, crocodiles), switch lanes around tall ones, and duck under overhead ones (rock arches, branches, bunting, beach nets).
- **Moving hazards**: charging emus, wombats crossing the track, and magpies that swoop at whichever lane you're in (a red ring on the ground warns you).
- **Koala rescues**: rescued koalas ride on your back, up to three at a time.
- **Power-ups**: the bush hat is a shield, the gumnut magnet pulls in leaves, and Super hop gives high, floaty double jumps.
- **Leaf combo**: collect leaves quickly to raise the multiplier up to x6. Golden leaves are worth 10.
- **Missions and ranks**: three missions are active at a time. Every 3 you complete raises your Ranger rank, which is a permanent score multiplier.
- **Skins**: Grey Roo, Quinn the Quokka, Kip the Koala, Starlight Roo and Golden Roo.

## Built-in money features

- **Gum leaves** are a soft currency (saved in `localStorage`) spent on skins and revives. Selling leaf packs as in-app purchases fits here.
- **Second chance** (free, once per run) is the rewarded-ad slot. `requestFreeRevive()` in `index.html` is the hook: show the ad, then call `revive()` only if it was watched.
- **Leaf revive** costs 75 leaves, doubling each time in a run. It creates demand for leaves.
- **Missions and ranks** give players a reason to come back.

## Names, landmarks and licences

- Every place is generic and fictional. The game has no Uluru, no Opera House, and no named bridge, and no stage is named after a real site.
- There are no brand names: "cooler" rather than a brand of cool box, "bush hat" rather than a hat brand, and the ferries use generic colours.
- A web search for "Gumleaf Dash" turned up no existing game. That is not a trademark clearance, so search the trademark registers (IP Australia, USPTO, EUIPO) before publishing commercially.
- Three.js is MIT-licensed. The Lilita One and Nunito fonts are under the SIL Open Font License. All models, textures, sounds and music are generated in code for this game.
