# Blast Battles — Audio Setup

## Folder Structure

Create a `music/` folder in the repo root and add the following files:

```
BlastBattle/
├── Blast_Battles_V1.2.6.html
├── music/
│   ├── hero_select.mp3          ← Character select screen theme
│   ├── gameplay_1.mp3           ← Gameplay pool track 1
│   ├── gameplay_2.mp3           ← Gameplay pool track 2
│   ├── gameplay_3.mp3           ← Gameplay pool track 3
│   ├── sfx_hero_zone.wav        ← Hero zone entry sound effect
│   └── sfx_villain_zone.wav     ← Villain zone entry sound effect
└── README.md
```

## Rename Files Before Committing

| Original filename | Rename to |
|---|---|
| `Hero_Theme_-_MK2.mp3` | `hero_select.mp3` |
| `Thor_s_Hammer_-_Ethan_Meixsell.mp3` | `gameplay_1.mp3` |
| `Actin_Up_-_MK2.mp3` | `gameplay_2.mp3` |
| *(phonk track)* | `gameplay_3.mp3` |
| `467315__kaunaj__enterhero.wav` | `sfx_hero_zone.wav` |
| `569047__humanoide9000__evil-villian-theme.wav` | `sfx_villain_zone.wav` |

## Audio Behaviour

| Trigger | Audio |
|---|---|
| First click on page | Select screen music begins |
| Character select screen | `hero_select.mp3` loops |
| Game starts | Random track from gameplay pool crossfades in |
| Gameplay track ends | Next random track starts automatically |
| Player lands on Hero Sanctum / Light Room | `sfx_hero_zone.wav` plays, BGM ducks to 20% |
| Player lands on Villain Den / Dark Alley | `sfx_villain_zone.wav` plays, BGM ducks to 20% |
| Play Again | Crossfades back to select screen music |
| 🔊 button (header) | Toggles mute on/off |

## Adding More Gameplay Tracks

Edit the `BB_Audio` script block in the HTML:

```javascript
// Add to TRACKS object:
gameplay_4: { src: './music/gameplay_4.mp3', loop: true },

// Add to GAMEPLAY_POOL array:
const GAMEPLAY_POOL = ['gameplay_1', 'gameplay_2', 'gameplay_3', 'gameplay_4'];
```

---

## Music Attribution

### NoCopyrightSounds (NCS) — Free to use with credit

**"Hero Theme" by MK2**
Music provided by NoCopyrightSounds.
Free Download / Stream: https://ncs.io/HeroTheme
Artist: https://soundcloud.com/mk2official

**"Actin Up" by MK2**
Music provided by NoCopyrightSounds.
Free Download / Stream: https://ncs.io/ActinUp
Artist: https://soundcloud.com/mk2official

### YouTube Audio Library — Free to use

**"Thor's Hammer" by Ethan Meixsell**
Source: YouTube Audio Library
https://www.youtube.com/audiolibrary

### Freesound.org — CC0 (Public Domain)

**"enterhero" by kaunaj**
https://freesound.org/s/467315/ — License: CC0 1.0

**"evil villain theme" by humanoide9000**
https://freesound.org/s/569047/ — License: CC0 1.0

**Phonk instrumental by kontraamusic**
https://freesound.org/s/798796/ — License: CC0 1.0
