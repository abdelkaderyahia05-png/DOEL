# Skills audio (SFX) pour le montage vidéo

Source : Short « Claude est nul en montage vidéo ! » (Henri · ExplorIA) — https://youtube.com/shorts/u5Loma35hjc

| Dossier | Rôle | Origine | Commit | Licence |
|---|---|---|---|---|
| `openverse-sfx/` | Cherche et télécharge des sons/musiques libres sur Openverse (sans clé API), écrit `credits.txt` | https://github.com/Varnan-Tech/opendirectory (`skills/openverse-sfx`) | caac7cd | MIT |
| `earshot/`, `real-sound/` | « Oreilles » de Claude : décrit/évalue un son, en génère un nouveau si rien ne convient | https://github.com/Leonxlnx/earshot (`skills/`) | 7a7f7c5 | MIT |
| `real-sfx/` | Repère les moments du montage et place les sons à l'image près, rend un MP4 + piste SFX | https://github.com/Clipwing/skills (`skills/real-sfx`) | edbefcb | Scripts MIT, sons uisfx CC0 |

## Prérequis

- `ffmpeg` + Python 3.10+
- openverse-sfx : `pip install librosa matplotlib numpy scipy`
- earshot (l'outil, pas inclus ici, ~350 Mo installé) : `pip install "earshot @ git+https://github.com/Leonxlnx/earshot"`
- real-sfx : `python scripts/setup.py init --uisfx` puis `python scripts/setup.py check`

## Prompt d'enchaînement

> Ajoute le sound design à cette vidéo : cherche chaque son sur Openverse (openverse-sfx), vérifie-le / génère-le avec earshot si rien ne convient, place-le à l'image près avec real-sfx, et vérifie la licence de chaque fichier (credits.txt).
