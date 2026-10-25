# Vendored skills

Third-party skills copied into this repo so they load in every Claude Code session
(local and cloud) for this project. Each folder keeps its original MIT `LICENSE`.

| Folder | Upstream | Commit | Changes |
|---|---|---|---|
| `hook-writing`, `hook-tactics`, `hook-voice-patterns`, `ad-concept-generator`, `ugc-scriptwriter` | [motion-creative/skills](https://github.com/motion-creative/skills) | `5d03170` | None |
| `ugc-editor` | [HiveHubollective/ugc-editor](https://github.com/HiveHubollective/ugc-editor) | `042c0c5` | `scripts/transcribe.py`, `qa.py` and `sort.py` read the speech model from `UGC_WHISPER_MODEL` (default `small.en`, unchanged). `SKILL.md`'s "Updating" section now points here, and a "Non-English footage" section was added. |

`partcraft-ugc` is PartCraft's own skill. It ties these skills to
`docs/ugc-video-playbook.md` and the brand facts.

The editor's `scripts/setup.sh` installs ffmpeg, uv and a Python environment in
`~/.ugc-editor`, and downloads a ~460 MB speech model on first run. Read it before
running it on a new machine.
