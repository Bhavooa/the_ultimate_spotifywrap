# The Ultimate Spotify Wrap

A lifetime analysis of Spotify listening history across multiple people, with per-person "wraps" and a side-by-side comparison.

## Architecture

```
Spotify exports (JSON) -> DuckDB (one `plays` table, `person` column)
  -> SQL/pandas feature queries -> aggregated JSON -> React app (Firebase Hosting)
```

- `analysis/`: Python + SQL ingest, features, export
- `web/`: React front end (later)
- `data/raw/<person>/`: raw exports, never committed

_Work in progress._
