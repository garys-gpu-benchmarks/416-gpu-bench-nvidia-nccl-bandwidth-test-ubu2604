# Results: 416 NCCL Bandwidth Test

**Main goal:** Measure NCCL collective bandwidth and latency  
**Tools:** Compile nccl_bw.cu with nvcc and NCCL; run bin/nccl_bw <min_bytes> <warmup> <iters> <num_gpus> <collective>

Reference results from the validation run on the system shown in each section (recorded 2026-11-22). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 80GB HBM3 (81559 MiB) · Intel(R) Xeon(R) Platinum 8468 · Ubuntu 26.04.1 LTS · kernel 6.8.0-149-generic · driver 595.112.07
- **Run:** 2026-11-22T11:16:22Z · status **N/A-EXPECTED** (exit 0)
- **Time (mm:ss):** setup 00:54 · benchmark 00:02 · whole run 01:02
- **Source:** run 416_20261122_111622
- **Command:** `bash run_benchmark.sh --smoke --num-gpus 1 --min-bytes 8 --max-bytes 1024 --step-factor 2 --warmup-iters 1 --num-iterations 2`

| # | Metric | Result |
|---|---|---|
| 1 | All-reduce bus bandwidth at max message size, GB/s, na on single GPU (allreduce_busbw_gb_s) | na (expected: needs at least two GPUs) |
| 2 | All-reduce algorithm bandwidth at max message size, GB/s, na on single GPU (allreduce_algbw_gb_s) | na (expected: needs at least two GPUs) |
| 3 | All-reduce latency at min message size, us, na on single GPU (allreduce_latency_at_min_bytes_us) | na (expected: needs at least two GPUs) |
<!-- /profile:smoke -->
