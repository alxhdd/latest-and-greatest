# 📡 Latest & Greatest (Portfolio Auto-Updater)

> *Because manually updating a personal website is a crime against automation.*

This repository acts as the automated brain and single source of truth for my live developer portfolio. I got tired of manually editing my website every time I shipped code, so I built a system to track my active hyperfocus and update my site for me. 

### ⚙️ The Architecture
Instead of static updates, this repo is driven by a custom GitHub Action workflow:
1. **The Tracker:** My active projects contain a `portf.json` config file.
2. **The Scanner:** A scheduled GitHub Action scans all my repositories hunting for that file. If the project is flagged as active (no skip), it calculates the latest commit data.
3. **The Aggregator:** The script isolates the absolute newest commit across all active projects and dumps the data into `latest.json` right here.
4. **The Deployment:** My portfolio frontend triggers a daily build, fetches this updated JSON, and dynamically renders my "Currently Working On" section.

---

### 🚀 Live Project Feed

**Project:** [The Portfolio That Maintains Itself](https://alxhdd.com)

Static site. Zero manual updates. Fully automated from repo to deployment.

_Last updated: 2026-06-09_
