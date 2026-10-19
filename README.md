# Open Virtual Try-On Models: Licenses and Commercial Use

Which open-source virtual try-on models can you actually ship in a product?
Most try-on repos are research code, and most of their weights are released
under **non-commercial** licenses. This list sorts the popular ones by what
their code and weights licenses allow, so you can rule models in or out before
you spend a day setting up a GPU.

- Every license below was read from the repository's `LICENSE` file and the
  model card on Hugging Face. **Last checked: 2026-10-19.**
- Code license and weights license are listed separately because they often differ.
- A model built on another base model (FLUX, Stable Diffusion, AnimateDiff)
  also inherits that base model's terms.
- This is a reading aid, not legal advice. Always check the source before you ship.

## Contents

- [Commercial use looks possible](#commercial-use-looks-possible)
- [Non-commercial only](#non-commercial-only)
- [Classic research baselines](#classic-research-baselines)
- [Datasets](#datasets)
- [Try one in your browser](#try-one-in-your-browser)
- [Contributing](#contributing)

## Commercial use looks possible

Permissive code **and** weights, but read the notes column.

| Model | Repo since | Type | Code license | Weights license | Demo | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| [FASHN VTON v1.5](https://github.com/fashn-AI/fashn-vton-1.5) | 2026-01 | Image | Apache-2.0 | Apache-2.0 ([model card](https://huggingface.co/fashn-ai/fashn-vton-1.5)) | [Space](https://huggingface.co/spaces/fashn-ai/fashn-vton-1.5) | Maskless, pixel space; weights about 2 GB. |
| [Leffa](https://github.com/franciszzj/Leffa) | 2024-12 | Image, pose transfer | MIT | MIT ([model card](https://huggingface.co/franciszzj/Leffa)) | [Space](https://huggingface.co/spaces/franciszzj/Leffa) | CVPR 2025. Check the base checkpoints it loads. |
| [OmniTry](https://github.com/Kunbyte-AI/OmniTry) | 2025-06 | Image, any wearable | Apache-2.0 | Apache-2.0 ([model card](https://huggingface.co/Kunbyte/OmniTry)) | — | Needs **FLUX.1-Fill-dev**, which has its own non-commercial license. Needs 28 GB VRAM or more (README). |
| [ViViD](https://github.com/alibaba-yuanjing-aigclab/ViViD) | 2024-05 | Video | Apache-2.0 | See repo | — | Loads Stable Diffusion and AnimateDiff weights; check each one. |
| [DCI-VTON](https://github.com/bcmi/DCI-VTON-Virtual-Try-On) | 2023-08 | Image | MIT | See repo | — | ACM MM 2023. Built on Stable Diffusion. |

## Non-commercial only

Fine for research, demos and learning. Not for a paid product without a separate agreement with the authors.

| Model | Repo since | Type | Code license | Weights license | Demo | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| [IDM-VTON](https://github.com/yisol/IDM-VTON) | 2024-03 | Image | CC BY-NC-SA 4.0 | CC BY-NC-SA 4.0 | [Space](https://huggingface.co/spaces/yisol/IDM-VTON) | ECCV 2024. [ComfyUI node](https://github.com/TemryL/ComfyUI-IDM-VTON) (GPL-3.0). |
| [OOTDiffusion](https://github.com/levihsu/OOTDiffusion) | 2024-01 | Image | CC BY-NC-SA 4.0 | CC BY-NC-SA 4.0 | [Space](https://huggingface.co/spaces/levihsu/OOTDiffusion) | AAAI 2025. Half-body and full-body checkpoints. |
| [CatVTON](https://github.com/Zheng-Chong/CatVTON) | 2024-07 | Image | CC BY-NC-SA 4.0 | CC BY-NC-SA 4.0 | — | ICLR 2025. Under 8 GB VRAM at 1024×768 (repo description). |
| [CatV2TON](https://github.com/Zheng-Chong/CatV2TON) | 2025-01 | Image and video | No license file | See repo | — | CVPR 2025 Workshop. No license file means no permission by default. |
| [catvton-flux](https://github.com/nftblackmagic/catvton-flux) | 2024-11 | Image | MIT | CC BY-NC 2.0 ([beta model card](https://huggingface.co/xiaozaa/catvton-flux-beta)) | — | Code is MIT, weights are not. Also built on FLUX.1-Fill-dev. |
| [FitDiT](https://github.com/BoyuanJiang/FitDiT) | 2024-11 | Image | CC BY-NC-SA 4.0 | CC BY-NC-SA 4.0 | [Space](https://huggingface.co/spaces/BoyuanJiang/FitDiT) | Focused on keeping garment details intact. |
| [Voost](https://github.com/nxnai/Voost) | 2025-07 | Try-on and try-off | CC BY-NC-SA 4.0 | See repo | — | SIGGRAPH Asia 2025. |
| [MagicTryOn](https://github.com/vivoCameraResearch/Magic-TryOn) | 2025-05 | Video | CC BY-NC-SA 4.0 | See repo | — | Video diffusion transformer. |
| [MV-VTON](https://github.com/hywang2002/MV-VTON) | 2024-04 | Multi-view image | CC BY-NC-SA 4.0 | See repo | — | AAAI 2025. |
| [StableVITON](https://github.com/rlawjdghek/StableVITON) | 2023-12 | Image | No license file | See repo | — | CVPR 2024. |
| [LaDI-VTON](https://github.com/miccunifi/ladi-vton) | 2023-05 | Image | CC BY-NC 4.0 | See repo | — | ACM MM 2023. |

## Classic research baselines

Pre-diffusion models that papers still compare against. Useful for learning how warping and parsing work.

| Model | Repo since | Code license | Notes |
| --- | --- | --- | --- |
| [VITON-HD](https://github.com/shadow2496/VITON-HD) | 2021-04 | CC BY-NC 4.0 | CVPR 2021. Also the name of the dataset most models train on. |
| [HR-VITON](https://github.com/sangyun884/HR-VITON) | 2022-06 | No license file | ECCV 2022. |
| [GP-VTON](https://github.com/xiezhy6/GP-VTON) | 2023-03 | No license file | CVPR 2023. |
| [PF-AFN](https://github.com/geyuying/PF-AFN) | 2021-03 | No license file | CVPR 2021, parser-free. |

## Datasets

| Dataset | License | Notes |
| --- | --- | --- |
| [VITON-HD](https://github.com/shadow2496/VITON-HD) | CC BY-NC 4.0 | Upper-body garments with paired model photos. |
| [Dress Code](https://github.com/aimagelab/dress-code) | Yoox Net-a-Porter research licence | Upper body, lower body and dresses. Access by request. |
| [DeepFashion2](https://github.com/switchablenorms/DeepFashion2) | See repo | Detection and segmentation; often used for garment parsing. |

## Try one in your browser

No GPU? These run without any setup:

- Hugging Face Spaces linked in the tables above (IDM-VTON, OOTDiffusion, Leffa, FitDiT, FASHN), and the [Kolors Virtual Try-On Space](https://huggingface.co/spaces/Kwai-Kolors/Kolors-Virtual-Try-On).
- [WearTryOn](https://weartryon.com) is a hosted try-on that runs on your own photo, with single garments, full outfits, outfit swaps from a photo, hairstyles, glasses and makeup. It also has a [Chrome extension](https://chromewebstore.google.com/detail/cedndndelahcchpoojemdileobahgldi) that adds a Try on button to product photos. You get one free image without an account and free credits when you sign up.

This list leaves out "undress" and "clothes remover" tools on purpose and will not accept them.

## Contributing

Pull requests are welcome for a new model, a license change, or a mistake. Please link the exact `LICENSE` file or model card you read, so the row can be checked.

---

Maintained by the team behind [WearTryOn](https://weartryon.com). The list itself is released under [CC BY 4.0](LICENSE).
