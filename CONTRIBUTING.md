# Contributing to DUM360

Thanks for your interest in **DUM360 (Distributed Unified Mesh 360)** — India's citizen-powered sovereign supercomputer mesh. This is an ambitious, nation-scale idea, and contributions of every kind are welcome.

> New here? Start with the [README](README.md), then fill the [Join the Mesh form](https://forms.gle/a2JxYZAZu1otR1gm7) and pick **"Contributor / Builder"**.

---

## Ways to contribute

| Area | Examples |
| --- | --- |
| 🧑‍💻 **Engineering** | Distributed scheduling/orchestration (Kubernetes, K3s, KubeEdge), WASM sandboxes, confidential computing, networking/relay, billing/metering, frontend. |
| 🔬 **Research** | Distributed LLM inference, pipeline/tensor parallelism over NKN, churn-tolerant redundancy, tidal/wave & seawater-cooled compute, energy & cost modeling. |
| 🎨 **Design & docs** | UI/UX, brand, diagrams, this landing page, written explainers. |
| 🏫 **Partnerships** | Universities, PSUs, enterprises and MSMEs willing to pilot idle-capacity sharing; solar/offshore operators. |
| 🐛 **Testing & feedback** | Try the site, file issues, suggest improvements. |

---

## This repository

`dum360-site` is the **public landing page** — a single, dependency-free `index.html` (inline CSS + a vanilla-JS `<canvas>` mesh animation). There is **no build step**.

### Run it locally

```bash
git clone https://github.com/nandal/dum360-site.git
cd dum360-site
python3 -m http.server 8080   # then open http://localhost:8080
# or simply: open index.html
```

### Editing guidelines

- Keep it **a single self-contained `index.html`** (no frameworks, no build tooling, no external runtime deps). Google Fonts via CDN is fine.
- Match the existing **clean modern SaaS** style — CSS variables at the top of `<style>`, consistent spacing, `.reveal` scroll animations.
- Test in a browser at **desktop and mobile widths** before opening a PR. Check the mesh animation, the **Rashtra Seva** toggle, and node hover tooltips.
- Keep claims **honest** — performance numbers are aspirational; don't overstate.

---

## Pull request process

1. **Fork** the repo and create a branch: `git checkout -b feat/short-description`.
2. Make focused changes with clear, descriptive commits.
3. Verify locally (desktop + mobile).
4. Open a **Pull Request** describing *what* changed and *why*. Screenshots/GIFs for visual changes are appreciated.
5. A maintainer will review. Be responsive to feedback. 🙏

### Commit style

- Use clear, imperative messages: `Add inference architecture section`, `Fix mesh layout on mobile`.
- One logical change per commit where practical.

---

## Reporting issues

Open a [GitHub issue](https://github.com/nandal/dum360-site/issues) with:

- **What** you expected vs. what happened (for bugs), or a clear description of the idea/proposal.
- Steps to reproduce, browser/OS, and screenshots where relevant.

---

## Code of conduct

Be respectful, constructive and inclusive. We're building national infrastructure together — assume good faith, welcome newcomers, and keep discussions focused on ideas.

---

## Questions?

Express interest or reach out via the [Join the Mesh form](https://forms.gle/a2JxYZAZu1otR1gm7).

**Jai Hind. 🇮🇳**
