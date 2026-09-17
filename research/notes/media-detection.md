# Image and video authenticity: annotated reading collection

Checked 17 September 2026. Eleven papers on captured, AI-generated and partially manipulated media: general images, processed clips, audiovisual recordings and human judgment. Publication status and open full-text versions are identified separately.

## M01 — CNN-Generated Images Are Surprisingly Easy to Spot... for Now

**Collected reading copy:** [PDF](../documents/M01-cnn-generated-images.pdf)

**Authors:** Sheng-Yu Wang, Oliver Wang, Richard Zhang, Andrew Owens, and Alexei A. Efros.  
**Publication:** 2020 — CVPR, pp. 8695–8704. Peer-reviewed conference paper.

[Source record](https://openaccess.thecvf.com/content_CVPR_2020/papers/Wang_CNN-Generated_Images_Are_Surprisingly_Easy_to_Spot..._for_Now_CVPR_2020_paper.pdf) · [Open proceedings PDF](https://openaccess.thecvf.com/content_CVPR_2020/papers/Wang_CNN-Generated_Images_Are_Surprisingly_Easy_to_Spot..._for_Now_CVPR_2020_paper.pdf)

Tests whether a detector trained on images from one generator can recognize images produced by other generators. Training on ProGAN with suitable augmentation transferred to several contemporary CNN synthesis methods. The paper also examines JPEG compression, blur and resizing, making it relevant to processed or reposted images. Its central limitation is historical scope: these results concern the generators tested in 2020 and do not establish equivalent performance on later diffusion models.

## M02 — Towards Universal Fake Image Detectors That Generalize Across Generative Models

**Collected reading copy:** [PDF](../documents/M02-universal-fake-image-detectors.pdf)

**Authors:** Utkarsh Ojha, Yuheng Li, and Yong Jae Lee.  
**Publication:** 2023 — CVPR, pp. 24480–24489. Peer-reviewed conference paper.

[Source record](https://openaccess.thecvf.com/content/CVPR2023/html/Ojha_Towards_Universal_Fake_Image_Detectors_That_Generalize_Across_Generative_Models_CVPR_2023_paper.html) · [Open proceedings PDF](https://openaccess.thecvf.com/content/CVPR2023/papers/Ojha_Towards_Universal_Fake_Image_Detectors_That_Generalize_Across_Generative_Models_CVPR_2023_paper.pdf)

Investigates why image detectors trained on GAN outputs can mistake unfamiliar synthetic images for real photographs. Simple classifiers using frozen pretrained visual representations transfer better to the tested diffusion and autoregressive generators than several directly trained detectors. The study covers varied image content beyond face swaps. However, generalization is demonstrated only for the evaluated models and datasets; “universal” in the title does not mean every future generator is detectable.

## M03 — Fake or JPEG? Revealing Common Biases in Generated Image Detection Datasets

**Collected reading copy:** [PDF](../documents/M03-fake-or-jpeg.pdf)

**Authors:** Patrick Grommelt, Louis Weiss, Franz-Josef Pfreundt, and Janis Keuper.  
**Publication:** 2025 — Computer Vision – ECCV 2024 Workshops, Part XXII, pp. 80–95. Published workshop paper; the open author version is from March 2024.

[Source record](https://doi.org/10.1007/978-3-031-92089-9_6) · [Open author-version PDF](https://arxiv.org/pdf/2403.17608v2)

Shows how JPEG compression and image dimensions can unintentionally reveal dataset labels, allowing a detector to learn collection differences instead of synthesis traces. Experiments on GenImage change substantially when these differences are controlled. This is particularly relevant to images resized or recompressed before posting. The analysis concentrates on ResNet50 and Swin-T baselines, so it demonstrates a concrete confound rather than proving that every detector relies on the same shortcut.

## M04 — A Sanity Check for AI-generated Image Detection

**Collected reading copy:** [PDF](../documents/M04-chameleon-image-detection.pdf)

**Authors:** Shilin Yan, Ouxiang Li, Jiayin Cai, Yanbin Hao, Xiaolong Jiang, Yao Hu, and Weidi Xie.  
**Publication:** 2025 — ICLR. Peer-reviewed conference paper.

[Source record](https://proceedings.iclr.cc/paper_files/paper/2025/hash/b0303773962ea1b5394c3a83cc7dd066-Abstract-Conference.html) · [Open proceedings PDF](https://proceedings.iclr.cc/paper_files/paper/2025/file/b0303773962ea1b5394c3a83cc7dd066-Paper-Conference.pdf)

Introduces Chameleon, containing photographs and highly realistic generated images of people, animals, objects and scenes. Generated examples were retained when two annotators independently mistook them for real photographs. Existing detectors frequently missed these examples; the proposed AIDE method combines semantic and image-noise features and improves the benchmark results. Because difficult examples were deliberately selected, this collection does not estimate average human or machine accuracy across all images.

## M05 — DF40: Toward Next-Generation Deepfake Detection

**Collected reading copy:** [PDF](../documents/M05-df40.pdf)

**Authors:** Zhiyuan Yan, Taiping Yao, Shen Chen, Yandan Zhao, Xinghe Fu, Junwei Zhu, Donghao Luo, Chengjie Wang, Shouhong Ding, Yunsheng Wu, and Li Yuan.  
**Publication:** 2024 — NeurIPS Datasets and Benchmarks Track. Peer-reviewed conference paper.

[Source record](https://proceedings.nips.cc/paper_files/paper/2024/hash/34239f60eca7ce9bee5280aaf81362d8-Abstract-Datasets_and_Benchmarks_Track.html) · [Open proceedings PDF](https://proceedings.nips.cc/paper_files/paper/2024/file/34239f60eca7ce9bee5280aaf81362d8-Paper-Datasets_and_Benchmarks_Track.pdf)

Combines 40 forgery techniques and evaluates eight detectors under protocols that distinguish changes in manipulation method from changes in source data. Results show that success on familiar face-forgery benchmarks need not transfer to other edits or whole-image synthesis. Localized edits and entirely generated images present different detection problems. The paper acknowledges limited comprehensive evaluation of video-level detectors, so its findings do not establish performance across full temporal or audiovisual content.

## M06 — Deepfake-Eval-2024: A Multi-Modal In-the-Wild Benchmark of Deepfakes Circulated in 2024

**Collected reading copy:** [PDF](../documents/M06-deepfake-eval-2024.pdf)

**Authors:** Nuria Alina Chandra, Hannah Lee, Ryan Murtfeldt, Lin Qiu, Arnab Karmakar, Emmanuel Tanumihardja, Kevin Farhat, Ben Caffee, Changyeon Lee, Jongwook Choi, Sejin Paik, Aerin Kim, and Oren Etzioni.  
**Publication:** 2026 — CVPR Workshops, pp. 10668–10678. Published workshop paper; first preprint appeared in March 2025.

[Source record](https://openaccess.thecvf.com/content/CVPR2026W/APAI/html/Chandra_Deepfake-Eval-2024_A_Multi-Modal_In-the-Wild_Benchmark_of_Deepfakes_Circulated_in_2024_CVPRW_2026_paper.html) · [Open proceedings PDF](https://openaccess.thecvf.com/content/CVPR2026W/APAI/papers/Chandra_Deepfake-Eval-2024_A_Multi-Modal_In-the-Wild_Benchmark_of_Deepfakes_Circulated_in_2024_CVPRW_2026_paper.pdf)

Evaluates image, video and audio detectors on suspicious material submitted from actual online circulation. Several off-the-shelf systems perform worse across these different datasets: Table 3 contrasts UFD’s 0.94 AUROC on prior benchmarks with 0.56 here. AUROC measures ranking rather than accuracy. The collection is selective, visual items require faces, and some audio labels consult detectors. These restrictions, alongside internal inconsistencies in headline statistics, limit broad claims about all media.

## M07 — AV-Deepfake1M: A Large-Scale LLM-Driven Audio-Visual Deepfake Dataset

**Collected reading copy:** [PDF](../documents/M07-av-deepfake1m.pdf)

**Authors:** Zhixi Cai, Shreya Ghosh, Aman Pankaj Adatia, Munawar Hayat, Abhinav Dhall, Tom Gedeon, and Kalin Stefanov.  
**Publication:** 2024 — ACM International Conference on Multimedia. Peer-reviewed conference paper; first preprint appeared in 2023.

[Source record](https://doi.org/10.1145/3664647.3680795) · [Open accepted-author PDF](https://arxiv.org/pdf/2311.15308v2)

Builds more than one million audiovisual clips with changes to audio, video or both. Its generation process inserts, deletes or replaces content, including short manipulated segments inside otherwise authentic recordings. The benchmark distinguishes deciding whether a clip is altered from locating the altered interval. This directly addresses mixed human-recorded and AI-manipulated products. Its source footage and generation pipelines are curated, limiting extrapolation to arbitrary recordings or live conversations.

## M08 — AVFF: Audio-Visual Feature Fusion for Video Deepfake Detection

**Collected reading copy:** [PDF](../documents/M08-avff.pdf)

**Authors:** Trevine Oorloff, Surya Koppisetti, Nicolò Bonettini, Divyaraj Solanki, Ben Colman, Yaser Yacoob, Ali Shahriyari, and Gaurav Bharaj.  
**Publication:** 2024 — CVPR, pp. 27102–27112. Peer-reviewed conference paper.

[Source record](https://openaccess.thecvf.com/content/CVPR2024/html/Oorloff_AVFF_Audio-Visual_Feature_Fusion_for_Video_Deepfake_Detection_CVPR_2024_paper.html) · [Open proceedings PDF](https://openaccess.thecvf.com/content/CVPR2024/papers/Oorloff_AVFF_Audio-Visual_Feature_Fusion_for_Video_Deepfake_Detection_CVPR_2024_paper.pdf)

Learns relationships between speech audio and facial motion from real videos, then uses those representations to classify manipulated clips. On a 70/30 FakeAVCeleb split, it reports 99.1% AUROC, which measures ranking performance rather than classification accuracy. The work illustrates the value of audiovisual correspondence. However, its visual-only and audiovisual comparison rows use different fake-label definitions, so that table alone cannot establish the causal benefit of adding audio.

## M09 — AV-Deepfake1M++: A Large-Scale Audio-Visual Deepfake Benchmark with Real-World Perturbations

**Collected reading copy:** [PDF](../documents/M09-av-deepfake1m-plus.pdf)

**Authors:** Zhixi Cai, Kartik Kuckreja, Shreya Ghosh, Akanksha Chuchra, Muhammad Haris Khan, Usman Tariq, Tom Gedeon, and Abhinav Dhall.  
**Publication:** 2025 — arXiv:2507.20579, technical report/preprint. A peer-reviewed publication was not verified.

[Source record](https://arxiv.org/abs/2507.20579) · [Open preprint PDF](https://arxiv.org/pdf/2507.20579v1)

Expands AV-Deepfake1M to roughly two million clips, additional recording sources and newer audio/video generators. It adds distortions associated with redistribution and transmission, including compression, blur, frame disturbances and audio degradation. This makes the work relevant to processed short clips and recorded conversations, including partially altered content. The distortions are simulated, however, and the technical report does not demonstrate performance across every actual platform or recording environment.

## M10 — Deepfake detection by human crowds, machines, and machine-informed crowds

**Collected reading copy:** [PDF](../documents/M10-human-machine-deepfake-judgment.pdf)

**Authors:** Matthew Groh, Ziv Epstein, Chaz Firestone, and Rosalind Picard.  
**Publication:** 2022 — Proceedings of the National Academy of Sciences 119(1), e2110013119. Peer-reviewed journal article; published online 28 December 2021.

[Source record](https://doi.org/10.1073/pnas.2110013119) · [Open published PDF, author-hosted](https://mattgroh.com/pdfs/detect-fakes-comparing-human-machine.pdf)

Two online studies involving 15,016 participants compare human judgments, aggregated judgments and a leading contemporary detector on authentic and manipulated videos. Humans and the model make different mistakes. Showing model predictions improves judgments on average, but wrong predictions can mislead viewers into abandoning correct answers. Most experimental clips use older facial-manipulation techniques and minimal context, so the results cannot establish equivalent human–machine complementarity for current fully generated video.

## M11 — Perceptual Judgments of Video Authenticity: An Examination of Viewing Duration, Confidence, Content, and Strategies

**Collected reading copy:** [PDF](../documents/M11-video-authenticity-human-perception.pdf)

**Authors:** Catherine E. Davodi, Sarah Barrington, Hany Farid, and Emily A. Cooper.  
**Publication:** 2026 — CVPR Workshops, pp. 10679–10686. Published workshop paper.

[Source record](https://openaccess.thecvf.com/content/CVPR2026W/APAI/html/Davodi_Perceptual_Judgments_of_Video_Authenticity_An_Examination_of_Viewing_Duration_CVPRW_2026_paper.html) · [Open author-copy PDF](https://hfarid.org/downloads/publications/cvprw26a.pdf)

Tests 376 participants on authentic and generated videos depicting human and nonhuman scenes. Increasing exposure from one frame to eight seconds raises identification of generated clips from 57.7% to 74.6%, while accuracy on genuine clips remains near 60%. The study also examines confidence and reported visual cues. Participants were US-based English speakers viewing a limited set of themes under controlled conditions, which constrains generalization to everyday viewing.

## Search and access record

Targeted primary-source collection, searched 16–17 September 2026; not an exhaustive systematic review. Full texts were inspected for all entries. M03 uses an openly available author version while its publication status was checked against published metadata. M09 remains explicitly labeled a preprint. No datasets or model weights were collected.

Selected exact queries executed during collection:

```text
site.openaccess.thecvf.com Wang CNN Generated Images Surprisingly Easy Spot Now CVPR 2020
site.openaccess.thecvf.com Ojha Towards Universal Fake Image Detectors Generalize Across Generative Models 2023
"Fake or JPEG?" Grommelt conference publication
site.proceedings.neurips.cc DF40 Toward Next Generation Deepfake Detection 2024
"Deepfake-Eval-2024" conference accepted 2026 2025
AVFF Audio Visual Feature Fusion for Video Deepfake Detection site:openaccess.thecvf.com
"AV-Deepfake1M: A Large-Scale" "doi"
"AV-Deepfake1M++" 2025 arxiv
Chameleon dataset AI generated image detection human ICLR 2025
Groh 2022 deepfake detection by human crowds machines machine informed crowds PNAS
"Davodi" "CVPR" "2026" human detection
site:hfarid.org "cvprw26a"
```
