# LIGHT WAVE DEHAZE

Fourteen slides covering the problem statement, existing approaches, motivation, method objectives, dataset, evaluation metrics, targets, checkpoint results, and next steps, followed by a thank-you slide. Slide text is in English; the user-supplied architecture comparison on slide 5 retains its original Vietnamese and English labels. The topic name follows the supplied midterm deck exactly: **LIGHT WAVE DEHAZE**. The university name is omitted from the cover. The cover has the original UET and Faculty of Information Technology (FIT) logos side by side, both 2.00 cm tall. Each content slide keeps only the UET logo in the footer, followed by the English school name, VNU University of Engineering and Technology. The footer logo is 0.50 cm tall. All logos preserve their original proportions. The enlarged original UET logo and template colors are retained. The cover has no subtitle. Reference lines are omitted from the visible slides; provenance is recorded here and in LaTeX comments.

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
| 5. UDPNet and MB-TaylorFormer | User-supplied image `assets/Sơ đồ kiến trúc khử sương ảnh.png`: depth-guided dehazing and multi-branch efficient Transformer architectures |
| 6. Combining Strengths | Translated question from page 5; replacement question-mark icon from Twemoji |
| 7. Frequency-Domain Observation | Original DWT illustration from page 6, with motivation from pages 5 and 8 |
| 8. Overall Design and Objectives | Editable vector schematic and combined restoration/efficiency objectives, based on pages 8, 10--11, and 14--15 |
| 9. Dataset | SOTS-ITS / RESIDE ITS: user-supplied counts interpreted as 12,990 training, 1,000 validation, and 500 test images; RESIDE ITS for training/validation and SOTS Indoor for testing |
| 10. Evaluation Metrics | Definitions and interpretation of PSNR, SSIM, FPS, and QSS (Quality-Speed Score), with QSS = FPS/MSE measuring the balance between quality and speed |
| 11. Target | PSNR and SSIM targets from the preliminary research proposal, pages 1--2; user-requested QSS > 0.45 replaces the FPS target |
| 12. Checkpoint Results | User-supplied comparison table; ours uses explicitly labeled illustrative values around the requested approximate PSNR, FPS, parameter count, and FLOPs |
| 13. Next Steps | Experiment with replacing Attention by Mamba in LFRN, tune the corresponding architecture/training hyperparameters, and compare quality and speed |
| 14. Thank You | Closing slide for questions and discussion |

The target slide lists proposed thresholds, not achieved results: PSNR >= 25 dB, SSIM >= 0.95, and QSS > 0.45. The QSS threshold is supplied by the user. Edge deployment is a future optimization direction and is not substituted for the source deck's topic name.

The checkpoint table preserves the supplied baseline data, including UDPNet's two-part parameter/FLOP counts. The ours row uses illustrative values (not measured results): PSNR 31.084 dB, FPS 17.263, 10.137 M parameters, and 49.286 G FLOPs; SSIM 0.9691 is retained from the supplied table. Every QSS entry is computed as `FPS * 10^(PSNR/10) / 255^2` and rounded to five decimal places. This gives QSS 0.34075 for ours, below the proposed target of 0.45. The calculation uses the displayed aggregate PSNR/FPS values and assumes an 8-bit image range.

The question-mark icon on slide 6 is from [Twemoji 14.0.2](https://github.com/twitter/twemoji/blob/v14.0.2/assets/svg/2753.svg), copyright Twitter, Inc. and contributors, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). It replaces the original watermarked illustration.

The remaining figures are extracted from the supplied PDF. Cropping removes only surrounding margins. The LightWaveDehaze overview is an editable TikZ vector schematic in `figures/lightwave-overview.tex`. It uses uniform rectangular processing blocks, original input/output photograph crops, and concise English labels. It summarizes LFRN followed by DEN; internal layers and subband routing are intentionally omitted. The symbol $\widetilde{I}$ denotes the intermediate image and $\widehat{I}$ the final restored image. This is a schematic of the method, not a layer-by-layer architecture or an experimental result. Other text, tables, the imaging equation, and targets are editable in LaTeX. The university logo remains the original branding asset.
