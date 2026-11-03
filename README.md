<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,100:1f6feb&height=190&section=header&text=Abhimanyu%20Prasad&fontColor=ffffff&fontSize=46&fontAlignY=36&desc=How%20do%20we%20know%20it%20works%3F&descSize=18&descAlignY=58&animation=fadeIn" width="100%" alt="Abhimanyu Prasad"/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=58A6FF&center=true&vCenter=true&width=640&lines=Bhojpuri+NLP+%C2%B7+Stanza+contributor;Testing+whether+AI+tests+can+be+trusted;Rust+kernels+that+check+every+read;Class+12+%C2%B7+Hazaribagh%2C+India" alt="Bhojpuri NLP, AI evaluation, Rust systems"/>

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

## 🔬 Research

**Ordered Disagreement in Open-Weight LLM Annotator Committees: Lessons from Building a Bhojpuri Sentiment Resource**<br>
<img src="https://img.shields.io/badge/status-under%20review-lightgrey" alt="under review"/> with Dr. Deepak Rakesh · [code](https://github.com/shodhx/purva)<br>
Five open models from five companies gave 451,002 labels to 90,207 Bhojpuri sentences. Their disagreements fall on one shared scale (Loevinger's H = 0.76), and Dawid-Skene, the standard way to combine labellers, did worse than a simple majority vote.

**Same Failure, Different Cause: Ungrounded Tool-Call Provenance in Simulated Agent Evaluation**<br>
<img src="https://img.shields.io/badge/NeurIPS%202026-UserSim%20Workshop-6f42c1" alt="NeurIPS 2026 UserSim Workshop"/> sole author · [code](https://github.com/abhiprd2000/simswap)<br>
Qwen and Llama fail the same tau2-bench tasks for different reasons, but the score counts them as one failure.

**Ablate-and-Measure Breaks When the Measurement Depends on the Ablation**<br>
<img src="https://img.shields.io/badge/NeurIPS%202026-ATTRIB%20Workshop%2C%20idea%20track-6f42c1" alt="NeurIPS 2026 ATTRIB Workshop, idea track"/> sole author<br>
In a pre-registered 144-run study, the metric existed for only 50 to 92% of runs, depending on the condition. I also reviewed two submissions for this workshop.

**Verify on Read, Update in Log Time: Per-Block Integrity for Mutable Edge-AI Model Files**<br>
<img src="https://img.shields.io/badge/IEEE%20AIoT%202026-SustainableAIoT%20workshop%2C%20accepted-00629B" alt="IEEE AIoT 2026 workshop, accepted"/> <img src="https://img.shields.io/badge/Indian%20patent%20application-202631065480-555555" alt="Indian patent application 202631065480"/> · [code](https://github.com/abhiprd2000/model-integrity-bench)<br>
Catches a tampered AI model file on every read, and updates a block in 4.9 µs instead of 44 ms to re-hash the whole file.

<table>
<tr>
<td align="center" width="50%"><img src="https://raw.githubusercontent.com/abhiprd2000/axiom-os-kernel/main/assets/fig1.png" alt="Each read hashes only the blocks it touches" width="100%"/><br><sub>Each read hashes only the blocks it touches</sub></td>
<td align="center" width="50%"><img src="https://raw.githubusercontent.com/abhiprd2000/axiom-os-kernel/main/assets/fig2.png" alt="Block-level checks stay flat as files grow, on x86-64 and ARM64" width="100%"/><br><sub>Block-level checks stay flat as files grow, on x86-64 and ARM64</sub></td>
</tr>
</table>

## 🤝 Open source

- **[Stanza](https://github.com/stanfordnlp/stanza)** (Stanford NLP): added Bhojpuri support. Opened [issue #1654](https://github.com/stanfordnlp/stanza/issues/1654) and had [5 PRs merged](https://github.com/stanfordnlp/stanza/pulls?q=is%3Apr+author%3Aabhiprd2000+is%3Amerged), including the IIT (BHU) corpus converter credited in the [v1.15.0 release notes](https://github.com/stanfordnlp/stanza/releases/tag/v1.15.0).
- **[UD Bhojpuri treebank](https://github.com/UniversalDependencies/UD_Bhojpuri-BHTB)**: [48 tag fixes](https://github.com/UniversalDependencies/UD_Bhojpuri-BHTB/pull/2), merged August 2026.
- **[GitPython](https://github.com/gitpython-developers/GitPython)**: credited finder of [CVE-2026-67325](https://github.com/advisories/GHSA-2f96-g7mh-g2hx), a high-severity command injection (CVSS 3.1: 8.8), fixed in 3.1.51.
- **[DoWhy](https://github.com/py-why/dowhy)** (causal inference): [my pull requests](https://github.com/py-why/dowhy/pulls?q=is%3Apr+author%3Aabhiprd2000).
- **Kaggle CLI**: merged fixes to Kaggle's official command-line tool. <!-- add your PR links here -->

## 🛠️ Projects

<a href="https://github.com/abhiprd2000/axiom-os-kernel"><img src="https://raw.githubusercontent.com/abhiprd2000/axiom-os-kernel/main/assets/axiom-banner.png" alt="Axiom OS" width="100%"/></a>

**[axiom-os-kernel](https://github.com/abhiprd2000/axiom-os-kernel)**: a bare-metal Rust kernel that checks file integrity on every read. The model-file checker above grew out of it. Design advice from Prof. Subodh Kumar (IIT Delhi).

**[tokcost](https://github.com/abhiprd2000/tokcost)**: exact BPE token counts and cost estimates for LLM APIs, as one Rust binary. On [crates.io](https://crates.io/crates/tokcost).

<img src="https://raw.githubusercontent.com/abhiprd2000/tokcost/master/demo/demo.gif" alt="tokcost demo" width="100%"/>

**[Vehicle classification](https://github.com/abhiprd2000/vehicle_classification_model-utd)**: a CNN trained from scratch (not pretrained) to sort 8 kinds of vehicles, with 78.5% test accuracy on 5,276 held-out images ([model](https://huggingface.co/abhiprd2000/vehicle_classification_model-utd)).<br>
🏅 Selected top 4 worldwide for Prof. Feng Chen's AI Safety Lab, UT Dallas, via an ML coding challenge.

**[Hugging Face](https://huggingface.co/abhiprd2000)**: my earlier Bhojpuri, Maithili and Hindi sentiment models and datasets (partly translated text).

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
