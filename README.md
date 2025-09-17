# DDOS-attack-map
I'm Planning to build an DDOS attack map site which will help people visualize and see how the DDOS attacks are occuring aroud the globe for the purpose to build this project I'll following this 

I'm trying to build a live DDOS attack map I mostly know how to build it but don't know how to do it. abundance of knowledge i guess

Periodically fetch traffic trends and attack spikes from Cloudflare (but how? )
fetch IP's from abuseIPDB ( but how? )
classify IP's with his DDOS confidence score with machine learning (but how? )
remote IP's to coordinates(i guess that's doable)
and show case them using the Github globe ( that's doable too)

and use fastAPI for backend (but how? )

I"ll be really happy if you could help me out as I'm a beginner 2nd year student I"m looking forward to learn these things.

# commit by commit goals: 

Repo & README — init git, create README with goals & milestones.

FastAPI skeleton — make /health and /status endpoints.

DB schema (draft) — create migrations or a SQL file with tables:

raw_events (id, timestamp, source, payload JSON)

ip_records (ip, first_seen, last_seen, asn, country, geo JSON)

ddos_events (id, start_ts, end_ts, affected_ips JSON)

ml_scores (ip, timestamp, score, model_version, features JSON)

Cloudflare fetcher (mock) — write a function that reads a sample JSON (simulate Cloudflare) and inserts to raw_events.

AbuseIPDB fetcher (mock) — same: import static IP list to a table and mark abuse_score field.

Write a small enrichment script — takes an IP, does geo lookup (offline local DB or free API) and stores coords.

Basic correlation script — simple join: if IP in abuse list and seen in Cloudflare spike → flag.

Simple ML prototype — train on existing features (abuse_count, packets, bytes, port_count, geo_presence) and output a score; evaluate with simple metrics.

Expose endpoint /hotspots — returns top N IPs with coordinates and score.

Frontend stub — minimal globe that queries /hotspots and renders points.

# Goals for building the project weekly

Week 1: repo, FastAPI skeleton, DB (tables), mock ingestion pipeline.
Week 2: implement real AbuseIPDB fetch + enrichment (geo), store ip_records.
Week 3: Cloudflare fetcher (or simulated), correlation script, endpoint /hotspots.
Week 4: ML prototype + training script + save model; ML endpoint to score IPs.
Week 5: Frontend globe + consume /hotspots; polish visualization.
Week 6: Dockerize, add scheduler, basic auth, operator feedback loop, deploy to a cheap VM/test.

that's all for now 

peace out
