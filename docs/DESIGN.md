# Arena design

Implement against this file, not folklore.

## Identity

- Product: **Arena**
- Repo: `computerpets-arena`
- Idea: Pet Arena Battles
- Genre: Auto-battler
- Engine: Unity / WebGL
- Surface: `WebGL / Unity editor`

## Loop

Rui does not leave the desktop to fight. Arena is the coliseum: 210 kinds, mood and stamina from the overlay, gear from Bazaar. A hungry pet underperforms. A well-cared pet hits above its rarity.

## Play beats

- Draft 3 pets from your kennel.
- Gear slots: hat / mark / accessory (legal trait slots only).
- Auto-resolve rounds; you pick stance (guard, frenzy, trick) between rounds.
- Winner takes treat-coin via Ledger, never the opponent NFT.

## Neighbors

- computerpets (vitals)
- computerpets-minter (gear tokens)
- computerpets-bazaar
- computerpets-ledger
- computerpets-dojo (trained stats)

## Failure doctrine

Disconnect mid-fight → pause + 60s reconnect, then forfeit treats not pets. Illegal hybrid loadout → reject at lock-in. WebGL GPU fail → desktop overlay still walks.

## Hard rules

1. Minigames cannot mint or burn NFTs by themselves (Minter is the write path).
2. Stats come from lived overlay care + Dojo caps, not cash shop.
3. Species kits stay inside Lore. Illegal hybrids never spawn.
4. Fail soft: the desktop overlay process is not this process.
