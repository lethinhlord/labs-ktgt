# Demo_lab_QIM - Final Test Report

Updated: 2026-05-12 23:25:00

## Passed Checks

- 12/12 Docker full workflow tests passed.
- 12/12 early `checkwork` tests failed correctly before required artifacts existed.
- 12/12 labs decode the bundled MP4 through `ffmpeg/ffprobe` before algorithm checks.
- 12/12 tar packages passed static Labtainer structure checks, including `dockerfiles/Dockerfile.<lab>.qimlab.student`, `qimlab/home_tar/home.tar`, and `qimlab/sys_tar/sys.tar`.
- 12/12 labs include Labtainer-style `results.config` and `goals.config` identifiers.
- Generated `work/`, `student-work/`, and `grade.txt` are excluded from every tar.
- Obsolete command/config patterns were removed: `--step`, `moreterm.py`, custom `qim-*` wrappers, `HOST_HOME_XFER seed_dir/`, and binary MP4 `FILE_REGEX`.

## Labtainer Note

The local Windows workspace does not provide `imodule` or `labtainer`, so real Labtainer runtime import/startup could not be executed here. Docker execution and tar-level structure checks passed for all 12 labs.
