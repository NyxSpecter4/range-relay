# 1800s skin — bind, do not rebuild

Same mesh: `worlds/drone-london-recon`.
Loader already named in ART_MANIFEST: `sgrok-texture-upgrade.js` → `authFacade` / `buildingMatBrick` / rooftops / water.
Epochs already exist: `data/london-epochs.js` (1586 / 1943 / modern).

## What Tudor vs Victorian actually is
- **Tudor / Elizabethan (c. 1586):** timber frame + lime nogging. File on London: `art/tex-facade-tudor.png`. Disk twin: `facade_elizabethan_tudor_timber_seamless.png`.
- **Victorian (c. 1840–1901) — the letterbox century:** stock brick + sash. File: `art/tex-facade-victorian.png`.
- **Do not** paint the whole city Tudor. 1800s London is Victorian brick, slate, cobble, gas. Tudor is a *district* (City / Southwark pockets), not the default wall.

## Slot → file (1800s pack)
| Mesh / material | File already on London |
|---|---|
| buildingMatBrick / authFacade majority | tex-facade-victorian.png |
| timber pockets only | tex-facade-tudor.png |
| roofs | tex-rooftop-slate.png |
| walk | tex-sidewalk-slate.png or textures/tex-cobble-or-ground.png |
| rails | tex-iron-railing.png |
| water | tex-thames-water.png |
| sky night | sky-london-night.png |
| lamp prop | props/prop-street-lamp.png |

**Off for this skin:** tex-facade-glass-*, tex-facade-corten, tex-chinatown-*, tex-neon-strip, SF glass fallbacks.

## Bind process (Corvus, one PR)
1. URL flag `?era=victorian` (RANGE RELAY Saturday) or epoch switch already in `london-epochs.js`.
2. texture-upgrade: if era=victorian, assign the table above; leave geometry.
3. Repeat wrap 1–2 on facades (1024² seamless). Asphalt road tile is 687×1024 — do not use as facade.
4. Hide modern props (K6 can stay as an anachronism joke; black cab off).
5. Fog + cooler key. No new raycaster.
6. Prove one block in the browser, then flip the city.

SGROK does not edit index.html’s 10k-line inline. This file is the bind list.
