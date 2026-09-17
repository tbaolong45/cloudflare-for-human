# Provenance, watermarking and adjacent personhood: reading collection

Reviewed **16–17 September 2026**. These ten readings cover media relevant to meetings, posts, short videos, calls and similar settings. This is a targeted collection, not an exhaustive systematic review. Summaries are paraphrased; publication status and limitations are stated separately. Long author lists are abbreviated with “et al.”; linked publication records provide the complete lists.

The central distinction is between evidence about **media origin/history**, **the people using a service**, and **the truth of a depicted event**. None implies the others. Missing provenance or a missing watermark is inconclusive: content may never have been marked, or its evidence may have been removed. Human-made media can also mislead. These distinctions follow from NIST’s synthesis and C2PA’s trust model, rather than from an evaluated system built for this project. [NIST AI 100-4](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-4.pdf), [C2PA 2.4](https://spec.c2pa.org/specifications/specifications/2.4/specs/C2PA_Specification.html).

## Media provenance and watermarking

### P01 — Reducing Risks Posed by Synthetic Content: An Overview of Technical Approaches to Digital Content Transparency

**Collected reading copy:** [PDF](../documents/P01-nist-synthetic-content.pdf)

**Authors:** Bilva Chandra, Jesse Dunietz, Kathleen Roberts, Yooyoung Lee, Peter Fontana, George Awad. **Year/status:** 2024; final NIST AI 100-4 technical report, November. The publication webpage’s April 2026 update does not change the report’s publication year.

[Publication record](https://www.nist.gov/publications/reducing-risks-posed-synthetic-content-overview-technical-approaches-digital-content) · [Full PDF](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-4.pdf) · [DOI](https://doi.org/10.6028/NIST.AI.100-4)

**Summary:** NIST organizes digital-content transparency into provenance tracking, watermarking and synthetic-content detection across images, audio, video and text. It explains how the approaches work, where they overlap, and how evaluation depends on the intended use. This is a useful starting point for understanding why recognizing synthetic content, recovering its history and judging its trustworthiness are different tasks.

**Limitation:** A technical synthesis, not a current detector leaderboard. It documents missing markers, removal and spoofing; no single approach provides comprehensive protection.

### P02 — Content Credentials: C2PA Technical Specification, version 2.4

**Collected reading copy:** [Official HTML snapshot](../documents/P02-c2pa-specification-2.4.html) · [Security document (HTML)](../documents/P02-c2pa-security-2.4.html)

**Author:** Coalition for Content Provenance and Authenticity. **Year/status:** 2026; published industry technical specification, April; companion security considerations of the same version.

[Official full specification](https://spec.c2pa.org/specifications/specifications/2.4/specs/C2PA_Specification.html) · [Security considerations](https://spec.c2pa.org/specifications/specifications/2.4/security/Security_Considerations.html)

**Summary:** C2PA specifies signed manifests describing content and its processing history, with cryptographic bindings that allow validators to detect certain changes. Its scope includes AI-related disclosures and live-video provisions. The trust model separates checking a signature and content integrity from deciding whether a signer or assertion should be trusted. This is the primary reading for understanding Content Credentials.

**Limitation:** A valid manifest does not establish factual truth or complete disclosure. The threat model includes stripping, stolen keys and compromised inputs before signing; absent credentials establish neither human nor AI origin.

### P03 — Watermark Anything with Localized Messages

**Collected reading copy:** [PDF](../documents/P03-watermark-anything.pdf)

**Authors:** Tom Sander, Pierre Fernandez, Alain Durmus, Teddy Furon, Matthijs Douze. **Year/status:** 2025; peer-reviewed ICLR paper. An updated arXiv version appeared on 22 July 2025.

[Publication record](https://arxiv.org/abs/2411.07231) · [ICLR full PDF](https://proceedings.iclr.cc/paper_files/paper/2025/file/c5ee1911dffe4886367eee7fca314235-Paper-Conference.pdf) · [Updated full text](https://arxiv.org/html/2411.07231v2)

**Summary:** Watermark Anything treats extraction as image segmentation, locating marked regions and recovering messages from them. It can handle composite images containing different watermarked sources, making it relevant to posts mixing generated and captured material. The paper evaluates extraction, localization and visual quality under image transformations, showing why identifying an edited region can be more informative than labeling an entire image.

**Limitation:** It detects deliberately embedded marks, not arbitrary AI images. Payload capacity, visible artifacts and combined transformations constrain results; the updated version includes post-review experiments.

### P04 — SynthID-Image: Image watermarking at internet scale

**Collected reading copy:** [PDF](../documents/P04-synthid-image.pdf)

**Authors:** Sven Gowal, Rudy Bunel, Florian Stimberg, David Stutz, Guillermo Ortiz-Jimenez, et al. **Year/status:** 2025; Google-authored technical preprint, arXiv v1, 10 October; no peer-reviewed venue identified in the checked record.

[Publication record](https://arxiv.org/abs/2510.09263) · [Full PDF](https://arxiv.org/pdf/2510.09263) · [Full HTML](https://arxiv.org/html/2510.09263v1)

**Summary:** The paper describes an image-watermarking system and separates mark detection, message recovery, perceptual quality and security. It evaluates an external variant, SynthID-O, against other post-processing watermark methods and discusses calibration and attacker access. Its practical contribution is a detailed account of the tradeoffs involved in marking large volumes of images and detecting those marks after subsequent transformations.

**Limitation:** Vendor-reported deployment is not independent effectiveness evidence. The threat model emphasizes making black-box attacks costly; it does not promise resistance to every white-box adversary or recognition of unmarked media.

### P05 — Invisible Image Watermarks Are Provably Removable Using Generative AI

**Collected reading copy:** [PDF](../documents/P05-watermark-removal.pdf)

**Authors:** Xuandong Zhao, Kexun Zhang, Zihao Su, Saastha Vasan, Ilya Grishchenko, Christopher Kruegel, Giovanni Vigna, Yu-Xiang Wang, Lei Li. **Year/status:** 2024; peer-reviewed NeurIPS paper.

[Proceedings record](https://proceedings.nips.cc/paper_files/paper/2024/hash/10272bfd0371ef960ec557ed6c866058-Abstract-Conference.html) · [Full PDF](https://proceedings.neurips.cc/paper_files/paper/2024/file/10272bfd0371ef960ec557ed6c866058-Paper-Conference.pdf) · [DOI](https://doi.org/10.52202/079017-0276)

**Summary:** This paper studies regeneration attacks that add noise and reconstruct an image to weaken an invisible watermark. It combines formal bounds for specified watermark and denoising assumptions with experiments on four schemes. It is a useful counterweight to watermarking proposals because it examines whether useful visual content can survive even when the identifying signal becomes difficult to recover.

**Limitation:** The result is conditional, particularly on pixel-level perturbations and reconstruction quality. Its title should not be generalized into proof that every possible watermark or later production system fails.

### P06 — Proactive Detection of Voice Cloning with Localized Watermarking

**Collected reading copy:** [PDF](../documents/P06-audioseal.pdf)

**Authors:** Robin San Roman, Pierre Fernandez, Hady Elsahar, Alexandre Défossez, Teddy Furon, Tuan Tran, in published proceedings order. **Year/status:** 2024; peer-reviewed ICML paper, PMLR 235, pp. 43180–43196. Method: **AudioSeal**.

[Proceedings record](https://proceedings.mlr.press/v235/san-roman24a.html) · [Full PDF, arXiv v2](https://arxiv.org/pdf/2401.17264v2) · [Full HTML](https://arxiv.org/html/2401.17264v2)

**Summary:** AudioSeal jointly trains an audio-watermark generator and detector to identify marked speech segments, including small portions embedded in a longer recording. A perceptual objective limits audible changes, while training transformations improve robustness to common edits. This is relevant to voice messages, calls and meeting recordings because it addresses where marked audio occurs, rather than only classifying an entire recording.

**Limitation:** It covers deliberately marked audio. Its own adversarial evaluation finds effective removal with detector access, leading the authors to recommend keeping detector weights private; benchmark performance is not a guarantee for every call pipeline.

### P07 — Video Seal: Open and Efficient Video Watermarking

**Collected reading copy:** [PDF](../documents/P07-video-seal.pdf)

**Authors:** Pierre Fernandez, Hady Elsahar, I. Zeki Yalniz, Alexandre Mourachko. **Year/status:** 2024; technical preprint, arXiv v1, 12 December. The current author publication page and Meta record still identify it as an arXiv publication; no peer-reviewed venue was identified in the checked records.

[Publication record](https://arxiv.org/abs/2412.09492) · [Full PDF](https://arxiv.org/pdf/2412.09492) · [Full HTML](https://arxiv.org/html/2412.09492v1) · [Author’s publication record](https://pierrefdz.github.io/publications/videoseal/)

**Summary:** Video Seal embeds and extracts messages in video while addressing compression, geometric edits and processing cost. It combines image/video training with temporal propagation, reusing a watermark across nearby frames to reduce computation. The paper is particularly relevant to short videos and recorded meetings because video processing introduces temporal and compression tradeoffs that an image-only watermark evaluation cannot fully characterize.

**Limitation:** It recognizes its embedded marks, not all manipulated videos. Reusing marks across frames can produce motion artifacts and extraction errors; evidence is limited to the paper’s evaluated settings.

## Adjacent readings: people, privacy and capture integrity

These address who participates or how evidence is captured. They are not substitutes for detecting AI-generated media.

### P08 — Personhood credentials: Artificial intelligence and the value of privacy-preserving tools to distinguish who is real online

**Collected reading copy:** [PDF](../documents/P08-personhood-credentials.pdf)

**Authors:** Steven Adler, Zoë Hitzig, Shrey Jain, et al. **Year/status:** 2024; conceptual/position preprint, first 15 August. Latest checked version: arXiv v4, 17 January 2025.

[Publication record](https://arxiv.org/abs/2408.07892) · [Full PDF, v4](https://arxiv.org/pdf/2408.07892v4) · [Full HTML](https://arxiv.org/html/2408.07892v4)

**Summary:** The authors describe credentials intended to show that an account is backed by a person while limiting disclosure of identifying information. The proposed combination is one credential per person per issuer and unlinkable use across services. It helps clarify the difference between restricting mass automated participation and determining whether a particular post, voice or image was produced using AI.

**Limitation:** This is a proposal, not demonstrated universal personhood verification. Lending, theft, exclusion and issuer concentration remain concerns; human-backed credentials do not imply human-authored content or honest behavior.

### P09 — The Privacy Pass Architecture

**Collected reading copy:** [PDF](../documents/P09-privacy-pass-architecture.pdf)

**Authors:** Alex Davidson, Jana Iyengar, Christopher A. Wood. **Year/status:** 2024; IETF **Informational RFC 9576**, June; not Standards Track.

[Official full text](https://www.rfc-editor.org/rfc/rfc9576.html) · [Full PDF](https://www.rfc-editor.org/rfc/rfc9576.pdf) · [DOI](https://doi.org/10.17487/RFC9576)

**Summary:** Privacy Pass separates the service requesting evidence, the party evaluating a client, the token issuer and the client presenting a token. Its goal is to authorize access while reducing the ability to link token issuance and redemption. It is a useful privacy reading when verification requires repeatedly presenting evidence about a device, account or person without exposing the underlying evaluation each time.

**Limitation:** A token’s meaning depends on the attestation policy; it does not inherently prove human presence or media origin. Privacy depends on deployment roles, collusion assumptions and timing or network side channels.

### P10 — Digital Identity Guidelines: Identity Proofing and Enrollment

**Collected reading copy:** [PDF](../documents/P10-nist-identity-proofing.pdf)

**Authors:** David Temoshok, Christine Abruzzi, Yee-Yin Choong, James L. Fenton, Ryan Galluzzo, Connie LaSalle, Naomi Lefkovitz, Andrew Regenscheid, Maria Vachino. **Year/status:** 2025; final NIST SP 800-63A-4 guideline, July.

[Official full HTML](https://pages.nist.gov/800-63-4/sp800-63a.html) · [Full PDF](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-63A-4.pdf) · [DOI](https://doi.org/10.6028/NIST.SP.800-63A-4)

**Summary:** This guideline concerns establishing a person’s identity, with a particularly relevant discussion of forged-media injection in §3.14. It distinguishes attacks on a physical presentation from attacks that replace or alter digital evidence between capture and verification. For live video or voice contexts, it explains why matching a face or evaluating apparent liveness leaves important questions about the capture pipeline unresolved.

**Limitation:** Its requirements concern identity proofing, not a universal detector for meetings, posts or clips. Biometric matching and presentation-attack detection alone do not address all injected synthetic evidence.

## Search and access notes

The following exact queries were executed on 16 September 2026 during the wider source review. Some found adjacent readings not retained in this shorter collection. Query wording is not evidence: the verified venue for Watermark Anything is **ICLR**, despite the original query saying ICML.

```text
site.c2pa.org specifications 2.4 2.3 latest technical specification 2026
site.rfc-editor.org RFC 9576 Privacy Pass architecture 9577 9578
personhood credentials artificial intelligence digital authenticity privacy anonymity 2024 paper
site.nist.gov reducing risks posed by synthetic content NIST AI 100-4
site.w3.org TR webauthn-3 2026 candidate recommendation user presence verification
site.nist.gov SP 800-63-4 2025 identity proofing authentication biometrics presentation attack detection
Watermark Anything localized image watermarking ICML 2025 paper
SynthID image video watermarking paper 2025 2026 robustness
site.usenix.org watermark image removal forgery 2025 UnMarker
site.proceedings.neurips.cc 2024 watermark image regeneration attacks
site.arxiv.org "Verifying Provenance of Digital Media" C2PA 2026
```

Additional exact queries on 17 September 2026:

```text
site.proceedings.mlr.press "Proactive Detection of Voice Cloning"
"Video Seal" "Video Watermarking" paper 2025
"Video Seal: Open and Efficient Video Watermarking" conference 2025 2026
```

Official records and full texts were checked directly. Relevant sections read included C2PA scope, version history, trust and threats; WAM method and limitations; SynthID threat models and limitations; watermark-removal assumptions; AudioSeal methods, adversarial removal and robustness; Video Seal temporal propagation; PHC requirements and credential-transfer risks; Privacy Pass roles and privacy; and NIST A-4 §3.14. NIST AI 100-4 was read selectively for taxonomy and limitations.

C2PA’s HTML specification was accessible; an attempted PDF URL failed in the browsing tool, so the collection uses official HTML. The AudioSeal proceedings PDF link also failed there; its complete arXiv v2 HTML was read and its corresponding PDF is supplied. No attacks were reproduced and no vendor effectiveness claim was independently audited. Confidence is high in the bibliographic facts and described scopes, but performance outside each paper’s evaluation remains unestablished by this collection.
