# DOEL — consignes pour Claude

## Montage vidéo : son et effets sonores (SFX)

Dès qu'une vidéo est montée, retouchée ou générée dans ce projet, s'occuper aussi du son **sans attendre que l'utilisateur le demande** : il ne le redira pas à chaque nouvelle vidéo. Les skills sont dans `.claude/skills/` (origine et licences : `.claude/skills/SOURCES.md`) :

1. **openverse-sfx** : chercher et télécharger les sons et musiques libres sur Openverse, puis tenir `credits.txt` à jour.
2. **earshot** / **real-sound** : écouter et juger les sons (Claude n'entend pas), et générer un son quand rien ne convient.
3. **real-sfx** : repérer les moments qui ont besoin d'un son (whoosh, pop, clic…) et les placer à l'image près.

Enchaînement par défaut : chercher chaque son avec openverse-sfx, le vérifier ou le générer avec earshot, le placer avec real-sfx, et vérifier la licence de chaque fichier.

Les utiliser seulement quand c'est utile (vidéo avec image ou montage), pas pour une tâche sans rapport avec la vidéo.

Prérequis à installer au besoin dans la session : `ffmpeg`, `pip install librosa matplotlib numpy scipy`, `pip install "earshot @ git+https://github.com/Leonxlnx/earshot"`, et pour real-sfx `python scripts/setup.py init --uisfx` depuis son dossier.
