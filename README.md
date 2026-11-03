<div align="center">

<h1>Abhimanyu Prasad</h1>

<p>I work on Bhojpuri NLP, on whether AI tests can be trusted, and on Rust systems.<br/>Class 12 student in Hazaribagh, Jharkhand, India.</p>

<p>
<img src="https://img.shields.io/badge/papers%20accepted-3-6f42c1?style=for-the-badge" alt="3 papers accepted"/>
<img src="https://img.shields.io/badge/under%20review%20%2F%20revision-2-6e7781?style=for-the-badge" alt="2 papers under review or in revision"/>
<img src="https://img.shields.io/badge/merged%20PRs-13-2ea043?style=for-the-badge" alt="13 merged PRs"/>
<img src="https://img.shields.io/badge/CVE-credited%20finder-cf222e?style=for-the-badge" alt="Credited CVE finder"/>
<img src="https://img.shields.io/badge/Bhojpuri%20labels-451K-1f6feb?style=for-the-badge" alt="451K Bhojpuri labels"/>
<img src="https://img.shields.io/badge/HF%20downloads-1.8K%2B-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="1.8K+ Hugging Face downloads"/>
</p>

Papers accepted at NeurIPS 2026 (UserSim and ATTRIB) and IEEE AIoT 2026. My Bhojpuri work is in Stanford's Stanza v1.15.0, and I have a patent application in India.

<p>
<a href="https://openreview.net/profile?id=~Abhimanyu_Prasad3"><img src="https://img.shields.io/badge/OpenReview-8C1B13" alt="OpenReview"/></a>
<a href="https://orcid.org/0009-0003-6740-3445"><img src="https://img.shields.io/badge/ORCID-A6CE39?logo=orcid&logoColor=white" alt="ORCID"/></a>
<a href="https://huggingface.co/abhiprd2000"><img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?logo=huggingface&logoColor=black" alt="Hugging Face"/></a>
<a href="https://crates.io/crates/tokcost"><img src="https://img.shields.io/badge/crates.io-tokcost-E6B14C?logo=rust&logoColor=white" alt="tokcost on crates.io"/></a>
<a href="https://github.com/shodhx"><img src="https://img.shields.io/badge/ShodhX-Research-24292F?logo=github&logoColor=white" alt="ShodhX Research"/></a>
</p>

</div>

### Hi there <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="28" alt="waving hand"/>

- 🔭 I study how AI systems are tested, and I build data and tools for **Bhojpuri**, my language.
- 🎯 Next: getting more Bhojpuri speakers to check the sentences my models disagree on.
- 🧑‍🏫 I've run coding sessions for 250 students at my school, though my own subject is Painting.
- 💻 Fun fact: my laptop is a hand-me-down. I fitted its SSD myself and moved the hard disk into the CD-drive slot.
- 🎮 Off the keyboard: Rusher in Call of Duty: Mobile, and a run up Canary Hill most mornings.

## Bhojpuri NLP

To my knowledge, these are among the first open-source sentiment resources for Bhojpuri. Version 2 (October 2026) is native text, built with [PURVA](https://github.com/shodhx/purva).

| | |
|---|---|
| **[PURVA Bhojpuri Sentiment Corpus v2](https://huggingface.co/datasets/abhiprd2000/Bhojpuri-Behavioral-Corpus-8K)** | **90,207** native sentences from 11 websites, with **451,002** labels from 5 open LLMs (Aya, Gemma, Llama, Mistral, Qwen) in 4 classes. I hand-labelled 270 sentences to check the labels. Split into train, dev and test. |
| **[Bhojpuri Sentiment Model v2](https://huggingface.co/abhiprd2000/bhojpuri-sentiment-model)** | IndicBERTv2 fine-tuned on PURVA labels. It gets **65.7%** accuracy against human labels on native text, **81%** on news and **83%** on encyclopedic text. |
| **[Maithili and Hindi](https://huggingface.co/abhiprd2000)** | Maithili_Sentiment_8K dataset, plus Maithili and Hindi sentiment models. |

**[Stanza](https://github.com/stanfordnlp/stanza) (Stanford NLP):** Bhojpuri ships in [v1.15.0](https://github.com/stanfordnlp/stanza/releases/tag/v1.15.0), which credits me by name. Most of my work was preparing the data and training the Bhojpuri models, using PURVA's text and resources. [4 PRs merged](https://github.com/stanfordnlp/stanza/pulls?q=is%3Apr+author%3Aabhiprd2000+is%3Amerged), plus [48 tag fixes](https://github.com/UniversalDependencies/UD_Bhojpuri-BHTB/pull/2) to the UD Bhojpuri treebank.

<details>
<summary>What I did for Stanza</summary>

- converted the IIT (BHU) Bhojpuri POS corpus, about 14,780 sentences
- cleaned and de-duplicated the training data, and reported a train/test near-duplicate leak I found in my own results
- ran tagging and parsing experiments with Hindi as donor data (MuRIL did best on POS tags)
- opened [issue #1654](https://github.com/stanfordnlp/stanza/issues/1654), where the work started

</details>

## Research

**Ordered Disagreement in Open-Weight LLM Annotator Committees: Lessons from Building a Bhojpuri Sentiment Resource**<br>
<img src="https://img.shields.io/badge/status-under%20review-lightgrey" alt="under review"/> With Dr. Deepak Rakesh (NIT Bhopal). [[code](https://github.com/shodhx/purva)] [[data](https://huggingface.co/datasets/abhiprd2000/Bhojpuri-Behavioral-Corpus-8K)]<br>
Five LLMs don't disagree at random: they sit on one shared scale (Loevinger's H = 0.76), so a native speaker only needs to check the sentences where they split.

<details>
<summary>Details</summary>

- Collected 90,207 sentences from 11 Bhojpuri websites (76,966 after cleaning), recording each one's source, style and licence; removed almost 12,000 whose origin I couldn't verify and 1,301 near-duplicates.
- Five open models from five companies labelled every sentence across 45 runs on free Kaggle GPUs: 451,002 labels. I hand-labelled 270 sentences to check them.
- Dawid-Skene, the standard way to combine labellers, did worse than a simple majority vote (57% vs 66%), and language-ID tools often mistook literary Bhojpuri for Hindi.

</details>

**Same Failure, Different Cause: Ungrounded Tool-Call Provenance in Simulated Agent Evaluation**<br>
<img src="https://img.shields.io/badge/NeurIPS%202026-UserSim%20Workshop-6f42c1" alt="NeurIPS 2026 UserSim Workshop"/> Sole author. [[OpenReview](https://openreview.net/forum?id=DVa9SVOw5s)] [[NeurIPS](https://neurips.cc/virtual/2026/169228)] [[code](https://github.com/abhiprd2000/simswap)]<br>
Qwen and Llama fail the same tau2-bench tasks for different reasons, but the benchmark counts them as one failure.

**Ablate-and-Measure Breaks When the Measurement Depends on the Ablation**<br>
<img src="https://img.shields.io/badge/NeurIPS%202026-ATTRIB%20Workshop%2C%20idea%20track-6f42c1" alt="NeurIPS 2026 ATTRIB Workshop, idea track"/> Sole author. [[OpenReview](https://openreview.net/forum?id=PfQ094vtjq)] [[NeurIPS](https://neurips.cc/virtual/2026/161696)] [[code](https://github.com/abhiprd2000/attrib-context-ablation)]<br>
In a pre-registered 144-run study, whether a score even existed depended on the condition: it was defined for only 50 to 92% of runs.

<details>
<summary>Details</summary>

- Removed parts of an AI agent's context in six ways: 12 tasks × 2 seeds × 6 conditions, about 16 GPU-hours on free Kaggle T4s.
- No condition made a significant difference after correction (smallest adjusted p = 0.235).
- tau2-bench only scores runs that end cleanly, which is why the metric itself moved. I reported two deviations from my pre-registration, and reviewed two other submissions for this workshop.

</details>

**Verify on Read, Update in Log Time: Per-Block Integrity for Mutable Edge-AI Model Files**<br>
<img src="https://img.shields.io/badge/IEEE%20AIoT%202026-workshop%20paper%20accepted-00629B" alt="IEEE AIoT 2026 workshop paper accepted"/> <img src="https://img.shields.io/badge/Indian%20patent%20application-202631065480-555555" alt="Indian patent application 202631065480"/> Code: [[model-integrity-bench](https://github.com/abhiprd2000/model-integrity-bench)] [[axiom-os-kernel](https://github.com/abhiprd2000/axiom-os-kernel)]<br>
Catches a tampered AI model file on every read, and updates a block in 4.9 µs instead of 44 ms to re-hash the whole file.

<details>
<summary>Details</summary>

- Linux's fs-verity checks files block by block, but only files that never change. My checker keeps a Merkle tree over 4 KiB blocks and verifies only the blocks each read touches.
- In a tamper test, one flipped weight failed exactly one block, and no corrupt bytes were served.
- Measured on an Intel i5-5200U laptop and a Snapdragon 7 Gen 4 phone. Design advice from Prof. Subodh Kumar (IIT Delhi).

</details>

**Article on "zombie" IoT devices**<br>
<img src="https://img.shields.io/badge/IEEE%20Potentials-in%20revision-00629B" alt="IEEE Potentials, in revision"/> Sole author.<br>
Why cloud-dependent smart devices stop working when their company shuts down.

## Security and open source

- **[GitPython](https://github.com/gitpython-developers/GitPython):** credited finder of [CVE-2026-67325](https://github.com/advisories/GHSA-2f96-g7mh-g2hx) (high severity, CVSS 3.1: 8.8). Abbreviated option names could slip past its guard against dangerous git options. My fix: [commit 2ab0516](https://github.com/gitpython-developers/GitPython/commit/2ab051697940144545a14d2f4a639c6409c3187f).
- **[Kaggle CLI](https://github.com/Kaggle/kaggle-cli):** [2 PRs merged](https://github.com/Kaggle/kaggle-cli/pulls?q=is%3Apr+author%3Aabhiprd2000+is%3Amerged), including a guard against path traversal when extracting downloaded models.

## Projects

<a href="https://github.com/abhiprd2000/axiom-os-kernel"><img src="https://raw.githubusercontent.com/abhiprd2000/axiom-os-kernel/main/assets/axiom-banner.png" alt="Axiom OS" width="100%"/></a>

**[axiom-os-kernel](https://github.com/abhiprd2000/axiom-os-kernel):** a bare-metal Rust kernel for x86-64 and ARM that checks file integrity on every read. The model-file checker grew out of it.

**[tokcost](https://github.com/abhiprd2000/tokcost):** exact BPE token counts and cost estimates for LLM APIs, as one Rust binary. On [crates.io](https://crates.io/crates/tokcost).

<img src="https://raw.githubusercontent.com/abhiprd2000/tokcost/master/demo/demo.gif" alt="tokcost demo" width="600"/>

**[Vehicle classification](https://github.com/abhiprd2000/vehicle_classification_model-utd)** [[model](https://huggingface.co/abhiprd2000/vehicle_classification_model-utd)]<br>
🏅 **Selected top 4 worldwide for Prof. Feng Chen's AI Safety Lab, UT Dallas.** A CNN trained from scratch on 26,378 images of 8 vehicle types, reaching 78.5% test accuracy against a 50% target.

## How I work

I learned offline from 2023 to 2025, from printed papers and the blog_os tutorial on that old laptop, so most of my public work starts in 2026. I run experiments on free Kaggle GPUs.

<p>
<img src="https://skillicons.dev/icons?i=py,rust,pytorch,linux,bash,git,githubactions,latex,vscode&theme=dark" alt="Python, Rust, PyTorch, Linux, Bash, Git, GitHub Actions, LaTeX, VS Code"/>
</p>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/abhiprd2000/abhiprd2000/output/github-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/abhiprd2000/abhiprd2000/output/github-snake.svg"/>
  <img alt="Contribution graph eaten by a snake" src="https://raw.githubusercontent.com/abhiprd2000/abhiprd2000/output/github-snake.svg"/>
</picture>
