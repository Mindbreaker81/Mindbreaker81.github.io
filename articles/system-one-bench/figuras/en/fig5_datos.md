# Figure 5 — complete data table

One row per configuration drawn in Figure 5 — the 115-entry web selection with a current adjusted score — sorted by adjusted score. `*` marks incomplete coverage (fewer than 11 phases; descriptive, not comparable). `n records` counts current ground-truth IDs; `n costs` counts records carrying a stored cost; `USD/1,000` is recorded API spend over the record denominator (`—` = no recorded API invoice — the plot's right-hand lane — and `≥` = partial or lower-bound cost); `n ms`/`Median ms` are client-measured milliseconds per record — for cascades, D1+reviewer pairs (fusions record no ms of their own). `jev`-adapter runs include a fixed inter-request pause inside those ms (0.3 s by default; 3.5 s for the Base Labs `:free` pair); `llm`-adapter runs carry no fixed pause. Local operation is unpriced, not free; the majority baseline needs no calls and is not a configuration, so it has no row. The point labelled “Qwen FP8” is `llm_qwen38_27b_fp8_jev71_off_d0_disc`; the later control `llm_qwen38_27b_fp8_jev76_off_d0_disc` (adjusted 67.2, median 2,707.5 ms over 194 IDs) is outside the web selection and is not drawn.

The Sets column counts complete phases including OOD; OOD is excluded from the adjusted aggregate. A complete run therefore has 11/11 phases but ten scored sets.

| Run | Adjusted | Sets | n records | n costs | USD/1,000 | n ms | Median ms | Notes |
|---|---:|---:|---:|---:|---:|---:|---:|---|
| `jev_haiku55rev_audit` | 77.6 | 11/11 | 194 | 194 | 0.683324 | 194 | 4,536 | cascade: ms = jev_v3 + jev_haiku55rev_raw per record; labelled “Jev→Haiku” in the figure |
| `llm_gpt6luna_jevrev_audit` | 74.6 | 11/11 | 194 | 194 | 0.244265 | 194 | 3,732 | cascade: ms = llm_gpt6luna_prob + llm_gpt6luna_jevrev_raw per record |
| `jev_cerebrasqwennsrev_audit` | 73.1 | 11/11 | 194 | 194 | 3.780519 | 194 | 1,824.5 | cascade: ms = jev_v3 + jev_cerebrasqwennsrev_raw per record |
| `llm_haiku55_adapt_prob` | 73.0 | 11/11 | 194 | 194 | ≥0.362988 | 194 | 2,655.5 | partial or lower-bound cost; labelled “Haiku” in the figure |
| `jev_cerebrasqwennsrev_review` | 72.4 | 11/11 | 194 | 194 | 3.780519 | 194 | 1,824.5 | cascade: ms = jev_v3 + jev_cerebrasqwennsrev_raw per record |
| `llm_gpt6luna_jevrev_review` | 72.1 | 11/11 | 194 | 194 | 0.244265 | 194 | 3,732 | cascade: ms = llm_gpt6luna_prob + llm_gpt6luna_jevrev_raw per record |
| `llm_haiku55_adapt_prob_r2` | 71.5 | 11/11 | 194 | 194 | 0.3599 | 194 | 2,597 | — |
| `jev_cerebrasqwenrev_review` | 71.5 | 11/11 | 194 | 194 | 4.052248 | 194 | 2,060 | cascade: ms = jev_v3 + jev_cerebrasqwenrev_raw per record |
| `jev_cerebrasqwenrev_audit` | 71.3 | 11/11 | 194 | 194 | 4.052248 | 194 | 2,060 | cascade: ms = jev_v3 + jev_cerebrasqwenrev_raw per record |
| `llm_gpt61sol_jevrev_audit` | 70.7 | 11/11 | 194 | 194 | 2.935008 | 194 | 4,138.5 | cascade: ms = llm_gpt61sol_low_prob + llm_gpt61sol_jevrev_raw per record |
| `decider_4b_solrev_review` | 70.6 | 11/11 | 194 | 194 | 5.394196 | 194 | 6,020.5 | cascade: ms = decider_4b + decider_4b_solrev_raw per record |
| `llm_cerebras_qwen38_27b_nostruct_prob` | 70.3 | 11/11 | 194 | 194 | 2.023579 | 194 | 636 | labelled “Cerebras-Qwen” in the figure |
| `llm_gpt61sol_jevrev_review` | 70.0 | 11/11 | 194 | 194 | 2.935008 | 194 | 4,138.5 | cascade: ms = llm_gpt61sol_low_prob + llm_gpt61sol_jevrev_raw per record |
| `decider_4b_haiku55rev_audit` | 69.4 | 11/11 | 194 | 194 | 0.666426 | 194 | 4,163.5 | cascade: ms = decider_4b + decider_4b_haiku55rev_raw per record |
| `llm_gpt61sol_low_prob` | 69.2 | 11/11 | 194 | 194 | 2.884691 | 194 | 3,515.5 | — |
| `decider_4b_solrev_audit` | 68.4 | 11/11 | 194 | 194 | 5.394196 | 194 | 6,020.5 | cascade: ms = decider_4b + decider_4b_solrev_raw per record |
| `llm_gpt61sol_low_disc` | 67.7 | 11/11 | 194 | 194 | 1.927948 | 194 | 2,304.5 | — |
| `jev_cascade_audit` | 67.6 | 11/11 | 194 | 194 | 0.084987 | 194 | 1,730 | cascade: ms = jev_v3 + jev_cascade_raw per record; labelled “Jev→Jev” in the figure |
| `llm_haiku55_off_disc` | 67.4 | 11/11 | 194 | 194 | 0.161984 | 194 | 1,288.5 | — |
| `decider_4b_llmrev_review` | 67.1 | 11/11 | 194 | 194 | 0.54073 | 194 | 8,800 | cascade: ms = decider_4b + decider_4b_llmrev_raw per record |
| `llm_qwen38_27b_arcgguf_inject_disc` | 66.8 | 11/11 | 194 | 0 | — | 194 | 3,421.5 | no recorded API invoice |
| `llm_qwen38_27b_nvfp4_inject_disc` | 66.7 | 11/11 | 194 | 0 | — | 194 | 2,213 | no recorded API invoice |
| `llm_qwen38_27b_fp8_jev71_off_d0_disc` | 66.6 | 11/11 | 194 | 0 | — | 194 | 2,636 | no recorded API invoice; labelled “Qwen FP8” in the figure |
| `medgemma_27b_jev77_jevrev_audit` | 66.5 | 11/11 | 194 | 194 | 0.050317 | 194 | 10,014 | cascade: ms = llm_medgemma_27b_it_bf16_jev77_d0_disc + medgemma_27b_jev77_jevrev_raw per record |
| `dgemma_26b_a4b_nvfp4_s1_jevrev_review` | 66.1 | 11/11 | 194 | 194 | 0.050292 | 194 | 724.5 | cascade: ms = dgemma_26b_a4b_nvfp4_s1 + dgemma_26b_a4b_nvfp4_s1_jevrev_raw per record |
| `jev114_cascade_audit` | 66.0 | 11/11 | 194 | 194 | 0.084992 | 194 | 1,078 | cascade: ms = jev_v114_typesafe_preview + jev114_cascade_raw per record |
| `dgemma_26b_a4b_nvfp4_jevrev_review` | 66.0 | 11/11 | 194 | 194 | 0.050294 | 194 | 917 | cascade: ms = dgemma_26b_a4b_nvfp4 + dgemma_26b_a4b_nvfp4_jevrev_raw per record |
| `llm_haiku55_off_prob` | 65.9 | 11/11 | 194 | 194 | 0.258596 | 194 | 1,656.5 | — |
| `decider_4b_jevrev_audit` | 65.6 | 11/11 | 194 | 194 | 0.050288 | 194 | 1,152 | cascade: ms = decider_4b + decider_4b_jevrev_raw per record; labelled “Dec4B→Jev” in the figure |
| `jev_1_14_cascade_audit` | 65.5 | 11/11 | 194 | 194 | 0.084991 | 194 | 1,177 | cascade: ms = jev_1_14 + jev_1_14_cascade_raw per record |
| `dgemma_26b_a4b_nvfp4_s1_jevrev_audit` | 65.1 | 11/11 | 194 | 194 | 0.050292 | 194 | 724.5 | cascade: ms = dgemma_26b_a4b_nvfp4_s1 + dgemma_26b_a4b_nvfp4_s1_jevrev_raw per record |
| `dgemma_26b_a4b_nvfp4_jevrev_audit` | 64.8 | 11/11 | 194 | 194 | 0.050294 | 194 | 917 | cascade: ms = dgemma_26b_a4b_nvfp4 + dgemma_26b_a4b_nvfp4_jevrev_raw per record |
| `llm_gpt6luna_prob` | 64.6 | 11/11 | 194 | 194 | 0.193936 | 194 | 3,151.5 | — |
| `decider_4b_msrev_audit` | 63.5 | 11/11 | 194 | 194 | 0.038532 | 194 | 957 | cascade: ms = decider_4b + decider_4b_msrev_raw per record |
| `llm_gpt6luna_disc` | 63.2 | 11/11 | 194 | 194 | 0.127915 | 194 | 1,896 | — |
| `llm_qwen38_27b_fp8_jev76_on_d0_disc` | 63.0 | 11/11 | 194 | 0 | — | 194 | 26,737 | no recorded API invoice |
| `llm_qwen38_27b_fp8_jev68_on_d0_prob` | 62.9 | 11/11 | 194 | 0 | — | 194 | 41,371 | no recorded API invoice |
| `decider_4b_jev114rev_audit` | 62.8 | 11/11 | 194 | 194 | 0.050288 | 194 | 742 | cascade: ms = decider_4b + decider_4b_jev114rev_raw per record |
| `llm_cerebras_qwen38_27b_disc` | 62.2 | 11/11 | 194 | 194 | 1.508419 | 194 | 573 | — |
| `llm_cerebras_qwen38_27b_nostruct_disc` | 61.8 | 11/11 | 194 | 194 | 1.382517 | 194 | 462 | — |
| `llm_cerebras_qwen38_27b_low_prob` | 59.9 | 11/11 | 194 | 194 | 2.235089 | 194 | 766 | — |
| `decider_4b_clefrev_audit` | 58.7 | 11/11 | 194 | 194 | — | 194 | 2,296 | cascade: ms = decider_4b + decider_4b_clefrev_raw per record; recorded zeros; no external API spend; labelled “Dec4B→Clef” in the figure |
| `mammoth_1_local` | 58.3 | 11/11 | 194 | 0 | — | 194 | 977 | no recorded API invoice |
| `mammoth_1_or` | 57.0 | 11/11 | 194 | 194 | — | 194 | 4,076.5 | recorded zeros; no external API spend |
| `clef_27b` | 55.8 | 11/11 | 194 | 0 | — | 194 | 874 | no recorded API invoice |
| `decider_4b_llmrev_audit` | 54.6 | 11/11 | 194 | 194 | 0.54073 | 194 | 8,800 | cascade: ms = decider_4b + decider_4b_llmrev_raw per record |
| `clef_27b_or` | 54.1 | 11/11 | 194 | 194 | 0.045451 | 194 | 765 | — |
| `elephant_1_local` | 53.6 | 11/11 | 194 | 0 | — | 194 | 337 | no recorded API invoice |
| `pplx_decider_v11_27b_or` | 53.3 | 11/11 | 194 | 194 | 0.038093 | 194 | 995.5 | — |
| `elephant_1_or` | 52.3 | 11/11 | 194 | 194 | — | 194 | 3,921.5 | recorded zeros; no external API spend |
| `llm_qwen38_27b_nvfp4_nostruct_prob` | 52.1 | 11/11 | 194 | 0 | — | 194 | 5,287 | no recorded API invoice |
| `llm_qwen38_27b_fp8_inject_prob` | 51.9 | 11/11 | 194 | 0 | — | 194 | 6,503 | no recorded API invoice |
| `dgemma_26b_a4b_nvfp4_s1` | 51.8 | 11/11 | 194 | 0 | — | 194 | 122 | no recorded API invoice; labelled “DGemma” in the figure |
| `decider_4b_d35rev_audit` | 51.8 | 11/11 | 194 | 194 | — | 194 | 722 | cascade: ms = decider_4b + decider_4b_d35rev_raw per record; recorded zeros; no external API spend |
| `decider_4b_drexrev_audit` | 51.6 | 11/11 | 194 | 194 | — | 194 | 2,129 | cascade: ms = decider_4b + decider_4b_drexrev_raw per record; recorded zeros; no external API spend |
| `llm_qwen38_27b_fp8_nostruct_t0_prob` | 51.6 | 11/11 | 194 | 0 | — | 194 | 6,485 | no recorded API invoice |
| `dgemma_26b_a4b_nvfp4` | 51.6 | 11/11 | 194 | 0 | — | 194 | 318 | no recorded API invoice |
| `llm_qwen38_27b_nvfp4_inject_prob` | 50.7 | 11/11 | 194 | 0 | — | 194 | 5,249.5 | no recorded API invoice |
| `mercury_decide_or` | 50.5 | 11/11 | 194 | 194 | 0.014504 | 194 | 815.5 | — |
| `jev_v114_typesafe_preview` | 50.3 | 11/11 | 194 | 194 | 0.034684 | 194 | 537 | — |
| `llm_qwen38_27b_fp8_jev68_off_d0_prob` | 50.0 | 11/11 | 194 | 0 | — | 194 | 6,247.5 | no recorded API invoice |
| `jev_1_14` | 49.8 | 11/11 | 194 | 194 | 0.034684 | 194 | 593.5 | — |
| `jev_luna_decisions` | 49.7* | 7/11 | 194 | 188 | ≥0.099886 | 194 | 675.5 | partial or lower-bound cost (cost known for 188/194 records); labelled “luna-dec” in the figure |
| `jev_v3` | 49.3 | 11/11 | 194 | 194 | 0.034684 | 194 | 638 | labelled “Jev” in the figure |
| `llm_qwen38_27b_fp8_nostruct_prob` | 49.2 | 11/11 | 194 | 0 | — | 194 | 6,368 | no recorded API invoice |
| `llm_dgemma_26b_a4b_nvfp4_nostruct_disc_rp` | 49.0 | 11/11 | 194 | 0 | — | 194 | 516 | no recorded API invoice |
| `llm_qwen38_27b_arcgguf_inject_prob` | 48.5 | 11/11 | 194 | 0 | — | 194 | 7,527 | no recorded API invoice |
| `decider_4b_clefflashrev_audit` | 48.2 | 11/11 | 194 | 194 | — | 194 | 541 | cascade: ms = decider_4b + decider_4b_clefflashrev_raw per record; recorded zeros; no external API spend |
| `llm_qwen38_27b_gguf81_nostruct_prob` | 48.0 | 11/11 | 194 | 0 | — | 194 | 10,738 | no recorded API invoice |
| `jev_ms_decision1` | 47.3 | 11/11 | 194 | 194 | 0.021242 | 194 | 693 | labelled “MS-Dec1” in the figure |
| `nimble_9b` | 46.9 | 11/11 | 194 | 0 | — | 194 | 1,619.5 | no recorded API invoice |
| `decider_4b_nimblerev_audit` | 45.9 | 11/11 | 194 | 194 | — | 194 | 7,629.5 | cascade: ms = decider_4b + decider_4b_nimblerev_raw per record; recorded zeros; no external API spend |
| `clef_flash_or` | 44.7 | 11/11 | 194 | 194 | 0.019517 | 194 | 720.5 | — |
| `clef_omni_or` | 44.7 | 11/11 | 194 | 194 | 0.130628 | 194 | 530 | — |
| `clef_flash_9b_xpu` | 44.6 | 11/11 | 194 | 0 | — | 194 | 142 | no recorded API invoice |
| `llm_ministral3b_med_disc` | 44.5* | 5/11 | 194 | 0 | — | 194 | 1,917 | no recorded API invoice |
| `drex_v15_9b` | 43.7 | 11/11 | 194 | 0 | — | 194 | 381 | no recorded API invoice; labelled “Drex” in the figure |
| `classify1_or` | 43.1 | 11/11 | 194 | 194 | 0.10409 | 194 | 691.5 | — |
| `drex_v20_or` | 41.9 | 11/11 | 194 | 194 | 0.028563 | 194 | 844.5 | — |
| `drex_v15_or` | 40.8 | 11/11 | 194 | 194 | 0.019042 | 194 | 875 | — |
| `jev_luna_decisions_fb` | 40.6 | 11/11 | 194 | 194 | 0.100639 | 194 | 671 | — |
| `solar_decide_or` | 39.9 | 11/11 | 194 | 194 | 0.160891 | 194 | 9,286.5 | — |
| `oai_luna_decisions` | 39.8 | 11/11 | 194 | 194 | 0.105666 | 194 | 441 | — |
| `decider_4b_cascade_audit` | 39.2* | 9/11 | 154 | 154 | — | 154 | 614 | cascade: ms = decider_4b + decider_4b_cascade_raw per record; recorded zeros; no external API spend |
| `decider_4b_aj32brev_audit` | 38.9 | 11/11 | 194 | 194 | — | 194 | 9,176.5 | cascade: ms = decider_4b + decider_4b_aj32brev_raw per record; recorded zeros; no external API spend |
| `decider_35b_a3b` | 38.8 | 11/11 | 194 | 0 | — | 194 | 675 | no recorded API invoice |
| `solar_decide_flash_or` | 36.9 | 11/11 | 194 | 194 | 0.160891 | 194 | 1,029.5 | — |
| `llm_cerebras_gptoss120b_low_prob` | 36.4 | 11/11 | 194 | 194 | 0.621215 | 194 | — | client ms not comparable |
| `decider_4b` | 33.8 | 11/11 | 194 | 0 | — | 194 | 200 | no recorded API invoice; labelled “Decider-4B” in the figure |
| `decider_35b_a3b_nvfp4` | 33.2 | 11/11 | 194 | 0 | — | 194 | 185 | no recorded API invoice |
| `liquid_d1_or` | 32.5 | 11/11 | 194 | 194 | 0.03135 | 194 | 610 | — |
| `tev1_4b_or` | 31.8 | 11/11 | 194 | 194 | 0.082287 | 194 | 784 | — |
| `kev_4b_or` | 30.7 | 11/11 | 194 | 194 | 0.019994 | 194 | 938.5 | — |
| `decider_4b_aj8brev_audit` | 27.7 | 11/11 | 194 | 194 | — | 194 | 2,750 | cascade: ms = decider_4b + decider_4b_aj8brev_raw per record; recorded zeros; no external API spend |
| `tev1_4b` | 27.0 | 11/11 | 194 | 0 | — | 194 | 452 | no recorded API invoice |
| `llm_medgemma_27b_it_bf16_jev77_d0_disc` | 23.7 | 11/11 | 194 | 0 | — | 194 | 9,387 | no recorded API invoice |
| `anyjev_qwen3_32b_l0` | 21.2 | 11/11 | 194 | 0 | — | 194 | 2,585.5 | no recorded API invoice |
| `decider_2b` | 19.5 | 11/11 | 194 | 0 | — | 194 | 78 | no recorded API invoice |
| `strands_2b_hobson_v19_xpu_trunc` | 19.4 | 11/11 | 194 | 0 | — | 194 | 124.5 | no recorded API invoice |
| `span01_lite_or` | 19.1 | 11/11 | 194 | 194 | — | 194 | 588 | recorded zeros; no external API spend |
| `span01_pro` | 18.5 | 11/11 | 194 | 194 | 0.016099 | 194 | 589 | — |
| `strands_2b_hobson_v19_xpu` | 17.9* | 10/11 | 194 | 0 | — | 194 | 125 | no recorded API invoice |
| `llm_gemma3_27b_it_bf16_jev77_d0_disc` | 13.7 | 11/11 | 194 | 0 | — | 194 | 9,418 | no recorded API invoice |
| `decider_0.8b` | 13.1 | 11/11 | 194 | 0 | — | 194 | 43 | no recorded API invoice |
| `anyjev_qwen3_8b_l0` | 12.7 | 11/11 | 194 | 0 | — | 194 | 702 | no recorded API invoice |
| `span01_lite` | 4.5 | 11/11 | 194 | 194 | — | 194 | 874 | recorded zeros; no external API spend |
| `gliner_decide_desc` | -2.4 | 11/11 | 194 | 0 | — | 194 | 42 | no recorded API invoice |
| `anyjev_qwen3_1.7b_l0` | -3.0 | 11/11 | 194 | 0 | — | 194 | 186 | no recorded API invoice |
| `tev1_0.8b` | -8.8 | 11/11 | 194 | 0 | — | 194 | 142 | no recorded API invoice |
| `llm_ministral3b_med_prob` | -9.8* | 4/11 | 194 | 0 | — | 194 | 4,780.5 | no recorded API invoice |
| `llm_qwen38_27b_prob` | -17.3* | 9/11 | 194 | 0 | — | 192 | 6,737 | no recorded API invoice |
| `laya_router` | -21.9 | 11/11 | 194 | 0 | — | 194 | 28 | no recorded API invoice |
| `clm_v0.1_8b` | -41.0 | 11/11 | 194 | 0 | — | 194 | 80 | no recorded API invoice |
| `llm_qwen38flash_prob` | -42.8* | 8/11 | 194 | 0 | — | 190 | 49,923.5 | no recorded API invoice |
| `julia_1` | -89.4 | 11/11 | 194 | 0 | — | 194 | 564.5 | no recorded API invoice |
