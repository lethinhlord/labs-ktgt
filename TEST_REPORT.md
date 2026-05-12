# Demo_lab_QIM - Final Test Report

Updated: 2026-05-12 23:55:00

## Passed Checks

- 12/12 Docker full workflow tests passed.
- 12/12 early `checkwork` tests failed correctly before required artifacts existed.
- 12/12 labs decode the bundled MP4 through `ffmpeg/ffprobe` before algorithm checks.
- 12/12 tar packages passed static Labtainer structure checks against `lab-demo/video-stego-dct`.
- 12/12 labs include `config/<lab>-home_tar.list`, `instr_config/pregrade.sh`, `dockerfiles/Dockerfile.<lab>.qimlab.student`, `qimlab/home_tar/home.tar`, `qimlab/sys_tar/sys.tar`, `qimlab/input.mp4`, `qimlab/message.txt`, and visible algorithm scripts.
- 12/12 `start.config` files align with the reference pattern: `REGISTRY b21dcat210`, `CONTAINER qimlab`, `USER ubuntu`, `TERMINALS 1`, `X11 YES`.
- 12/12 labs use the required MP4: `9c993a10-a70b-4046-8673-7ed9508140b3 (online-video-cutter.com).mp4`.
- Required MP4 SHA-256: `ca13501e8af0bd70bcc0325f2a8c0a23df503b7f45faec7609f96f918d9ee51f`.
- 12/12 labs include Labtainer-style `results.config` and `goals.config` identifiers.
- Generated `work/`, `student-work/`, and `grade.txt` are excluded from every tar.
- Obsolete command/config patterns were removed: `--step`, `moreterm.py`, custom `qim-*` wrappers, `HOST_HOME_XFER seed_dir/`, and binary MP4 `FILE_REGEX`.

## Labtainer Note

The local Windows workspace does not provide `imodule` or `labtainer`, so real Labtainer runtime import/startup could not be executed here. Docker execution and tar-level structure checks passed for all 12 labs.
