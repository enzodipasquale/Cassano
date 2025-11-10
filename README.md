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

## Registering the Player
```bash
export SERVER_URL="https://ubx-dev-914970891924.us-central1.run.app"
export GITHUB_TOKEN="ghp_example123"
PLAYER_NAME="cassano"
curl -sS -X POST "$SERVER_URL/register" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer $GITHUB_TOKEN" \
  -d "{\"player_name\":\"${PLAYER_NAME}\"}"
```

## GitHub Actions
`.github/workflows/schedule_strategy.yml` submits actions on a 5‑minute cadence (you can also trigger it manually). Add the secrets `GAME_TOKEN` and `SERVER_URL` before enabling it.

