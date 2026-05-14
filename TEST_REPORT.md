# Demo_lab_QIM - Test Report

Updated: 2026-05-14

## Passed Checks

- 12/12 lab directories regenerated successfully from `regenerate_labs_utf8.py`.
- 12/12 tar packages exist as individual importable files in `Demo_lab_QIM/tars`.
- 12/12 generated `config/start.config` files use `REGISTRY lethinhlord`.
- 12/12 tar packages also contain `REGISTRY lethinhlord` inside `<lab>/config/start.config`.
- 0/12 generated labs and 0/12 tar packages contain the old `REGISTRY b22dcat295`.
- Docker Hub contains `lethinhlord/labtainer.base2:latest`, mirrored from the public Labtainer base image required by `FROM $registry/labtainer.base2`.
- 12/12 guides contain 9 math-card formula blocks: DCT 2D, matrix DCT/IDCT, DCT quantization, scalar QIM, blind QIM extraction, dither modulation, ST-QIM embedding, ST-QIM extraction, and PSNR/BER/SSIM quality metrics.
- 12/12 guides use MathML for the formula body, so fractions, summations, subscripts, superscripts, hats, and argmin notation render visually instead of appearing as plain text.
- 12/12 formula sections use real Greek/math symbols: `Δ`, `Σ`, `π`, `α`, `λ`, `μ`, `σ`, `∈`, `≤`, `≠`, `√`, and `∑`.
- 12/12 formula sections were checked to ensure old entity-based formula text such as `&Delta;`, `&Sigma;`, `&pi;`, `&alpha;`, `&lambda;`, `&mu;`, `&sigma;`, and old manual fraction markup no longer appears.
- 12/12 guides still embed three cropped textbook figures as base64 data images.
- 12/12 `results.config` files keep Labtainer result identifiers: `video_hash`, `extract_frames`, `extract_audio`, `prepare_payload`, `embed_message`, `extract_message`, `quality_metrics`, and `combine_video`.
- 12/12 generated tars keep the required GitHub `imodule` URL format: `https://github.com/lethinhlord/labs-ktgt/<lab>.tar`.
- 12/12 generated Python lab scripts compile successfully with `py_compile`.
- 84/84 student-facing guide files and 36/36 guide files inside packaged `home.tar` archives were checked to ensure they do not expose result files, grading config paths, internal result identifiers, or `Y - ...` checkwork markers.

## Math Review

- DCT 2D: verified with the standard 8x8 orthonormal JPEG-style DCT form using `C(0)=1/sqrt(2)` and factor `1/4`.
- Matrix DCT/IDCT: verified as `C = T X T^T` and `X = T^T C T` for an orthonormal transform matrix.
- Quantization: verified as coefficient quantization `Cq = round(C/Q)` and reconstruction `Chat = Cq*Q`.
- Scalar QIM: rewritten in the standard dither/coset form `Q_Δ(x,d_b)=Δ·round((x-d_b)/Δ)+d_b`, with `d_0=0` and `d_1=Δ/2`.
- QIM extraction: verified as blind nearest-coset decision using the received coefficient `r`.
- ST-QIM: verified as projection `z=u^T x`, quantization of `z`, and vector update `y=x+lambda(z'-z)u` with unit-norm keyed spreading vector `u`.
- ST-QIM extraction: verified as nearest-coset decision after projecting the received vector with the same key-derived `u`.
- Quality metrics: verified PSNR, BER, and SSIM formulas; MSE is written over `H*W*C` for image/video frames.
