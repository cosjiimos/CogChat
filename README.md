# CogChat

**Knowledge Graph-Augmented Conversational AI with a Heterogeneous Graph Transformer for Cognitive Grounding in Design Generation**

[Jiin Choi](https://cosjiimos.github.io/)<sup>1,2</sup>, [Kyung Hoon Hyun](https://designai.hanyang.ac.kr/People_Kyung-Hoon-Hyun)<sup>1,2,\*</sup>

<sup>1</sup>[Design AI Lab](https://designai.hanyang.ac.kr), Interior Architecture Design, Hanyang University, Seoul, Republic of Korea
<sup>2</sup>Human-Centered AI Design Institute, Hanyang University, Seoul, Republic of Korea
<sup>\*</sup>Corresponding author

**ACM UIST 2026** &middot; to appear &middot; [arXiv:2608.13216](https://arxiv.org/abs/2608.13216)

![CogChat overview](assets/img/fig_1.png)

CogChat grounds an LLM chat assistant in a personal **heterogeneous knowledge graph** built from each designer's input, and uses a **Heterogeneous Graph Transformer (HGT)** to select the structurally relevant nodes for every response — and to generate *intentional* and *exploratory* probing questions.

LLM chat systems keep context through *recency*: the last few turns in a sliding window. In design conversation this breaks down — relational meaning decays between turns, identical words mean different things to different designers, and the conversation loops instead of deepening. CogChat preserves the relational structure of how a designer thinks, rather than what they said most recently.

## Contents

- **Problem** — why recency-based context loses the relations design reasoning runs on
- **Interface** — interactive in-context entity inspection
- **Pipeline** — the five per-turn stages (KG construction → link sets → HGT embedding → grounded response → probing)
- **Probing questions** — intentional vs. exploratory, derived from graph structure
- **Results** — technical evaluation (ASQA, RewardBench) and the within-subjects study with nine professional designers
