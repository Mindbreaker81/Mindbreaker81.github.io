# Figura 5 — tabla de datos completa

Una fila por configuración dibujada en la Figura 5 —la selección web de 115 entradas con ajustado vigente—, ordenada por ajustado. El `*` marca cobertura incompleta (menos de 11 fases; descriptivo, no comparable). «n registros» cuenta los IDs del GT vigente; «n costes» los registros con coste guardado; «USD/1.000» es el gasto API registrado sobre el denominador de registros («—» = sin factura API registrada, el carril derecho del gráfico; «≥» = coste parcial o cota inferior); «n ms»/«Mediana ms» son milisegundos medidos desde el cliente por registro —en las cascadas, pares D1+revisor (las fusiones no guardan ms propio)—. Los runs del adaptador `jev` incluyen una pausa fija entre peticiones dentro de esos ms (0,3 s por defecto; 3,5 s en los runs `:free` de Base Labs); los del adaptador `llm` no llevan pausa fija. La operación local no tiene precio, no es gratis; la línea base de mayoría no necesita llamadas y no es una configuración, así que no tiene fila. El punto rotulado «Qwen FP8» es `llm_qwen38_27b_fp8_jev71_off_d0_disc`; el control posterior `llm_qwen38_27b_fp8_jev76_off_d0_disc` (ajustado 67,2, mediana 2.707,5 ms sobre 194 IDs) está fuera de la selección web y no se dibuja.

La columna Sets cuenta fases completas incluido OOD; OOD queda fuera del agregado ajustado. Un run completo tiene por tanto 11/11 fases, pero diez sets puntuables.

| Run | Ajustado | Sets | n registros | n costes | USD/1.000 | n ms | Mediana ms | Notas |
|---|---:|---:|---:|---:|---:|---:|---:|---|
| `jev_haiku55rev_audit` | 77,6 | 11/11 | 194 | 194 | 0,683324 | 194 | 4.536 | cascada: ms = jev_v3 + jev_haiku55rev_raw por registro; rotulado «Jev→Haiku» en la figura |
| `llm_gpt6luna_jevrev_audit` | 74,6 | 11/11 | 194 | 194 | 0,244265 | 194 | 3.732 | cascada: ms = llm_gpt6luna_prob + llm_gpt6luna_jevrev_raw por registro |
| `jev_cerebrasqwennsrev_audit` | 73,1 | 11/11 | 194 | 194 | 3,780519 | 194 | 1.824,5 | cascada: ms = jev_v3 + jev_cerebrasqwennsrev_raw por registro |
| `llm_haiku55_adapt_prob` | 73,0 | 11/11 | 194 | 194 | ≥0,362988 | 194 | 2.655,5 | coste parcial o cota inferior; rotulado «Haiku» en la figura |
| `jev_cerebrasqwennsrev_review` | 72,4 | 11/11 | 194 | 194 | 3,780519 | 194 | 1.824,5 | cascada: ms = jev_v3 + jev_cerebrasqwennsrev_raw por registro |
| `llm_gpt6luna_jevrev_review` | 72,1 | 11/11 | 194 | 194 | 0,244265 | 194 | 3.732 | cascada: ms = llm_gpt6luna_prob + llm_gpt6luna_jevrev_raw por registro |
| `llm_haiku55_adapt_prob_r2` | 71,5 | 11/11 | 194 | 194 | 0,3599 | 194 | 2.597 | — |
| `jev_cerebrasqwenrev_review` | 71,5 | 11/11 | 194 | 194 | 4,052248 | 194 | 2.060 | cascada: ms = jev_v3 + jev_cerebrasqwenrev_raw por registro |
| `jev_cerebrasqwenrev_audit` | 71,3 | 11/11 | 194 | 194 | 4,052248 | 194 | 2.060 | cascada: ms = jev_v3 + jev_cerebrasqwenrev_raw por registro |
| `llm_gpt61sol_jevrev_audit` | 70,7 | 11/11 | 194 | 194 | 2,935008 | 194 | 4.138,5 | cascada: ms = llm_gpt61sol_low_prob + llm_gpt61sol_jevrev_raw por registro |
| `decider_4b_solrev_review` | 70,6 | 11/11 | 194 | 194 | 5,394196 | 194 | 6.020,5 | cascada: ms = decider_4b + decider_4b_solrev_raw por registro |
| `llm_cerebras_qwen38_27b_nostruct_prob` | 70,3 | 11/11 | 194 | 194 | 2,023579 | 194 | 636 | rotulado «Cerebras-Qwen» en la figura |
| `llm_gpt61sol_jevrev_review` | 70,0 | 11/11 | 194 | 194 | 2,935008 | 194 | 4.138,5 | cascada: ms = llm_gpt61sol_low_prob + llm_gpt61sol_jevrev_raw por registro |
| `decider_4b_haiku55rev_audit` | 69,4 | 11/11 | 194 | 194 | 0,666426 | 194 | 4.163,5 | cascada: ms = decider_4b + decider_4b_haiku55rev_raw por registro |
| `llm_gpt61sol_low_prob` | 69,2 | 11/11 | 194 | 194 | 2,884691 | 194 | 3.515,5 | — |
| `decider_4b_solrev_audit` | 68,4 | 11/11 | 194 | 194 | 5,394196 | 194 | 6.020,5 | cascada: ms = decider_4b + decider_4b_solrev_raw por registro |
| `llm_gpt61sol_low_disc` | 67,7 | 11/11 | 194 | 194 | 1,927948 | 194 | 2.304,5 | — |
| `jev_cascade_audit` | 67,6 | 11/11 | 194 | 194 | 0,084987 | 194 | 1.730 | cascada: ms = jev_v3 + jev_cascade_raw por registro; rotulado «Jev→Jev» en la figura |
| `llm_haiku55_off_disc` | 67,4 | 11/11 | 194 | 194 | 0,161984 | 194 | 1.288,5 | — |
| `decider_4b_llmrev_review` | 67,1 | 11/11 | 194 | 194 | 0,54073 | 194 | 8.800 | cascada: ms = decider_4b + decider_4b_llmrev_raw por registro |
| `llm_qwen38_27b_arcgguf_inject_disc` | 66,8 | 11/11 | 194 | 0 | — | 194 | 3.421,5 | sin factura API registrada |
| `llm_qwen38_27b_nvfp4_inject_disc` | 66,7 | 11/11 | 194 | 0 | — | 194 | 2.213 | sin factura API registrada |
| `llm_qwen38_27b_fp8_jev71_off_d0_disc` | 66,6 | 11/11 | 194 | 0 | — | 194 | 2.636 | sin factura API registrada; rotulado «Qwen FP8» en la figura |
| `medgemma_27b_jev77_jevrev_audit` | 66,5 | 11/11 | 194 | 194 | 0,050317 | 194 | 10.014 | cascada: ms = llm_medgemma_27b_it_bf16_jev77_d0_disc + medgemma_27b_jev77_jevrev_raw por registro |
| `dgemma_26b_a4b_nvfp4_s1_jevrev_review` | 66,1 | 11/11 | 194 | 194 | 0,050292 | 194 | 724,5 | cascada: ms = dgemma_26b_a4b_nvfp4_s1 + dgemma_26b_a4b_nvfp4_s1_jevrev_raw por registro |
| `jev114_cascade_audit` | 66,0 | 11/11 | 194 | 194 | 0,084992 | 194 | 1.078 | cascada: ms = jev_v114_typesafe_preview + jev114_cascade_raw por registro |
| `dgemma_26b_a4b_nvfp4_jevrev_review` | 66,0 | 11/11 | 194 | 194 | 0,050294 | 194 | 917 | cascada: ms = dgemma_26b_a4b_nvfp4 + dgemma_26b_a4b_nvfp4_jevrev_raw por registro |
| `llm_haiku55_off_prob` | 65,9 | 11/11 | 194 | 194 | 0,258596 | 194 | 1.656,5 | — |
| `decider_4b_jevrev_audit` | 65,6 | 11/11 | 194 | 194 | 0,050288 | 194 | 1.152 | cascada: ms = decider_4b + decider_4b_jevrev_raw por registro; rotulado «Dec4B→Jev» en la figura |
| `jev_1_14_cascade_audit` | 65,5 | 11/11 | 194 | 194 | 0,084991 | 194 | 1.177 | cascada: ms = jev_1_14 + jev_1_14_cascade_raw por registro |
| `dgemma_26b_a4b_nvfp4_s1_jevrev_audit` | 65,1 | 11/11 | 194 | 194 | 0,050292 | 194 | 724,5 | cascada: ms = dgemma_26b_a4b_nvfp4_s1 + dgemma_26b_a4b_nvfp4_s1_jevrev_raw por registro |
| `dgemma_26b_a4b_nvfp4_jevrev_audit` | 64,8 | 11/11 | 194 | 194 | 0,050294 | 194 | 917 | cascada: ms = dgemma_26b_a4b_nvfp4 + dgemma_26b_a4b_nvfp4_jevrev_raw por registro |
| `llm_gpt6luna_prob` | 64,6 | 11/11 | 194 | 194 | 0,193936 | 194 | 3.151,5 | — |
| `decider_4b_msrev_audit` | 63,5 | 11/11 | 194 | 194 | 0,038532 | 194 | 957 | cascada: ms = decider_4b + decider_4b_msrev_raw por registro |
| `llm_gpt6luna_disc` | 63,2 | 11/11 | 194 | 194 | 0,127915 | 194 | 1.896 | — |
| `llm_qwen38_27b_fp8_jev76_on_d0_disc` | 63,0 | 11/11 | 194 | 0 | — | 194 | 26.737 | sin factura API registrada |
| `llm_qwen38_27b_fp8_jev68_on_d0_prob` | 62,9 | 11/11 | 194 | 0 | — | 194 | 41.371 | sin factura API registrada |
| `decider_4b_jev114rev_audit` | 62,8 | 11/11 | 194 | 194 | 0,050288 | 194 | 742 | cascada: ms = decider_4b + decider_4b_jev114rev_raw por registro |
| `llm_cerebras_qwen38_27b_disc` | 62,2 | 11/11 | 194 | 194 | 1,508419 | 194 | 573 | — |
| `llm_cerebras_qwen38_27b_nostruct_disc` | 61,8 | 11/11 | 194 | 194 | 1,382517 | 194 | 462 | — |
| `llm_cerebras_qwen38_27b_low_prob` | 59,9 | 11/11 | 194 | 194 | 2,235089 | 194 | 766 | — |
| `decider_4b_clefrev_audit` | 58,7 | 11/11 | 194 | 194 | — | 194 | 2.296 | cascada: ms = decider_4b + decider_4b_clefrev_raw por registro; ceros registrados; sin gasto API externo; rotulado «Dec4B→Clef» en la figura |
| `mammoth_1_local` | 58,3 | 11/11 | 194 | 0 | — | 194 | 977 | sin factura API registrada |
| `mammoth_1_or` | 57,0 | 11/11 | 194 | 194 | — | 194 | 4.076,5 | ceros registrados; sin gasto API externo |
| `clef_27b` | 55,8 | 11/11 | 194 | 0 | — | 194 | 874 | sin factura API registrada |
| `decider_4b_llmrev_audit` | 54,6 | 11/11 | 194 | 194 | 0,54073 | 194 | 8.800 | cascada: ms = decider_4b + decider_4b_llmrev_raw por registro |
| `clef_27b_or` | 54,1 | 11/11 | 194 | 194 | 0,045451 | 194 | 765 | — |
| `elephant_1_local` | 53,6 | 11/11 | 194 | 0 | — | 194 | 337 | sin factura API registrada |
| `pplx_decider_v11_27b_or` | 53,3 | 11/11 | 194 | 194 | 0,038093 | 194 | 995,5 | — |
| `elephant_1_or` | 52,3 | 11/11 | 194 | 194 | — | 194 | 3.921,5 | ceros registrados; sin gasto API externo |
| `llm_qwen38_27b_nvfp4_nostruct_prob` | 52,1 | 11/11 | 194 | 0 | — | 194 | 5.287 | sin factura API registrada |
| `llm_qwen38_27b_fp8_inject_prob` | 51,9 | 11/11 | 194 | 0 | — | 194 | 6.503 | sin factura API registrada |
| `dgemma_26b_a4b_nvfp4_s1` | 51,8 | 11/11 | 194 | 0 | — | 194 | 122 | sin factura API registrada; rotulado «DGemma» en la figura |
| `decider_4b_d35rev_audit` | 51,8 | 11/11 | 194 | 194 | — | 194 | 722 | cascada: ms = decider_4b + decider_4b_d35rev_raw por registro; ceros registrados; sin gasto API externo |
| `decider_4b_drexrev_audit` | 51,6 | 11/11 | 194 | 194 | — | 194 | 2.129 | cascada: ms = decider_4b + decider_4b_drexrev_raw por registro; ceros registrados; sin gasto API externo |
| `llm_qwen38_27b_fp8_nostruct_t0_prob` | 51,6 | 11/11 | 194 | 0 | — | 194 | 6.485 | sin factura API registrada |
| `dgemma_26b_a4b_nvfp4` | 51,6 | 11/11 | 194 | 0 | — | 194 | 318 | sin factura API registrada |
| `llm_qwen38_27b_nvfp4_inject_prob` | 50,7 | 11/11 | 194 | 0 | — | 194 | 5.249,5 | sin factura API registrada |
| `mercury_decide_or` | 50,5 | 11/11 | 194 | 194 | 0,014504 | 194 | 815,5 | — |
| `jev_v114_typesafe_preview` | 50,3 | 11/11 | 194 | 194 | 0,034684 | 194 | 537 | — |
| `llm_qwen38_27b_fp8_jev68_off_d0_prob` | 50,0 | 11/11 | 194 | 0 | — | 194 | 6.247,5 | sin factura API registrada |
| `jev_1_14` | 49,8 | 11/11 | 194 | 194 | 0,034684 | 194 | 593,5 | — |
| `jev_luna_decisions` | 49,7* | 7/11 | 194 | 188 | ≥0,099886 | 194 | 675,5 | coste parcial o cota inferior (coste conocido en 188/194 registros); rotulado «luna-dec» en la figura |
| `jev_v3` | 49,3 | 11/11 | 194 | 194 | 0,034684 | 194 | 638 | rotulado «Jev» en la figura |
| `llm_qwen38_27b_fp8_nostruct_prob` | 49,2 | 11/11 | 194 | 0 | — | 194 | 6.368 | sin factura API registrada |
| `llm_dgemma_26b_a4b_nvfp4_nostruct_disc_rp` | 49,0 | 11/11 | 194 | 0 | — | 194 | 516 | sin factura API registrada |
| `llm_qwen38_27b_arcgguf_inject_prob` | 48,5 | 11/11 | 194 | 0 | — | 194 | 7.527 | sin factura API registrada |
| `decider_4b_clefflashrev_audit` | 48,2 | 11/11 | 194 | 194 | — | 194 | 541 | cascada: ms = decider_4b + decider_4b_clefflashrev_raw por registro; ceros registrados; sin gasto API externo |
| `llm_qwen38_27b_gguf81_nostruct_prob` | 48,0 | 11/11 | 194 | 0 | — | 194 | 10.738 | sin factura API registrada |
| `jev_ms_decision1` | 47,3 | 11/11 | 194 | 194 | 0,021242 | 194 | 693 | rotulado «MS-Dec1» en la figura |
| `nimble_9b` | 46,9 | 11/11 | 194 | 0 | — | 194 | 1.619,5 | sin factura API registrada |
| `decider_4b_nimblerev_audit` | 45,9 | 11/11 | 194 | 194 | — | 194 | 7.629,5 | cascada: ms = decider_4b + decider_4b_nimblerev_raw por registro; ceros registrados; sin gasto API externo |
| `clef_flash_or` | 44,7 | 11/11 | 194 | 194 | 0,019517 | 194 | 720,5 | — |
| `clef_omni_or` | 44,7 | 11/11 | 194 | 194 | 0,130628 | 194 | 530 | — |
| `clef_flash_9b_xpu` | 44,6 | 11/11 | 194 | 0 | — | 194 | 142 | sin factura API registrada |
| `llm_ministral3b_med_disc` | 44,5* | 5/11 | 194 | 0 | — | 194 | 1.917 | sin factura API registrada |
| `drex_v15_9b` | 43,7 | 11/11 | 194 | 0 | — | 194 | 381 | sin factura API registrada; rotulado «Drex» en la figura |
| `classify1_or` | 43,1 | 11/11 | 194 | 194 | 0,10409 | 194 | 691,5 | — |
| `drex_v20_or` | 41,9 | 11/11 | 194 | 194 | 0,028563 | 194 | 844,5 | — |
| `drex_v15_or` | 40,8 | 11/11 | 194 | 194 | 0,019042 | 194 | 875 | — |
| `jev_luna_decisions_fb` | 40,6 | 11/11 | 194 | 194 | 0,100639 | 194 | 671 | — |
| `solar_decide_or` | 39,9 | 11/11 | 194 | 194 | 0,160891 | 194 | 9.286,5 | — |
| `oai_luna_decisions` | 39,8 | 11/11 | 194 | 194 | 0,105666 | 194 | 441 | — |
| `decider_4b_cascade_audit` | 39,2* | 9/11 | 154 | 154 | — | 154 | 614 | cascada: ms = decider_4b + decider_4b_cascade_raw por registro; ceros registrados; sin gasto API externo |
| `decider_4b_aj32brev_audit` | 38,9 | 11/11 | 194 | 194 | — | 194 | 9.176,5 | cascada: ms = decider_4b + decider_4b_aj32brev_raw por registro; ceros registrados; sin gasto API externo |
| `decider_35b_a3b` | 38,8 | 11/11 | 194 | 0 | — | 194 | 675 | sin factura API registrada |
| `solar_decide_flash_or` | 36,9 | 11/11 | 194 | 194 | 0,160891 | 194 | 1.029,5 | — |
| `llm_cerebras_gptoss120b_low_prob` | 36,4 | 11/11 | 194 | 194 | 0,621215 | 194 | — | ms de cliente no comparables |
| `decider_4b` | 33,8 | 11/11 | 194 | 0 | — | 194 | 200 | sin factura API registrada; rotulado «Decider-4B» en la figura |
| `decider_35b_a3b_nvfp4` | 33,2 | 11/11 | 194 | 0 | — | 194 | 185 | sin factura API registrada |
| `liquid_d1_or` | 32,5 | 11/11 | 194 | 194 | 0,03135 | 194 | 610 | — |
| `tev1_4b_or` | 31,8 | 11/11 | 194 | 194 | 0,082287 | 194 | 784 | — |
| `kev_4b_or` | 30,7 | 11/11 | 194 | 194 | 0,019994 | 194 | 938,5 | — |
| `decider_4b_aj8brev_audit` | 27,7 | 11/11 | 194 | 194 | — | 194 | 2.750 | cascada: ms = decider_4b + decider_4b_aj8brev_raw por registro; ceros registrados; sin gasto API externo |
| `tev1_4b` | 27,0 | 11/11 | 194 | 0 | — | 194 | 452 | sin factura API registrada |
| `llm_medgemma_27b_it_bf16_jev77_d0_disc` | 23,7 | 11/11 | 194 | 0 | — | 194 | 9.387 | sin factura API registrada |
| `anyjev_qwen3_32b_l0` | 21,2 | 11/11 | 194 | 0 | — | 194 | 2.585,5 | sin factura API registrada |
| `decider_2b` | 19,5 | 11/11 | 194 | 0 | — | 194 | 78 | sin factura API registrada |
| `strands_2b_hobson_v19_xpu_trunc` | 19,4 | 11/11 | 194 | 0 | — | 194 | 124,5 | sin factura API registrada |
| `span01_lite_or` | 19,1 | 11/11 | 194 | 194 | — | 194 | 588 | ceros registrados; sin gasto API externo |
| `span01_pro` | 18,5 | 11/11 | 194 | 194 | 0,016099 | 194 | 589 | — |
| `strands_2b_hobson_v19_xpu` | 17,9* | 10/11 | 194 | 0 | — | 194 | 125 | sin factura API registrada |
| `llm_gemma3_27b_it_bf16_jev77_d0_disc` | 13,7 | 11/11 | 194 | 0 | — | 194 | 9.418 | sin factura API registrada |
| `decider_0.8b` | 13,1 | 11/11 | 194 | 0 | — | 194 | 43 | sin factura API registrada |
| `anyjev_qwen3_8b_l0` | 12,7 | 11/11 | 194 | 0 | — | 194 | 702 | sin factura API registrada |
| `span01_lite` | 4,5 | 11/11 | 194 | 194 | — | 194 | 874 | ceros registrados; sin gasto API externo |
| `gliner_decide_desc` | -2,4 | 11/11 | 194 | 0 | — | 194 | 42 | sin factura API registrada |
| `anyjev_qwen3_1.7b_l0` | -3,0 | 11/11 | 194 | 0 | — | 194 | 186 | sin factura API registrada |
| `tev1_0.8b` | -8,8 | 11/11 | 194 | 0 | — | 194 | 142 | sin factura API registrada |
| `llm_ministral3b_med_prob` | -9,8* | 4/11 | 194 | 0 | — | 194 | 4.780,5 | sin factura API registrada |
| `llm_qwen38_27b_prob` | -17,3* | 9/11 | 194 | 0 | — | 192 | 6.737 | sin factura API registrada |
| `laya_router` | -21,9 | 11/11 | 194 | 0 | — | 194 | 28 | sin factura API registrada |
| `clm_v0.1_8b` | -41,0 | 11/11 | 194 | 0 | — | 194 | 80 | sin factura API registrada |
| `llm_qwen38flash_prob` | -42,8* | 8/11 | 194 | 0 | — | 190 | 49.923,5 | sin factura API registrada |
| `julia_1` | -89,4 | 11/11 | 194 | 0 | — | 194 | 564,5 | sin factura API registrada |
