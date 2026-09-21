<div align="center">

<img src="assets/logo.png" width="118" alt="Ardit Berisha" />

# Ardit Berisha

**AI researcher and engineer.** Founder of Grow Labs.<br>
I train language models from scratch, then make them run on hardware that shouldn't be able to run them.

<sub>Born 6 February 2006 · Building since I was ten · Kosovo</sub>

<br>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-ardit--berishaa1-1B3BD6?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ardit-berishaa1/)
[![Amaro Than](https://img.shields.io/badge/App_Store-Amaro_Than-1B3BD6?style=flat-square&logo=apple&logoColor=white)](https://apps.apple.com/be/app/amaro-than/id6756788715)
[![AINARA](https://img.shields.io/badge/App_Store-AINARA-1B3BD6?style=flat-square&logo=apple&logoColor=white)](https://apps.apple.com/us/app/ainara/id6812123504)
[![Instagram](https://img.shields.io/badge/Instagram-ardit.berishaa1-1B3BD6?style=flat-square&logo=instagram&logoColor=white)](https://www.instagram.com/ardit.berishaa1/)

</div>

---

> ### I never got a computer science degree. I pre-trained myself.
>
> School doesn't teach you. It fine-tunes what you already know.

I went to a computer science high school, and that is the whole of my formal education in this.
Everything else came from documentation, from source code, and from breaking things until they
made sense. I have never taken a course in technology — not one.

---

## The range

|  | |
|---|---|
| **Parameters trained** | 20M → 32B, from scratch |
| **Hardware** | one laptop → NVIDIA GPUs on Google Cloud |
| **Deployed on** | phones, low-end PCs, CPU-only inference |
| **Started** | 2016, age 10, writing BAT files |

I trained my first model in 2022: **20 million parameters, 10,000 samples**, on my own laptop.
Three runs brought the overfitting gap from above **2.9** down to **0.1851** — doubling the
dataset cut it by about 68%. Everything I know about learning rate, dropout and temperature came
from breaking that model first.

Work now runs at **12B and 32B** on NVIDIA GPUs in Google Cloud. The method never changed. Only
the cost of being wrong did.

---

## What I work on

**Pre-training** — tokenizer, embeddings, transformer layers, output head, and the training loop
that grinds cross-entropy loss down. Same six stages at 20M and at 32B.

**Post-training** — the stage that decides whether a model is usable or useless. Learning rate,
dropout, weight decay and sampling temperature separate coherent text from a loop or a confident lie.

**Data development** — corpora as JSONL, one example per line, validation held back so I can tell
learning apart from memorising. If a fact is not in the data, the model cannot know it.

**Running it on bad hardware** — most of the world does not have an H100. I would rather ship
something that runs on what people already own than something that needs a datacentre to say hello.

---

## Projects

| Repository | What it is |
|---|---|
| **[marie](https://github.com/arditbe/marie)** | Open-source general intelligence for medicine and micro-scale instruments. Find it at 10⁻² m, remove it at 10⁻⁵ m, without taking the healthy tissue around it. An instrument working at a micron cannot be driven by a hand — so the intelligence comes first, and the instrument is its hand. |
| **[auditor](https://github.com/arditbe/auditor)** | An agent that audits your fine-tuned model on its own, on a schedule. Writes fresh probes each run, has a separate judge commit to criteria *before* seeing the answer, makes one probe in four a trap for hallucination, and drills harder wherever a score comes back weak. Google ADK · Vertex AI · Firestore · Cloud Run. |
| **[ReShoot](https://github.com/arditbe/ReShoot)** | A local-first photo metadata auditor and editor. Describe a shot in plain English; it rewrites EXIF, XMP and IPTC to match, then scores how convincing the result is. Golden hour is computed from the NOAA solar equations, not guessed. Your original file is never touched. |
| **[foryou-ai-engine](https://github.com/arditbe/foryou-ai-engine)** | **AINARA** — the recommendation engine behind Amaro Than's For You feed. A 14-dimension ranker over follow graph, watch time, text and visual interest match, trend velocity and author affinity, with a diversity pass so the feed doesn't collapse onto one author. |
| **[antinude](https://github.com/arditbe/antinude)** | A deliberately conservative NSFW detection API. Flags explicit content, ignores anything that is merely skin — because in moderation the expensive mistake is the false positive. CPU-only, no CUDA. |
| **[scrape-the-internet](https://github.com/arditbe/scrape-the-internet)** | Collects text across DuckDuckGo, Bing, Yandex and AOL and writes JSONL ready for fine-tuning. Built because the dataset is the part nobody hands you. |

---

## Research

Nine papers, written under Grow Labs in September 2026. All of them report what failed as
carefully as what worked.

<details>
<summary><b>Building models</b></summary>

<br>

- **[How to Build an AI From Scratch: A Complete Step-by-Step Guide](papers/how-to-build-an-ai.pdf)**<br>
  The whole build with every line of code — setup, data, tokenizing, the transformer, the training
  loop, hyperparameters, and sampling. Runs on a laptop. *More data gives better generation, and
  reading the output is the only true test.*

- **[How to Make AI: Building a Language Model From Scratch](papers/how-to-make-ai.pdf)**<br>
  Written around my first model: 20M parameters, 10,000 samples. Every setting that broke it first,
  and the numbers that fixed each one.

- **[Fine-Tuning Makes Specialists: Why Fine-Tuned Models Behave Like Narrow AI](papers/fine-tuning-narrow-ai.pdf)**<br>
  Fine-tuning usually moves a model *towards* narrow AI, not towards general intelligence. Evidence
  on catastrophic forgetting, and the one real exception. Written out of fine-tuning Mistral-7B for
  the Romani language.

- **[Auditor: An Autonomous Agent for Continuous Evaluation of Fine-Tuned Models](papers/auditor-paper.pdf)**<br>
  The system paper behind the repository. Anyone can fine-tune on a laptop now; almost nobody can
  tell whether the result is any good.

</details>

<details>
<summary><b>Where this is going</b></summary>

<br>

- **[From Narrow to General: Can Self-Learning Systems Lead to AGI?](papers/from-narrow-to-general.pdf)**<br>
  Scale alone will not reach AGI, because a model's knowledge freezes the moment training ends. A
  proposal for systems that update themselves while acting, and five experiments to test it.

- **[How AI Works, and Can It Take Over the World?](papers/how-ai-works.pdf)**<br>
  ANI, AGI, ASI in plain language, and what changes if a superintelligence has a body. A Hollywood
  takeover is not the danger. Loss of control is, and the near-term harms are already here.

- **[How AI and AGI Can Change the World for Good](papers/ai-for-good.pdf)**<br>
  The other side of the argument: where narrow AI already does measurable good, and what must be
  true for the benefits to reach everyone. Real and large — but not automatic.

</details>

<details>
<summary><b>Measuring the field</b></summary>

<br>

- **[Do AI Benchmarks Matter?](papers/do-benchmarks-matter.pdf)**<br>
  Goodhart's law applies the moment labs compete on a table. Test setup alone moved one model
  between 67.4% and 73.7% on the same benchmark. Add contamination and saturation, and a two-point
  lead means almost nothing.

- **[Claude and ChatGPT: Two Paths in AI, and How GPT-6 Astra Changed the View](papers/claude-vs-chatgpt.pdf)**<br>
  Two philosophies, and what Astra changed. The question is no longer which model is smartest, but
  which can be trusted, measured and controlled.

</details>

---

## Where the work lives

**Grow Labs** — my own AI lab. Training runs, the papers, and research into models that keep
learning after deployment. This is my full focus.

**Amaro Than Platforms LLC** — CTO and co-founder since 2022, written line by line. Stepping away
to put everything into Grow Labs.

**Friday** — my own AI platform, built independently.

**Tubify** — the social platform I built in 2020, where everything I had taught myself stopped
being separate tricks and became one system.

---

<div align="center">
<sub>

Open to research collaboration, compute partnerships, and anything that has to survive contact
with real people's devices.

**[LinkedIn](https://www.linkedin.com/in/ardit-berishaa1/)** · **[Instagram](https://www.instagram.com/ardit.berishaa1/)**

</sub>
</div>
