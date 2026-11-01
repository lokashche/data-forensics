# data-forensics

Forensic statistics to check if data is real, using SciPy.

## Purpose

This repo has the code and notebooks for the talk "An Auditor's Guide to
Catching Fake Data: Forensic Statistics with SciPy" at SciPy India 2026.
It shows simple statistical tests that can flag numbers which may be
made up or wrong. The examples use synthetic data with planted
fabrication and Indian open government finance data.

## Tests covered

1. **Benford's Law**: first-digit test with `scipy.stats.chisquare` and mean absolute deviation (MAD).
2. **Last-digit and round-number tests**: checks for too many round numbers or uneven last digits.
3. **GRIM test**: checks whether a reported mean is possible for the sample size.
4. **Audit sampling**: sample sizes for data and label QA with `scipy.stats.binom` and `scipy.stats.hypergeom`.

## Status

Work in progress - built for SciPy India 2026.

## Setup

```bash
git clone https://github.com/lokashche/data-forensics.git
cd data-forensics
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

## Licence

MIT. See [LICENSE](LICENSE).
