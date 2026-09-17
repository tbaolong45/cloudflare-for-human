# Voice, calls and spoken-media verification: annotated documents

Checked 17 September 2026. Eight selected sources cover synthetic-speech detection, localized audio edits, generalization, human listening, active caller verification, and the narrower meaning of caller-ID authentication. Summaries describe the cited work, including material limits; they do not propose a project architecture. This is a targeted collection, not an exhaustive review.

## A01 — ASVspoof 5: Design, collection and validation of resources for spoofing, deepfake, and adversarial attack detection using crowdsourced speech

**Collected reading copy:** [PDF](../documents/A01-asvspoof5-resources.pdf)

**Authors:** Xin Wang, Héctor Delgado, Hemlata Tak, Jee-weon Jung, Hye-jin Shim, Massimiliano Todisco, Ivan Kukanov, Xuechen Liu, Md Sahidullah, Tomi Kinnunen, Nicholas Evans, Kong Aik Lee, Junichi Yamagishi, Myeonghun Jeong, Ge Zhu, Yongyi Zang, You Zhang, Soumi Maiti, Florian Lux, Nicolas Müller, Wangyou Zhang, Chengzhe Sun, Shuwei Hou, Siwei Lyu, Sébastien Le Maguer, Cheng Gong, Hanjie Guo, Liping Chen, Vishwanath Singh. **Year/venue:** 2026, *Computer Speech & Language* 95, 101825; published online 28 May 2025. **Status:** peer-reviewed journal article.

[Publisher DOI](https://doi.org/10.1016/j.csl.2025.101825) · [Institutional record](https://www.eurecom.edu/en/publication/8080) · [Open published PDF](https://publica-rest.fraunhofer.de/server/api/core/bitstreams/3c721dee-3a01-40cb-b9dd-171e3ee8564b/content)

Documents a speech benchmark involving roughly 2,000 speakers, 32 attack algorithms and varied recording conditions. It includes synthesized speech, converted voices and adversarial attacks, with seven speaker-disjoint partitions. Resource design and baseline experiments distinguish detecting spoofed speech from verifying a claimed speaker under attack. **Limitation:** a curated challenge corpus is not a representative sample of all languages, telephone networks or conversational impersonation scenarios; its coverage defines what its results can establish.

## A02 — ASVspoof 5: Evaluation of Spoofing, Deepfake, and Adversarial Attack Detection Using Crowdsourced Speech

**Collected reading copy:** [PDF](../documents/A02-asvspoof5-evaluation.pdf)

**Authors:** Xin Wang, Héctor Delgado, Nicholas Evans, Xuechen Liu, Tomi Kinnunen, Hemlata Tak, Kong Aik Lee, Ivan Kukanov, Md Sahidullah, Massimiliano Todisco, Junichi Yamagishi. **Year/venue:** 2026, *IEEE Transactions on Audio, Speech and Language Processing* 34, 2354–2367. **Status:** peer-reviewed journal article; open copy is accepted author version v3, 11 April 2026.

[Publisher DOI](https://doi.org/10.1109/TASLPRO.2026.3682962) · [Author record](https://arxiv.org/abs/2601.03944) · [Full text](https://arxiv.org/html/2601.03944v3) · [Open PDF](https://arxiv.org/pdf/2601.03944v3)

Analyzes submissions from 53 teams and subsequent experiments. It examines adversarial attacks, audio encoding, transfer to other datasets and calibration of detector scores. Strong challenge results coexist with degradation on unfamiliar recordings; neural compression can also make genuine speech resemble synthesized output. **Limitation:** performance depends on the evaluation condition and scoring threshold. Benchmark error measures are not a direct estimate of mistakes during live calls, nor proof of the speaker's identity.

## A03 — ADD 2023: the Second Audio Deepfake Detection Challenge

**Collected reading copy:** [PDF](../documents/A03-add2023.pdf)

**Authors:** Jiangyan Yi, Jianhua Tao, Ruibo Fu, Xinrui Yan, Chenglong Wang, Tao Wang, Chu Yuan Zhang, Xiaohui Zhang, Yan Zhao, Yong Ren, Le Xu, Junzuo Zhou, Hao Gu, Zhengqi Wen, Shan Liang, Zheng Lian, Shuai Nie, Haizhou Li. **Year/venue:** 2023, IJCAI Workshop on Deepfake Audio Detection and Analysis, CEUR Workshop Proceedings 3597, 125–130. **Status:** peer-reviewed workshop paper.

[Official proceedings](https://ceur-ws.org/Vol-3597/) · [Open published PDF](https://ceur-ws.org/Vol-3597/paper21.pdf)

Describes three challenge tasks: competition between generation and detection systems, locating manipulated intervals within audio, and identifying the generating algorithm, including an unknown-source category. It is directly relevant to recordings where only a few words have been altered, rather than the entire clip being synthetic. **Limitation:** challenge scores reflect specified generators, datasets and protocols; the training resources include Chinese speech corpora, so they do not establish universal language or channel coverage.

## A04 — Does Audio Deepfake Detection Generalize?

**Collected reading copy:** [PDF](../documents/A04-audio-detection-generalization.pdf)

**Authors:** Nicolas M. Müller, Pavel Czempin, Franziska Dieckmann, Adam Froghyar, Konstantin Böttinger. **Year/venue:** 2022, Interspeech, 2783–2787. **Status:** peer-reviewed conference paper.

[Official record](https://www.isca-archive.org/interspeech_2022/muller22_interspeech.html) · [DOI](https://doi.org/10.21437/Interspeech.2022-108) · [Open published PDF](https://www.isca-archive.org/interspeech_2022/muller22_interspeech.pdf)

Reimplements twelve detector architectures under a common evaluation framework and introduces the In-the-Wild audio dataset: 37.9 hours of authentic and synthetic recordings involving 58 public figures. Models performing well on ASVspoof 2019 often deteriorate substantially on this collected online material. **Limitation:** the dataset contains English-speaking celebrities and politicians, with selected publicly identified fakes; it is neither representative call traffic nor an evaluation of current generation and detection systems.

## A05 — People are poorly equipped to detect AI-powered voice clones

**Collected reading copy:** [PDF](../documents/A05-human-voice-clone-detection.pdf)

**Authors:** Sarah Barrington, Emily A. Cooper, Hany Farid. **Year/venue:** 2025, *Scientific Reports* 15, 11004, published 31 March. **Status:** peer-reviewed journal article.

[Publisher record](https://www.nature.com/articles/s41598-025-94170-3) · [DOI](https://doi.org/10.1038/s41598-025-94170-3) · [Open published PDF](https://www.emilyacooper.org/pubs/2025Barrington_SciRep.pdf)

Separates voice-identity matching from judging whether speech is AI-generated. In the 300-listener authenticity study, mean correctness was 60.8% for generated voices and 67.4% for real voices. A separate 304-listener experiment found clones often sounded like the corresponding person. **Limitation:** stimuli came from 220 US native-English speakers and one commercial cloning service. Controlled listening to selected clips does not reproduce an unexpected interactive call, and recognizing an identity differs from recognizing synthetic speech.

## A06 — Deepfake CAPTCHA: A Method for Preventing Fake Calls

**Collected reading copy:** [PDF](../documents/A06-deepfake-captcha-2023.pdf)

**Authors:** Lior Yasur, Guy Frankovits, Fred M. Grabovski, Yisroel Mirsky. **Year/venue:** 2023, ACM ASIA CCS, 608–622. **Status:** peer-reviewed conference paper; open arXiv copy is the author manuscript.

[Publisher DOI](https://doi.org/10.1145/3579856.3595801) · [Institutional publication record](https://cris.iucc.ac.il/en/publications/deepfake-captcha-a-method-for-preventing-fake-calls-5/) · [Full text](https://arxiv.org/html/2301.03064v1) · [Open PDF](https://arxiv.org/pdf/2301.03064v1)

Presents active caller verification: the caller performs tasks intended to expose limitations of real-time voice conversion, after which models analyze the response. It mainly evaluates audio, with preliminary video work. Unlike conventional image CAPTCHAs, it challenges content generation rather than visual classification. **Limitation:** it requires interaction, can inconvenience callers, and tests particular synthesis systems. This is collected as prior work on live calls, not endorsed as the project's direction or a lasting guarantee.

## A07 — Deep-Fake CAPTCHA: Mitigating Next-Generation Social Engineering Attacks

**Collected reading copy:** [PDF](../documents/A07-deepfake-captcha-2026-preprint.pdf)

**Authors:** Guy Frankovits, Lior Yasur, Fred M. Grabovski, Yisroel Mirsky. **Year/status:** 2026, arXiv:2609.11404v1, submitted 10 September; preprint with no peer-reviewed venue verified.

[Author record](https://arxiv.org/abs/2609.11404) · [Full text](https://arxiv.org/html/2609.11404v1) · [Open PDF](https://arxiv.org/pdf/2609.11404v1)

Expands the earlier D-CAPTCHA research to both audio and video impersonation. Its response assessment combines realism, identity consistency, task completion and response time, with experiments using selected real-time synthesis systems. This makes it relevant literature for calls and video meetings. **Limitation:** it is a very recent extension from the same authors, not an independent replication; effectiveness against future systems or arbitrary communication platforms remains unestablished. It is included as prior work, not a recommendation.

## A08 — STIR/SHAKEN Broadly Implemented Starting Today

**Collected reading copy:** [PDF](../documents/A08-fcc-stir-shaken-scope.pdf)

**Organization:** US Federal Communications Commission. **Date/status:** 30 June 2021, official agency news release; not the technical standard or a Commission order.

[Official document and PDF](https://docs.fcc.gov/public/attachments/DOC-373714A1.pdf)

Explains carrier-level caller-ID authentication and the passage of verified telephone-number information between providers. The FCC explicitly distinguishes improved caller-ID information from assurance that a call is legitimate. This is useful background when assessing what an existing telephone trust mechanism actually verifies. **Limitation:** telephone-number authentication does not establish human-origin speech or exclude voice cloning. The dated announcement should not be used as a statement of current worldwide deployment or regulation.

## Query and access notes

ASVspoof 5 and ADD were carried forward from the team's earlier full-text review; titles, authors and publication status were checked against primary records again. ASVspoof's evaluation metadata was additionally confirmed through IEEE's deposited [Crossref record](https://api.crossref.org/works/10.1109/TASLPRO.2026.3682962). The 2026 volume/pages are published metadata; arXiv v3 is the open accepted manuscript.

New targeted queries:

```text
"Does Audio Deepfake Detection Generalize" "In the Wild" Müller 2022
"Humans cannot reliably detect speech deepfakes"
"People are poorly equipped to detect AI-powered voice clones" paper 2025
"ASVspoof 5: Design, collection and validation" authors
"ASVspoof 5" "101825" Wang authors
```

A01's published PDF, A03–A05 full papers, A08's full release, and the relevant methods/limitations in A02/A06/A07 were read or rechecked. Nature's browser page intermittently rejected retrieval; A05's published author-hosted PDF was read instead. An EURECOM PDF download timed out; the same A01 published paper was successfully retrieved from Fraunhofer. A06's institutional PDF mirror timed out, so its accessible arXiv author version is listed. These access substitutions do not change publication status.

Screened but omitted to keep the collection compact: [Mai et al., *Warning: Humans cannot reliably detect speech deepfakes*, PLOS ONE 2023](https://doi.org/10.1371/journal.pone.0285333). Its English/Mandarin experiment is relevant, but A05 adds more speaker identities and separates identity from authenticity judgments. No datasets or models were downloaded.
