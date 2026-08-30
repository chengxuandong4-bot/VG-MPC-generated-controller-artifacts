# VG-MPC selected controller artifacts

This minimal archive contains only the selected controller-configuration artifacts from the 36 original model--benchmark--mode conditions, plus the smallest index needed to identify them.

## Important scope statement

In the retained experiments, the generated artifacts are primarily executable controller parameter configurations or parameter patches consumed by fixed MATLAB/Python controller implementations. They are not complete standalone controller programs, and this archive intentionally excludes the benchmark implementations, generation workflow, prompts, API metadata, metrics histories, plots, tests, hardware code, and repeated-run analyses.

## Contents

- `api_generated/`: 25 complete controller configurations directly associated with successful API-generation records.
- `fallback_generated/`: 7 complete configurations produced by the fallback path. They are retained for transparency but must not be described as direct LLM outputs.
- `incomplete_or_unretained/`: one incomplete fallback snapshot, two other unretained endpoints, and the expert-assisted `B030_FF35` endpoint. No matching complete controller configuration was retained for these four conditions; their JSON files are provenance records rather than executable controller configurations.
- `INDEX.csv`: one row for each of the 36 original campaign conditions.
- `SHA256SUMS.txt`: integrity hashes for every other file in this archive.

## Interpretation boundary

Only files under `api_generated/` should be called API-generated controller configurations. Files under `fallback_generated/` and `incomplete_or_unretained/` remain included at the author's request so the reported campaign endpoints are not silently omitted.

The GPT-5.2 AUV dual-objective endpoint `B030_FF35` is classified as expert-assisted rather than purely LLM-generated. Generations 1--79 were API-based automatic iterations; expert recommendations were then used to revise the prompt and selected controller parameters for generation 80, which counted in the scheduled run budget; generations 81--100 resumed API-based automatic iteration. The benchmark simulator, metrics, score computation, acceptance rules, pairwise comparison, and incumbent-update logic were not manually changed. The matching complete generation-80 configuration was not retained and is therefore not reconstructed in this archive.

No open-source license has yet been selected for this pre-publication package.
