# LIGHT WAVE DEHAZE

Ten slides in English covering the problem statement, existing approaches, motivation, method objectives, and evaluation metrics, followed by a thank-you slide. The topic name follows the supplied midterm deck exactly: **LIGHT WAVE DEHAZE**. The university name is omitted from the cover. The cover has the original UET and Faculty of Information Technology (FIT) logos side by side, both 2.00 cm tall. Each content slide keeps only the UET logo in the footer, followed by the English school name, VNU University of Engineering and Technology. The footer logo is 0.50 cm tall. All logos preserve their original proportions. The enlarged original UET logo and template colors are retained. The cover has no subtitle. Reference lines are omitted from the visible slides; provenance is recorded here and in LaTeX comments.

## Build

Run twice in the directory containing `main.tex`:

```bash
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

Alternatively, upload the complete folder to Overleaf and select pdfLaTeX.

## Edit

- Slide content: `main.tex`.
- UET theme: `beamerthemeUET.sty`.
- Image assets: `assets/`.
- Editable overview diagram: `figures/lightwave-overview.tex`.
- Team members: Lương Duy Quân, Lê Minh Sơn, and Nguyễn Khánh Việt. Vietnamese diacritics are preserved in the names.
- The two cover logos are 2.00 cm tall; the single UET footer logo is 0.50 cm tall. The supervisor field is left empty.

## Sources

- Template: https://github.com/InboxMeNow/TemplateSlideUET
- Original FIT logo: https://www.fit.uet.vnu.edu.vn/wp-content/uploads/2024/04/cropped-fit-logo1.png, as used on the official faculty website https://www.fit.uet.vnu.edu.vn/.
- Midterm slides: the 21-page PDF supplied by the user. The images and LightWaveDehaze results come from this file.
- Preliminary research proposal: the two-page PDF supplied as `Untitled document.pdf`.
- PSNR and SSIM definitions: https://scikit-image.org/docs/stable/api/skimage.metrics.html. FPS denotes frames processed per second; fair comparisons fix the hardware, image resolution, and batch size.

## Alignment with the supplied deck

| Output slide | Reference in the midterm deck |
| --- | --- |
| 1. LIGHT WAVE DEHAZE | Topic name from page 1 |
| 2. Problem Statement | Formula and original hazy/clean image pair from page 2 |
| 3. Why Dehazing Is Needed | Original building photo and detection/tracking illustration from page 3 |
| 4. Existing Dehazing Approaches | Physical Prior, CNN, Transformer, and Diffusion from page 4 |
| 5. Combining Strengths | Translated question from page 5; replacement question-mark icon from Twemoji |
| 6. Frequency-Domain Observation | Original DWT illustration from page 6, with motivation from pages 5 and 8 |
| 7. Overall Design and Objectives | Editable vector schematic and combined restoration/efficiency objectives, based on pages 8, 10--11, and 14--15 |
| 8. Evaluation Metrics | Definitions and interpretation of PSNR, SSIM, and FPS, introduced before their target values |
| 9. Further Optimization Targets | Separate future targets from the preliminary research proposal, pages 1--2 |
| 10. Thank You | Closing slide for questions and discussion |

The optimization-target slide lists target thresholds from the proposal, not achieved results. Edge deployment is a future optimization direction and is not substituted for the source deck's topic name.

The question-mark icon on slide 5 is from [Twemoji 14.0.2](https://github.com/twitter/twemoji/blob/v14.0.2/assets/svg/2753.svg), copyright Twitter, Inc. and contributors, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). It replaces the original watermarked illustration.

The remaining figures are extracted from the supplied PDF. Cropping removes only surrounding margins. The LightWaveDehaze overview is an editable TikZ vector schematic in `figures/lightwave-overview.tex`. It uses uniform rectangular processing blocks, original input/output photograph crops, and concise English labels. It summarizes LFRN followed by DEN; internal layers and subband routing are intentionally omitted. The symbol $\widetilde{I}$ denotes the intermediate image and $\widehat{I}$ the final restored image. This is a schematic of the method, not a layer-by-layer architecture or an experimental result. Other text, tables, the imaging equation, and targets are editable in LaTeX. The university logo remains the original branding asset.
