# CAPTCHA: historical background documents

Checked 17 September 2026. These three sources provide background on distinguishing automated access from human activity. They are not proposed solutions for determining whether calls, meetings, posts or other media contain AI-generated/manipulated content. Active caller-verification research is collected separately in [voice-calls.md](voice-calls.md).

## C01 — Breaking reCAPTCHAv2

**Collected reading copy:** [PDF](../documents/C01-breaking-recaptchav2.pdf)

**Authors:** Andreas Plesner, Tobias Vontobel, Roger Wattenhofer. **Year/venue:** 2024, IEEE COMPSAC, 1047–1056. **Status:** peer-reviewed conference paper; the linked arXiv copy is the author manuscript.

[Publisher DOI](https://doi.org/10.1109/COMPSAC61105.2024.00142) · [Full text](https://arxiv.org/html/2409.08831v1) · [Open PDF](https://arxiv.org/pdf/2409.08831v1)

Studies automated image-challenge solving using a vision model and browser automation. One demo-site experiment completed all 100 sessions with changing IP addresses and repeated challenges. The paper also examines how browser history and interaction signals affect completion. **Limitation:** this is eventual session completion in a particular environment, not perfect first-attempt recognition or evidence that every deployed CAPTCHA is defeated. It addresses automated access, not media authenticity.

## C02 — An Empirical Study & Evaluation of Modern CAPTCHAs

**Collected reading copy:** [PDF](../documents/C02-modern-captcha-evaluation.pdf)

**Authors:** Andrew Searles, Yoshimichi Nakatsuka, Ercan Ozturk, Andrew Paverd, Gene Tsudik, Ai Enkoji. **Year/venue:** 2023, USENIX Security, 3081–3097. **Status:** peer-reviewed conference paper.

[Official record](https://www.usenix.org/conference/usenixsecurity23/presentation/searles) · [Open PDF](https://www.usenix.org/system/files/usenixsecurity23-searles.pdf)

Examines modern CAPTCHA use, completion times, preferences, task context and abandonment. Its studies include 1,400 completers and 14,000 challenges across the main and follow-up experiments. The findings show that user burden cannot be described by accuracy or solving time alone. **Limitation:** its comparison with automated solvers draws on earlier papers rather than one matched human-versus-bot experiment. It does not evaluate AI-generated media identification.

## C03 — Inaccessibility of CAPTCHA: Alternatives to Visual Turing Tests on the Web

**Collected reading copy:** [Official HTML snapshot](../documents/C03-captcha-accessibility.html)

**Organization/editors:** W3C; Scott Hollier, Janina Sajka, Jason White, Michael Cooper. **Year:** 2021, 16 December version. **Status:** W3C Group Draft Note; not a W3C Recommendation or normative compliance standard.

[Official full document](https://www.w3.org/TR/2021/DNOTE-turingtest-20211216/)

Reviews accessibility barriers in visual, audio and other CAPTCHA formats, including human/avatar image comparison. It also discusses human-solving relay services and alternatives to conventional puzzles. The document explains why completing a challenge cannot exclude every form of abuse and why offering audio does not accommodate all disabilities. **Limitation:** this is accessibility and security guidance, not a current empirical detector benchmark or a standard for verifying media origin.

## Access notes

Primary full texts were read in the earlier review and retained after the scope correction. C01's COMPSAC publication was verified through the manuscript acceptance footnote and IEEE-deposited Crossref metadata, DOI `10.1109/COMPSAC61105.2024.00142`. C02 uses official USENIX proceedings; C03 uses W3C's dated document. C03 is an HTML document; an official-page snapshot is included in the collected documents.

Relevant discovery queries retained from the earlier search: `Breaking reCAPTCHAv2 100% automated solving 2024 arxiv Plesner`; `"Breaking reCAPTCHAv2" "COMPSAC"`; `"An Empirical Study" "CAPTCHAs" 2023 Searles Tsudik`; `W3C CAPTCHA accessibility limitations Turing tests note`.
