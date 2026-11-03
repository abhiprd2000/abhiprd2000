<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,100:1f6feb&height=190&section=header&text=Abhimanyu%20Prasad&fontColor=ffffff&fontSize=46&fontAlignY=36&desc=How%20do%20we%20know%20it%20works%3F&descSize=18&descAlignY=58&animation=fadeIn" width="100%" alt="Abhimanyu Prasad"/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=58A6FF&center=true&vCenter=true&width=640&lines=Bhojpuri+NLP+%C2%B7+Stanza+contributor;Testing+whether+AI+tests+can+be+trusted;Rust+kernels+that+check+every+read;Class+12+%C2%B7+Hazaribagh%2C+Jharkhand%2C+India" alt="Bhojpuri NLP, AI evaluation, Rust systems"/>

<p>
<a href="https://openreview.net/profile?id=~Abhimanyu_Prasad3"><img src="https://img.shields.io/badge/OpenReview-8C1B13?style=for-the-badge" alt="OpenReview"/></a>
<a href="https://orcid.org/0009-0003-6740-3445"><img src="https://img.shields.io/badge/ORCID-A6CE39?style=for-the-badge&logo=orcid&logoColor=white" alt="ORCID"/></a>
<a href="https://huggingface.co/abhiprd2000"><img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face"/></a>
<a href="https://crates.io/crates/tokcost"><img src="https://img.shields.io/badge/crates.io-tokcost-E6B14C?style=for-the-badge&logo=rust&logoColor=white" alt="tokcost on crates.io"/></a>
<a href="https://github.com/shodhx"><img src="https://img.shields.io/badge/ShodhX-Research-24292F?style=for-the-badge&logo=github&logoColor=white" alt="ShodhX Research"/></a>
</p>

</div>

### Hi there <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="28" alt="waving hand"/>

- 🔭 I study how AI systems are tested, and I build data and tools for **Bhojpuri**, my language.
- 🎯 Next: getting more Bhojpuri speakers to check the sentences my models disagree on.
- 📚 Curious about: how much a small test set can really prove.
- 🗣️ I speak Bhojpuri, Hindi and English.
- 🧑‍🏫 I've run coding sessions for 250 students at my school, though my own subject is Painting.
- 💻 Fun fact: my laptop is a hand-me-down. I fitted its SSD myself and moved the hard disk into the CD-drive slot.
- 🎮 Off the keyboard: Rusher in Call of Duty: Mobile, and a run up Canary Hill most mornings.

## 🗣️ Bhojpuri NLP

To my knowledge, my Hugging Face models and datasets are among the first open-source sentiment resources for Bhojpuri. They were updated with [PURVA](https://github.com/shodhx/purva) in October 2026, and together with my Maithili and Hindi releases they have **1,800+ downloads**.

| Resource | What it is | Numbers |
|---|---|---|
| [bhojpuri-sentiment-model](https://huggingface.co/abhiprd2000/bhojpuri-sentiment-model) | XLM-RoBERTa fine-tuned for 3-class Bhojpuri sentiment on 18,049 sentences | **97.6% accuracy** (macro F1 0.976) on a balanced 501-sentence test set · 70% on 30 new out-of-domain sentences · 133 downloads |
| [Bhojpuri-Behavioral-Corpus-8K](https://huggingface.co/datasets/abhiprd2000/Bhojpuri-Behavioral-Corpus-8K) | 68,822 Bhojpuri sentences with English translations, balanced across positive, negative and neutral, in science, agriculture, environment and general domains | 210 downloads |
| [Maithili_Sentiment_8K](https://huggingface.co/datasets/abhiprd2000/Maithili_Sentiment_8K) | Maithili sentiment dataset | 349 downloads |
| [maithili-sentiment-model](https://huggingface.co/abhiprd2000/maithili-sentiment-model) · [hindi-sentiment-model](https://huggingface.co/abhiprd2000/hindi-sentiment-model) | Sentiment models for Maithili and Hindi | 124 · 152 downloads |

**[Stanza](https://github.com/stanfordnlp/stanza) (Stanford NLP):** Bhojpuri ships in Stanza [v1.15.0](https://github.com/stanfordnlp/stanza/releases/tag/v1.15.0), and the release notes credit me by name. Most of my work was preparing the data and training the Bhojpuri models, using text and resources from PURVA:
- converted the IIT (BHU) Bhojpuri POS corpus, about 14,780 sentences, for Stanza
- cleaned and de-duplicated the training data, and reported a train/test near-duplicate leak I found in my own results
- ran tagging and parsing experiments with Hindi as donor data (MuRIL did best on POS tags)
- opened [issue #1654](https://github.com/stanfordnlp/stanza/issues/1654) and had [4 PRs merged](https://github.com/stanfordnlp/stanza/pulls?q=is%3Apr+author%3Aabhiprd2000+is%3Amerged)

**[UD Bhojpuri treebank](https://github.com/UniversalDependencies/UD_Bhojpuri-BHTB):** went through the treebank tag by tag and fixed [48 wrong tags](https://github.com/UniversalDependencies/UD_Bhojpuri-BHTB/pull/2), merged August 2026. With Stanza, that's 5 merged PRs.

## 🔬 Research

### Ordered Disagreement in Open-Weight LLM Annotator Committees: Lessons from Building a Bhojpuri Sentiment Resource
<img src="https://img.shields.io/badge/status-under%20review-lightgrey" alt="under review"/> with Dr. Deepak Rakesh · [code](https://github.com/shodhx/purva)

Bhojpuri has tens of millions of speakers but, to my knowledge, no sentiment dataset of native text with human-checked labels, and very few people can label it. Can free, open models do that labelling instead?
- I collected 90,207 sentences from 11 Bhojpuri websites, recording each one's source, style and licence. I removed almost 12,000 whose origin I couldn't verify and 1,301 near-duplicates.
- Five open models from five companies labelled every sentence, across 45 runs on free Kaggle GPUs: 451,002 labels. I hand-labelled 270 sentences to check them.
- The models don't disagree at random. Each has its own line for what counts as an opinion, and they all sit on one shared scale (Loevinger's H = 0.76). So a native speaker only needs to check the sentences where they split, about a third of the data.
- Dawid-Skene, the standard way to combine labellers, did worse than a simple majority vote (57% vs 66%), and language-ID tools often mistook literary Bhojpuri for Hindi.

### Same Failure, Different Cause: Ungrounded Tool-Call Provenance in Simulated Agent Evaluation
<img src="https://img.shields.io/badge/NeurIPS%202026-UserSim%20Workshop-6f42c1" alt="NeurIPS 2026 UserSim Workshop"/> sole author · [OpenReview](https://openreview.net/forum?id=DVa9SVOw5s) · [NeurIPS page](https://neurips.cc/virtual/2026/169228) · [code](https://github.com/abhiprd2000/simswap)

Agent benchmarks like tau2-bench report pass or fail. I traced where each tool call's arguments came from in runs of Qwen2.5-7B-Instruct and Llama-3.1-8B-Instruct. Both models fail the same tasks, but their ungrounded tool calls come from different causes, so one score hides two different problems.

### Ablate-and-Measure Breaks When the Measurement Depends on the Ablation
<img src="https://img.shields.io/badge/NeurIPS%202026-ATTRIB%20Workshop%2C%20idea%20track-6f42c1" alt="NeurIPS 2026 ATTRIB Workshop, idea track"/> sole author · [OpenReview](https://openreview.net/forum?id=PfQ094vtjq) · [NeurIPS page](https://neurips.cc/virtual/2026/161696) · [code](https://github.com/abhiprd2000/attrib-context-ablation)

Is most of an AI agent's policy document ignored? I removed parts of the agent's context in six ways, in a pre-registered study of 144 runs (12 tasks, 2 seeds, 6 conditions, about 16 GPU-hours on free Kaggle T4s).
- No condition made a significant difference after correction (smallest adjusted p = 0.235).
- The real finding was in the metric: tau2-bench only scores runs that end cleanly, so whether a score existed at all depended on the condition. It was defined for only 50 to 92% of runs.
- I reported two deviations from my pre-registration, and I reviewed two other submissions for this workshop.

### Verify on Read, Update in Log Time: Per-Block Integrity for Mutable Edge-AI Model Files
<img src="https://img.shields.io/badge/IEEE%20AIoT%202026-SustainableAIoT%20workshop%2C%20accepted-00629B" alt="IEEE AIoT 2026 workshop, accepted"/> <img src="https://img.shields.io/badge/Indian%20patent%20application-202631065480-555555" alt="Indian patent application 202631065480"/> · code: [model-integrity-bench](https://github.com/abhiprd2000/model-integrity-bench) · [axiom-os-kernel](https://github.com/abhiprd2000/axiom-os-kernel)

A tampered AI model file can quietly change what the model does. Linux's fs-verity checks files block by block, but only files that never change.
- My checker keeps a Merkle tree over the 4 KiB blocks of a model file and verifies only the blocks each read touches.
- On a write it updates one leaf and its path: 4.9 µs, against 44 ms to re-hash the whole file.
- In a tamper test, one flipped weight failed exactly one block, and no corrupt bytes were served.
- Measured on an Intel i5-5200U laptop and a Snapdragon 7 Gen 4 phone. It grew out of Axiom, my Rust kernel, with design advice from Prof. Subodh Kumar (IIT Delhi).

## 🔐 Open source and security

- **[GitPython](https://github.com/gitpython-developers/GitPython):** credited finder of [CVE-2026-67325](https://github.com/advisories/GHSA-2f96-g7mh-g2hx) (high severity, CVSS 3.1: 8.8). Its guard against dangerous git options could be bypassed with abbreviated option names. I wrote the first fix ([commit 2ab0516](https://github.com/gitpython-developers/GitPython/commit/2ab051697940144545a14d2f4a639c6409c3187f), merged in [#2168](https://github.com/gitpython-developers/GitPython/pull/2168)), which the maintainers extended before releasing 3.1.51.
- **[Kaggle CLI](https://github.com/Kaggle/kaggle-cli):** [merged fixes](https://github.com/Kaggle/kaggle-cli/pulls?q=is%3Apr+author%3Aabhiprd2000+is%3Amerged) to Kaggle's official command-line tool.

## 🛠️ Projects

<a href="https://github.com/abhiprd2000/axiom-os-kernel"><img src="https://raw.githubusercontent.com/abhiprd2000/axiom-os-kernel/main/assets/axiom-banner.png" alt="Axiom OS" width="100%"/></a>

**[axiom-os-kernel](https://github.com/abhiprd2000/axiom-os-kernel):** a bare-metal Rust kernel for x86-64 and ARM that checks file integrity on every read, with FAT32, an ATA driver, process isolation, a priority scheduler and a 28-command shell. The model-file checker above grew out of it.

**[tokcost](https://github.com/abhiprd2000/tokcost):** exact BPE token counts and cost estimates for LLM APIs, as one Rust binary. On [crates.io](https://crates.io/crates/tokcost).

<img src="https://raw.githubusercontent.com/abhiprd2000/tokcost/master/demo/demo.gif" alt="tokcost demo" width="100%"/>

**[Vehicle classification](https://github.com/abhiprd2000/vehicle_classification_model-utd)** · [model](https://huggingface.co/abhiprd2000/vehicle_classification_model-utd)<br>
🏅 **Selected top 4 worldwide for Prof. Feng Chen's AI Safety Lab, UT Dallas.**<br>
The model behind it is a 3-block CNN trained from scratch, with no pretrained weights, on 26,378 images of 8 vehicle types. It reached 78.5% accuracy on 5,276 held-out test images against a 50% target, using dropout and batch normalisation to avoid overfitting. Its model card also lists where it hasn't been tested, like low light and bad weather.

## ⚙️ How I work

I learned offline from 2023 to 2025, from printed papers and the blog_os tutorial on that old laptop, so most of my public work starts in 2026. I run experiments on free Kaggle GPUs and use AI coding assistants for some test, demo and plotting code.

## 🧰 Tools

<p>
<img src="https://skillicons.dev/icons?i=py,rust,pytorch,linux,bash,git,githubactions,latex,vscode&theme=dark" alt="Python, Rust, PyTorch, Linux, Bash, Git, GitHub Actions, LaTeX, VS Code"/>
</p>
<p>
<img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?logo=huggingface&logoColor=black" alt="Hugging Face"/>
<img src="https://img.shields.io/badge/Kaggle-20BEFF?logo=kaggle&logoColor=white" alt="Kaggle"/>
<img src="https://img.shields.io/badge/Stanza-8C1515" alt="Stanza"/>
<img src="https://img.shields.io/badge/BLAKE3-1f6feb" alt="BLAKE3"/>
</p>

## 🐍 Contributions

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/abhiprd2000/abhiprd2000/output/github-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/abhiprd2000/abhiprd2000/output/github-snake.svg"/>
  <img alt="Contribution graph eaten by a snake" src="https://raw.githubusercontent.com/abhiprd2000/abhiprd2000/output/github-snake.svg"/>
</picture>

<div align="center">

> *No data is better than faulty data.*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1f6feb,100:0d1117&height=110&section=footer" width="100%" alt=""/>

</div>
