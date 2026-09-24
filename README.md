# fblog – Firebase & Google Cloud Log Viewer

A fast, lightweight CLI log viewer, stream filter, and metrics aggregator for Firebase / Google Cloud Run / Cloud Functions JSON log exports.

---

## ✨ Features

- **Local Timezone Conversion**: Automatically converts UTC ISO timestamps (`2026-09-23T18:33:07Z`) to your machine's local time (including milliseconds and DST adjustments).
- **Colorized Output**: Highlights HTTP methods, response status codes, latencies, and log severities (`ERROR`, `WARNING`, `INFO`).
- **Dynamic Metrics Summary (`--sum`)**: Automatically parses, calculates totals, counts, and averages for any custom numeric label in your logs (e.g., Firestore Reads, DB operations, Execution times).
- **Dynamic Field Filtering**: Use kebab-case CLI flags matching JSON keys (e.g. `--text-payload`, `--execution-id`, `--request-url`, `--status`).
- **Case-Insensitive Substring Search**: Match partial strings without worrying about exact casing or special regex characters (`/`, `[]`, `.`).
- **Section Streaming (`--until`)**: Stream logs from a matching entry until an end delimiter (e.g., `---`) is encountered.
- **Context Fetching (`-n`)**: Capture the matching log plus the next **N** log entries.
- **Dynamic Help**: Run `-h` on your log file to list all available filter flags present in that specific export.

---

## 📦 Requirements

- `bash` (4.0+)
- `jq`

On Arch Linux:
```bash
sudo pacman -S jq
