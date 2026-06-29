# CogChat

**Knowledge Graph-Augmented Conversational AI with a Heterogeneous Graph Transformer for Cognitive Grounding in Design Generation** — UIST '26 project page.

CogChat grounds an LLM chat assistant in a personal **heterogeneous knowledge graph** built from each designer's input, and uses a **Heterogeneous Graph Transformer (HGT)** to select the structurally relevant nodes for every response — and to generate *intentional* and *exploratory* probing questions.

## Project page

The site is a single static file: [`index.html`](index.html). Figures live in [`assets/img/`](assets/img/).

### Run locally

```bash
python -m http.server 8000
# then open http://localhost:8000
```

### GitHub Pages

Enable Pages on the `main` branch (root). A `.nojekyll` file is included so the `assets/` directory is served as-is.

## Contents

- **Problem** — why recency-based context loses the relations design reasoning runs on
- **Interface** — interactive in-context entity inspection
- **Pipeline** — the five per-turn stages (KG construction → link sets → HGT embedding → grounded response → probing)
- **Probing questions** — intentional vs. exploratory, derived from graph structure
- **Results** — technical evaluation (ASQA, RewardBench) and the within-subjects study with nine professional designers
