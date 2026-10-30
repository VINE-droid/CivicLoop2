# CivicLoop

Small, local-first civic report demo. Start with `npm install && npm start`, then open http://localhost:3000.

## Architecture
Express serves `/public` and JSON endpoints. `data/db.json` stores reports and histories; missing data is seeded automatically. Multer stores optional uploaded photos under `public/uploads`. The browser uses plain HTML/CSS/JS and Leaflet with OpenStreetMap tiles.

## Pipeline
On submission, the server assigns a category from keyword matches, takes the first sentence as a summary, compares token counts using cosine similarity, links nearby same-category likely duplicates, and computes a transparent 0–100 factor score. Scores are recomputed on reads. No LLM or embeddings are used.

Demo reset is on the Official Dashboard. Synthetic ward location is centered near Bengaluru coordinates.
