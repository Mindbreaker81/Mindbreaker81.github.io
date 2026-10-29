# DGX Bench

Public report: <https://mindbreaker81.github.io/projects/dgx-bench/>

A frozen Spanish-language report comparing local models on NVIDIA DGX Spark with frontier APIs:
code fixes, agent loops, plan execution, live planner/reviewer/executor chains, vision and OCR.
The report includes configuration limits, controls and methodological caveats.

`index.html` is self-contained. `snapshot.json` records the source HTML checksum, export time and
source checkout commit. Internal service addresses and lab navigation are omitted from this edition.

Updates are prepared from the reviewed `benchmark/index.html` in the local `dgx-bench` checkout:

```bash
# Prepare files for review without publishing:
python3 benchmark/export-public.py --site-dir ../mindbreaker81.github.io

# From a clean, synchronized portfolio checkout, export, commit and publish:
./publish-github.sh ../mindbreaker81.github.io
```

The update command belongs to `dgx-bench`; it is not executed by GitHub Pages. The portfolio serves
only the exported static report. Model weights, credentials and raw API responses are not included.
