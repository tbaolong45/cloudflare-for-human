# Text, messaging, privacy and safety context

Updated 17 September 2026. All summaries below are paraphrased. I01–I04 concern content origin; I05–I06 concern communication guarantees; I07–I09 provide evaluation and documented safety context. These are complementary reading topics, not a prescribed system design.

## I01 — RAID: A Shared Benchmark for Robust Evaluation of Machine-Generated Text Detectors

**Collected reading copy:** [PDF](../documents/I01-raid.pdf)

**Liam Dugan et al. — ACL 2024, pp. 12463–12492. Peer-reviewed conference paper.**

**Summary.** Introduces a benchmark with more than six million generated texts across eleven models, eight domains, eleven attacks and four decoding strategies. Evaluating twelve detectors reveals weaknesses under unfamiliar generators, different sampling settings and adversarial edits. It is useful for studying the reliability of classifications applied to posts, messages and other text. **Limit:** its results describe the included models, domains and attacks; they do not establish performance on every language or very short post.

[Publication and abstract](https://aclanthology.org/2024.acl-long.674/) · [Full paper](https://aclanthology.org/2024.acl-long.674.pdf)

## I02 — GPT detectors are biased against non-native English writers

**Collected reading copy:** [PDF](../documents/I02-text-detector-bias.pdf)

**Weixin Liang, Mert Yuksekgonul, Yining Mao, Eric Wu and James Zou — Patterns 4 (2023), 100779. Peer-reviewed journal article.**

**Summary.** Examines seven detectors using non-native English TOEFL essays and US school essays. The tested systems frequently misclassify the non-native writing as AI-generated; changes to linguistic expression also alter their judgments. This provides evidence of unequal error costs when classifying writing by its statistical style. **Limit:** the study concerns particular 2023 detectors and essay collections, not a measurement of all current tools, populations or social posts.

[Published article](https://doi.org/10.1016/j.patter.2023.100779) · [Open author full text](https://arxiv.org/html/2304.02819v3)

## I03 — Can AI-Generated Text be Reliably Detected? Stress Testing AI Text Detectors Under Various Attacks

**Collected reading copy:** [PDF](../documents/I03-text-detection-attacks.pdf)

**Vinu Sankar Sadasivan, Aounon Kumar, Sriram Balasubramanian, Wenxiao Wang and Soheil Feizi — TMLR 2025; first preprint 2023. Peer-reviewed journal paper; linked author manuscript v4, January 2025.** The linked author manuscript retains the shorter title.

**Summary.** Tests how repeated paraphrasing affects several detection approaches, including classifiers, watermarks and retrieval. It also examines attacks that cause human-written material to look watermarked and develops a theoretical relationship between detection and differences in human/model text distributions. **Limit:** the experiments and theorem have specified settings and assumptions; they do not prove that every text detector must fail on every task.

[Published venue record](https://openreview.net/forum?id=OOgsAZdFOt) · [Author record and abstract](https://arxiv.org/abs/2303.11156) · [Full author text](https://arxiv.org/html/2303.11156v4)

## I04 — Scalable watermarking for identifying large language model outputs

**Collected reading copy:** [PDF](../documents/I04-synthid-text.pdf)

**Sumanth Dathathri et al. — Nature 634 (2024), 818–823. Peer-reviewed journal article, published 23 October 2024.**

**Summary.** Introduces SynthID-Text, which changes token selection during generation to embed a detectable statistical marker. The authors evaluate detection and quality, including user feedback on nearly twenty million Gemini responses. This is evidence that a cooperating provider can apply text watermarking at substantial scale. **Limit:** that production experiment assesses quality, not universal detection accuracy. Unmarked generators remain outside its coverage, and editing or paraphrasing can weaken the marker.

[Publication, abstract and full text](https://www.nature.com/articles/s41586-024-08025-4) · [Publisher PDF](https://www.nature.com/articles/s41586-024-08025-4.pdf)

## I05 — Domain-Based Message Authentication, Reporting, and Conformance (DMARC)

**Collected reading copy:** [PDF](../documents/I05-dmarc.pdf)

**Todd M. Herr and John Levine, editors — IETF RFC 9989, May 2026. Standards Track, Proposed Standard; obsoletes RFCs 7489 and 9091.**

**Summary.** Specifies how receiving mail systems assess whether an email's author domain aligns with authenticated domain information and how domain owners express handling preferences. It is relevant when comparing content verification with existing sender-authentication infrastructure. **Limit:** domain authorization says nothing about whether a human composed the message, whether its statements are true, or whether a sender is honest. Display-name deception and content analysis are outside its scope.

[Official specification](https://www.rfc-editor.org/rfc/rfc9989.html)

## I06 — The Messaging Layer Security (MLS) Protocol

**Collected reading copy:** [PDF](../documents/I06-messaging-layer-security.pdf)

**Richard Barnes et al. — IETF RFC 9420, July 2023. Standards Track, Proposed Standard.**

**Summary.** Defines a protocol for encrypted group communication, including changes in membership, protection of past messages and recovery after some compromises. It supplies background for the privacy question: a delivery service need not receive the plaintext of conversations. **Limit:** encryption and protocol authentication do not establish human authorship, media originality or truthful speech. The specification also does not imply that every meeting or messaging application implements MLS.

[Official specification](https://www.rfc-editor.org/rfc/rfc9420.html)

## I07 — Dos and Don'ts of Machine Learning in Computer Security

**Collected reading copy:** [PDF](../documents/I07-security-ml-evaluation.pdf)

**Daniel Arp et al. — USENIX Security 2022, pp. 3971–3988. Peer-reviewed conference paper.**

**Summary.** Analyzes recurring methodological errors in security machine learning, including unrepresentative data, information leakage, misleading evaluation and overlooked adversaries. It helps readers judge whether a reported human/AI detector result supports the claimed use. **Limit:** this is cross-domain methodological work, not an empirical evaluation of this project's proposed layer or a ranking of current deepfake detectors.

[Publication and abstract](https://www.usenix.org/conference/usenixsecurity22/presentation/arp) · [Venue PDF](https://www.usenix.org/system/files/sec22-arp.pdf) · [Author copy](https://www.mlsec.org/docs/2022-sec.pdf)

## I08 — Alert on Fraud Schemes Involving Deepfake Media Targeting Financial Institutions

**Collected reading copy:** [PDF](../documents/I08-fincen-deepfake-alert.pdf)

**FinCEN — FIN-2024-Alert004, 13 November 2024. Official operational advisory.**

**Summary.** Describes reported use of synthetic or altered identity documents, images and other media to impersonate people and circumvent verification. It discusses suspicious patterns and investigative indicators based on reporting and agency information. This is a documented application of the broader privacy and safety problem. **Limit:** an advisory is not a controlled detector study, and its observations do not provide a global prevalence estimate or establish that all AI-generated content is fraudulent.

[Official full document](https://www.fincen.gov/system/files/shared/FinCEN-Alert-DeepFakes-Alert508FINAL.pdf)

## I09 — LCQ9: Combating frauds involving deepfake

**Collected reading copy:** [Official HTML snapshot](../documents/I09-deepfake-meeting-case.html)

**Hong Kong Government — official legislative response, 26 June 2024. Primary incident account.**

**Summary.** Describes a January 2024 case involving approximately HK$200 million and a fabricated video conference followed by payment instructions through messaging. The response specifically describes prerecorded material with no interaction during the fabricated conference. It supplies a primary source for investigating meeting-related impersonation. **Limit:** this case does not demonstrate a fully interactive real-time deepfake meeting or measure how common such attacks are.

[Official response, reply (1)](https://www.info.gov.hk/gia/general/202406/26/P2024062600192.htm)

## Access and search notes

Primary records and the relevant source text were inspected. The Liang publisher endpoint was unavailable; its open author manuscript supplied the findings. Sadasivan's arXiv version has the shorter title and identifies publication in TMLR; publication-year metadata was cross-checked against the venue and current author record during the initial review. The Hong Kong source was read during the initial review; after a subsequent browser timeout, its official HTML was downloaded and the incident details rechecked. The TMLR venue page presented a browser challenge, so the accessible author manuscript remains the reading copy. Local download outcomes are recorded in the document index.

Additional executed queries on 17 September 2026:

- `RAID Shared Benchmark Robust Evaluation Machine Generated Text Detectors ACL 2024 paper`
- `Scalable watermarking for identifying large language model outputs Nature 2024 SynthID Text paper`
- `"Stress Testing AI Text Detectors" "TMLR" "2025"` (restricted to OpenReview/arXiv; no search results; the existing primary author record was opened directly).

<details>
<summary>Initial parent search log, 16 September 2026</summary>

1. `site.fincen.gov deepfake media fraud financial institutions alert 2024`
2. `site.fcc.gov STIR SHAKEN caller ID authentication does not stop scam calls`
3. `site.cloudflare.com turnstile bot management detection signals documentation`
4. `site.nist.gov 800-63B-4 phishing resistant authentication biometrics deepfake`
5. `site.nist.gov adversarial machine learning synthetic content NIST AI 100-4 2024`
6. `site.rfc-editor.org RFC DMARC authentication content legitimacy`
7. `site.usenix.org fraud detection base rate fallacy intrusion detection Axelsson`
8. `site.police.gov.hk deepfake 200 million video conference 2024`
9. `site.w3.org TR secure payment confirmation transaction payee amount authentication 2026`
10. `site.pnas.org GPT detectors biased non native English writers Liang 2023`
11. `site.arxiv.org Can AI-Generated Text be Reliably Detected Sadasivan 2023`
12. `credit card fraud detection realistic modeling novel learning strategy Dal Pozzolo 2018 primary paper`
13. `"Credit Card Fraud Detection: A Realistic Modeling" "pdf"`
14. `"The base-rate fallacy" "Axelsson" "10.1145"`
15. `site.usenix.org "Dos and Don'ts of Machine Learning" security`
16. `"Can AI-Generated Text be Reliably Detected" "TMLR" 2024`
17. `"10.1109/TNNLS.2017.2736643" 2018 3784`

These queries include adjacent material considered during screening. A search hit is not itself evidence or an included source.

</details>
