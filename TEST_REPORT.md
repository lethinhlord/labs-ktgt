# Demo_lab_QIM - Final Test Report

Updated: 2026-05-14

## Passed Checks

- 12/12 lab directories were regenerated successfully from `regenerate_labs_utf8.py`.
- 12/12 tar packages exist as individual importable files in `Demo_lab_QIM/tars`.
- 12/12 tar packages contain the standard Labtainer files: `config/start.config`, `instr_config/results.config`, `instr_config/goals.config`, `dockerfiles/Dockerfile.<lab>.qimlab.student`, `qimlab/home_tar/home.tar`, and `qimlab/sys_tar/sys.tar`.
- 12/12 `home.tar` files contain `guide.html`, `NOTE.txt`, `run_lab.py`, algorithm entrypoints, the sample MP4, and three cropped textbook illustration images.
- 12/12 `guide.html` files no longer contain the removed model section, model CSS class, Labtainer host/container diagram text, or footer.
- 12/12 `guide.html` files start with the new “Lý thuyết thuật toán cần biết” section covering DCT, quantization, QIM, ST-QIM, payload reliability, BER, PSNR, and SSIM.
- 12/12 `guide.html` files use styled math-card formula blocks with fractions, superscripts/subscripts, sigma notation, and short notes for DCT, quantization, QIM, ST-QIM, BER, PSNR, and SSIM.
- 12/12 `guide.html` files embed three cropped textbook figures as base64 data images, so the figures render even when the HTML is opened outside the lab folder.
- 12/12 `guide.html` files have no remaining relative `media/...` image references and no old `<pre class="formula">` blocks.
- 12/12 `guide.html` files no longer include the paragraph beginning with “Nguồn học thuật chính...”.
- 12/12 `guide.html` files no longer include the blue note block beginning with “Khi làm bài, ưu tiên đối chiếu...”.
- 12/12 `results.config` files continue to use Labtainer result identifiers: `video_hash`, `extract_frames`, `extract_audio`, `prepare_payload`, `embed_message`, `extract_message`, `quality_metrics`, and `combine_video`.
- 12/12 `goals.config` files remain empty like the reference `lab-demo/video-stego-dct`.
- 12/12 Python scripts in the generated lab home folders compile successfully with `py_compile`.
- 12/12 labs keep `REGISTRY b22dcat295`, `CONTAINER qimlab`, `USER ubuntu`, `TERMINALS 1`, and `X11 YES` in `start.config`.
- 12/12 lab guides keep the requested commands: `imodule https://github.com/lethinhlord/labs-ktgt/<lab>.tar` and `labtainer -r <lab>`.

## Runtime Notes

- Host Windows smoke execution could not run `extract_frames_audio.py` because `ffmpeg` is not installed in the local Windows PATH.
- Docker smoke execution could not be run in this environment because Docker Desktop daemon was not active: Docker CLI is installed, but the Linux engine pipe was unavailable.
- The generated Dockerfiles still install `ffmpeg` inside the lab image, so this blocker is local-environment specific rather than a missing packaged dependency.
