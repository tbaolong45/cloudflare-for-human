# Human and AI content verification: reading collection

Updated **17 September 2026**. A curated scoping review with **41 paraphrased source summaries**, original references and **42 collected full-text files**.

The project investigates a verification layer that can distinguish human-created or human-captured content from AI-generated or AI-manipulated content, and assess human participation in interactions. Meetings, posts, shorts, calls, messages, images and recordings are examples of its intended scope. The scope extends across platforms, devices and communication channels, with privacy, safety and reliability as core concerns.

## Research summary

The literature approaches this problem through media forensics, watermarking, signed provenance, and evidence about people or accounts. These methods establish different things: a statistical indication of synthesis, the presence of an embedded marker, a verifiable record of content history, or an assertion about a participant. NIST's overview provides the clearest starting map of detection, provenance and transparency methods. [NIST AI 100-4](https://doi.org/10.6028/NIST.AI.100-4).

Results depend on what was tested. Studies of circulated media, audio benchmarks and text detectors report sensitivity to unfamiliar generators, data sources, editing and delivery conditions. Their findings warrant careful reading of the evaluated task and limitations, rather than treating a benchmark result as a universal human/AI verdict. [Deepfake-Eval-2024](https://arxiv.org/html/2503.02857v5), [ASVspoof 5 evaluation](https://arxiv.org/html/2601.03944v3), [RAID](https://aclanthology.org/2024.acl-long.674/).

Signed provenance describes an asset's asserted history; personhood credentials concern its participant. Neither, by itself, establishes that a depicted event is true or that every contribution was made without AI assistance. This distinction matters for mixed human/AI content and for separating content origin from safety or honest intent. [C2PA 2.4 security considerations](https://spec.c2pa.org/specifications/specifications/2.4/security/Security_Considerations.html), [personhood credentials paper](https://arxiv.org/html/2408.07892v4).

## Summaries and original documents

Each entry gives the title, authors or issuing body, date and publication status, a short summary, a material limitation, and links to the source and full text. The original abstract is available through the source link.

| Reading collection | What it covers |
| --- | --- |
| [Images, video and audiovisual content](notes/media-detection.md) | Generated images, altered video, partial audio/video edits, circulated media and human judgment; relevant to posts, shorts, recorded meetings and other visual media. |
| [Voice, calls and live interactions](notes/voice-calls.md) | Speech synthesis and voice conversion detection, audio benchmarks, human listening, active caller verification research and caller-number authentication. |
| [Provenance, watermarking and privacy](notes/provenance-identity.md) | Content history, embedded markers, capture and identity evidence, and privacy-preserving participation credentials. |
| [Text, messaging and safety context](notes/integration-evidence.md) | AI-written text, watermarking, mistaken attribution, email authentication, encrypted communication and documented misuse. |
| [CAPTCHA background](notes/captcha-evidence.md) | Automated solving, user burden and accessibility; retained as background to the project's move beyond CAPTCHA. |

**[Open the collected documents](documents/README.md)** for 38 PDFs, four official HTML snapshots and their original download sources. PDFs are papers or official documents; HTML files are snapshots of the linked source, not newly authored reports.

## A short starting sequence

1. **NIST AI 100-4** — an overview of the major technical approaches and their limitations. See the provenance collection.
2. **Deepfake-Eval-2024** — an example of the gap between established benchmark results and selected media circulated in the world. See the media collection.
3. **ASVspoof 5 evaluation** — speech-specific evidence on detection and transfer across datasets. See the voice collection.
4. **C2PA 2.4** — the specification for signed content provenance and the boundaries of its guarantees. See the provenance collection.
5. **RAID** — robustness evidence for generated-text detection across models, domains and attacks. See the text collection.
6. **Personhood credentials** — a conceptual treatment of human participation and privacy, separate from classifying content. See the provenance collection.

The collection labels peer-reviewed papers, preprints, technical reports and standards separately. It is a targeted literature collection, not an exhaustive search or an independently reproduced detector evaluation. [Search and verification method](search-protocol.md).
