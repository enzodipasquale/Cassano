# Cassano Penalty Player

## Strategy
Cassano trusts instinct and blasts the ball in a **random direction** every time:
- Chooses between `0` (left), `1` (centre), or `2` (right)
- Does not look at previous rounds or opponents

## How to Run Locally
```bash
python strategy.py
```

Set these environment variables first:
- `SERVER_URL` – game platform endpoint
- `GITHUB_TOKEN` – personal access token (optional locally, required in CI)

## GitHub Actions
This repo ships with two workflows in `.github/workflows/`:
- `register.yml` registers the player on push
- `penalty-shootout-manual.yml` lets you trigger a manual game

Add your secrets (`GAME_TOKEN`, `SERVER_URL`, `GITHUB_TOKEN`) in the repo settings before enabling the workflows.

