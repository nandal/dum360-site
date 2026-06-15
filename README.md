<div align="center">

# 🇮🇳 DUM360 — Distributed Unified Mesh 360

### India's first decentralized, citizen-powered, sovereign edge supercomputer

**Pool the nation's idle compute — phones, gaming PCs, university & PSU labs, enterprise & MSME machines, and solar/tidal-powered rigs — into one secure, sovereign mesh.**

[🌐 Live site](https://nandal.github.io/dum360-site/) · [✍️ Join the mesh](https://forms.gle/a2JxYZAZu1otR1gm7) · [🤝 Contribute](#-contributing)

![Made in India](https://img.shields.io/badge/Made%20in-India%20🇮🇳-FF9933)
![Status](https://img.shields.io/badge/status-concept%20%2F%20early-blue)
![Hosting](https://img.shields.io/badge/data-100%25%20India--hosted-138808)
![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen)

</div>

---

## 🪔 What is DUM360?

**DUM360 (Distributed Unified Mesh 360)** is a proposed national infrastructure platform that aggregates the **unused, idle computing capacity already sitting across India** — and turns it into a massive, secure, sovereign cloud.

Its founding thesis is simple:

> **At any given moment, the vast majority of the nation's computing power sits idle** — phones at night, gaming PCs after hours, university and PSU labs over evenings/weekends/vacations, enterprise & MSME workstations outside business hours, and surplus daytime solar. DUM360 treats *every powered-on, under-utilized processor in India as latent national infrastructure.*

This repository hosts the **public landing page** for the project (a single, dependency-free `index.html`). The detailed Product Requirement Document (PRD) is maintained privately.

---

## 🎯 Dual-use mandate

| Mode | What it does |
| --- | --- |
| 🟢 **Peace-time** | Hyper-affordable AI training, LLM inference and rendering for Indian startups, researchers and academics — paying everyday contributors directly via **UPI**, and institutions via credits/grants. |
| 🔴 **Rashtra Seva (Emergency)** | A cryptographically-authenticated government trigger instantly remobilizes the entire national compute pool for public-good crises — disaster/climate modeling, bio-defense sequencing, cryptographic & cyber defense. |

---

## 🧩 The compute supply tiers

DUM360 ingests idle capacity from **every layer** of the national compute stack:

| Tier | Examples | Interconnect | Best-fit workloads |
| --- | --- | --- | --- |
| 🎓 **Institutional labs** | IITs, NITs, IIITs, central/state universities | LAN + **NKN** backbone | In-cluster & cross-campus model parallelism; HPC jobs |
| 🏛️ **Government / PSU** | Public-sector R&D labs, ministry data centres | Wired / sovereign | High-trust, sovereign & emergency workloads |
| 🏢 **Enterprise / MSME** | Company servers, startup & MSME workstations | Business broadband | Off-hours batch inference, rendering, ETL |
| ☀️🌊 **Renewable-powered rigs** | Solar grids (GJ/RJ); emerging seawater-cooled tidal/wave/offshore-solar rigs | Wired / subsea | Daytime solar + 24×7 tidal green baseload; big-model sharding |
| 📱 **Consumer devices** | Gaming PCs, desktops, phones | Consumer broadband | Burst, request-parallel inference, light tasks |

**Design principle:** use the *country-wide* mesh for **request-level parallelism (throughput)**, and confine **model-level parallelism** to LAN/NKN-connected clusters where the interconnect can sustain it.

---

## 🧠 AI inference architecture

DUM360 matches **model size to interconnect quality** rather than naively splitting one model across the public internet:

1. **Request-parallel (default)** — models that fit on one node (7B–34B quantized) are replicated; whole requests route to whole nodes → scales to millions of concurrent inferences nationwide.
2. **In-cluster sharding** — large models (70B–400B+) are split *only* inside well-connected clusters (campus lab, GPU rig, PSU data centre).
3. **NKN cross-campus** — the biggest models pipeline across institutions over the National Knowledge Network — a loosely-coupled academic grid.
4. **Speculative decoding** — small models draft tokens, big cluster-hosted models verify.

> Targeted at **massively-parallel, latency-tolerant** workloads (batch inference, rendering, sequencing, Monte-Carlo, cryptanalysis). *Precedent:* Folding@home reached ~exascale throughput as a distributed network in 2020.

---

## 🔐 Why it's trustworthy

- **Confidential computing** — workloads run in encrypted sandboxes; hosts can't read the RAM/data on their own machines.
- **100% India-hosted** — control planes, metadata and relay traffic never cross the border (DPDP-aligned).
- **≥3× redundancy** — every task chunk is mirrored across independent machines, so a closed laptop never fails a job.
- **Graceful eviction** — cordon-and-drain 30 min before your scheduled exit; checkpoints upload, your device is returned.

---

## 🗺️ Roadmap

| Phase | Timeline | Goal | Target |
| --- | --- | --- | --- |
| **Alpha** | Months 1–3 | K3s desktop wrapper across student/dev machines & select colleges | 100 concurrent nodes, zero data loss |
| **Beta** | Months 4–6 | Indian cloud partner for orchestration; solar-grid agreements | 50,000 nodes; inference at 50% less than hyperscalers |
| **National scale** | Months 7–12 | Mobile WASM app; advisory lines with national disaster groups | 1M+ active nodes — a standby sovereign supercomputer |

---

## 💻 This repository (the landing page)

A single, self-contained, dependency-free `index.html` (inline CSS + vanilla-JS canvas animation). No build step.

```bash
# Clone
git clone https://github.com/nandal/dum360-site.git
cd dum360-site

# Option A: just open it
open index.html        # macOS  (use xdg-open on Linux)

# Option B: serve locally (recommended)
python3 -m http.server 8080
# then visit http://localhost:8080
```

Deployed via **GitHub Pages**; `CNAME` (when present) points the custom domain at this site.

---

## 🤝 Contributing

DUM360 is an open, ambitious, nation-scale idea — **builders, researchers, designers and domain experts are all welcome.**

**Ways to get involved**

- 🧑‍💻 **Code** — distributed systems, Kubernetes/K3s/KubeEdge, WASM, scheduling, confidential computing, frontend.
- 🔬 **Research** — distributed inference, model sharding over NKN, tidal/wave & seawater-cooled compute, energy modeling.
- 🎨 **Design / content** — UI, brand, docs, diagrams.
- 🏫 **Institutional partners** — universities, PSUs, enterprises and MSMEs willing to pilot idle-capacity sharing.

**How to start**

1. ⭐ Star the repo and read this README.
2. ✍️ Fill the [**Join the Mesh** form](https://forms.gle/a2JxYZAZu1otR1gm7) (pick "Contributor / Builder").
3. 🐛 Open an [issue](https://github.com/nandal/dum360-site/issues) to propose an idea or report a bug.
4. 🔧 For landing-page changes: fork → branch → edit `index.html` → open a Pull Request.

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

---

## ⚠️ Status & disclaimer

DUM360 is currently a **concept / early-stage project**. Performance figures (e.g. "multi-ExaFLOP", "50% cheaper") are *aspirational targets* and design goals, not measured results. Tidal/wave-powered compute is a forward-looking R&D track; floating-solar + seawater-cooling is the near-term realistic path. Nothing here is a commitment of capacity or service.

---

## 📫 Contact

- **Join / express interest:** [forms.gle/a2JxYZAZu1otR1gm7](https://forms.gle/a2JxYZAZu1otR1gm7)
- **Author:** Sandeep Nandal

<div align="center">

**Made in India 🇮🇳 · Sovereign by design · Hosted 100% in India**

</div>
