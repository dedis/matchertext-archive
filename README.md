# MatcherText snapshot archive

Content-addressed inputs for the MatcherText injection-research pipeline.
Each object is stored as `sha256/<digest>`. `injection-research/manifest.json`
in the MatcherText repository maps each input to its digest. The pipeline
verifies each digest before it uses an object.

```sh
export MATCHERTEXT_SNAPSHOT_ARCHIVE=https://raw.githubusercontent.com/dedis/matchertext-archive/main
python3 pipeline/run_all.py
```

Objects are never changed or removed. A new snapshot only adds objects.

`juliet-c` is not here because it is larger than the GitHub file limit. The
pipeline downloads the same bytes from Zenodo record 4701387.

Each object keeps the terms of its upstream source.
