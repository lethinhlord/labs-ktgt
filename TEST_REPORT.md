# Demo_lab_QIM - Final Test Report

Updated: 2026-05-14 17:05:00

## Passed Checks

- 12/12 Docker full workflow tests passed.
- 12/12 early `checkwork` tests failed correctly before required artifacts existed.
- 12/12 labs decode the bundled MP4 through `ffmpeg/ffprobe` before algorithm checks.
- 12/12 tar packages passed static Labtainer structure checks against `lab-demo/video-stego-dct`.
- 12/12 labs include `config/<lab>-home_tar.list`, `instr_config/pregrade.sh`, `dockerfiles/Dockerfile.<lab>.qimlab.student`, `qimlab/home_tar/home.tar`, `qimlab/sys_tar/sys.tar`, `qimlab/input.mp4`, `qimlab/message.txt`, and visible algorithm scripts.
- 12/12 tar packages exclude root-only Docker/test files and the expanded `qimlab/home` tree, matching the cleaner `video-stego-dct` package shape.
- 12/12 `home_tar/home.tar` files include `.local/bin/checkwork` and `.bashrc` prepends `$HOME/.local/bin` to `PATH`.
- 12/12 algorithm entrypoint scripts are included both at container level and in `home_tar`.
- 12/12 `start.config` files align with the reference pattern: `REGISTRY b22dcat295`, `CONTAINER qimlab`, `USER ubuntu`, `TERMINALS 1`, `X11 YES`.
- 12/12 `guide.html` and `NOTE.txt` files use the requested import command pattern: `imodule https://github.com/lethinhlord/labs-ktgt/<lab>.tar`.
- 12/12 `guide.html` and `NOTE.txt` files use the requested run command pattern: `labtainer -r <lab>`.
- 12/12 `guide.html` files were compacted against the `video-stego-dct` reference style: purpose, theory, Labtainer model, startup commands, sequential tasks, checkwork, and stoplab only.
- 12/12 `guide.html` files have no footer class or `Demo_lab_QIM` footer text.
- 12/12 `guide.html` and `NOTE.txt` files use `stoplab <lab>` with the exact lab name.
- 12/12 tar files are named exactly by lab id, for example `qim_scalar.tar`, `qim_dct_block.tar`, and `stqim_video_pipeline.tar`.
- 12/12 labs use the required MP4: `9c993a10-a70b-4046-8673-7ed9508140b3 (online-video-cutter.com).mp4`.
- Required MP4 SHA-256: `ca13501e8af0bd70bcc0325f2a8c0a23df503b7f45faec7609f96f918d9ee51f`.
- 12/12 labs include Labtainer-style `results.config` and `goals.config` identifiers.
- Generated `work/`, `student-work/`, and `grade.txt` are excluded from every tar.
- Obsolete command/config patterns were removed: `--step`, `moreterm.py`, custom `qim-*` wrappers, `HOST_HOME_XFER seed_dir/`, and binary MP4 `FILE_REGEX`.

## Labtainer Note

The local Windows workspace does not provide `imodule` or `labtainer`, so real Labtainer runtime import/startup could not be executed here. Docker execution and tar-level structure checks passed for all 12 labs.
