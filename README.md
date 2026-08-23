# Arena

**Pet Arena Battles** — Turn-based auto-battler using live pet stats and NFT gear as loadout.

Part of the [ComputerPets](https://github.com/RicheyWorks/computerpets) universe. Map: [computerpets-ecosystem](https://github.com/RicheyWorks/computerpets-ecosystem).

> Status: **design scaffold**. Gameplay contract is frozen. Engine choice is the one in the brief. Implementation comes next.

## Loop

Rui does not leave the desktop to fight. Arena is the coliseum: 210 kinds, mood and stamina from the overlay, gear from Bazaar. A hungry pet underperforms. A well-cared pet hits above its rarity.

## Genre & engine

- Genre: **Auto-battler**
- Engine: **Unity / WebGL**
- Stack: Unity 6 · C# · WebGL export · NFT gear from Minter · stats from flagship vitals
- Default surface: `WebGL / Unity editor`

## How you play

1. Draft 3 pets from your kennel.
2. Gear slots: hat / mark / accessory (legal trait slots only).
3. Auto-resolve rounds; you pick stance (guard, frenzy, trick) between rounds.
4. Winner takes treat-coin via Ledger, never the opponent NFT.

## Talks to

- computerpets (vitals)
- computerpets-minter (gear tokens)
- computerpets-bazaar
- computerpets-ledger
- computerpets-dojo (trained stats)

## Failure doctrine

Disconnect mid-fight → pause + 60s reconnect, then forfeit treats not pets. Illegal hybrid loadout → reject at lock-in. WebGL GPU fail → desktop overlay still walks.

Canon rules that never yield:

- 210 living kinds. No illegal hybrids.
- Overlay pets can get tired, sick, or hide. Tokens are not burned by a minigame.
- Desktop walk stays the main quest. Closing Arena must leave Rui walking.

## Layout

```
computerpets-arena/
  README.md
  LICENSE
  docs/DESIGN.md
  src/                implementation lands here
```

## Run (Windows)

```powershell
Open Arena/ in Unity Hub; File > Build Settings > WebGL. Or npm run preview after export.
```

Meet Rui first via the [flagship start-here](https://github.com/RicheyWorks/computerpets/blob/main/docs/START-HERE.md). This game is optional.

## License

MIT. See [LICENSE](LICENSE).

---

*Two hundred ten living kinds. Keep them so a line does not go quiet.*
