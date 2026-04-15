# AXIOM-QUANTUM v1.0 Security Audit Report

**Run ID:** `run_20260416_004103`  **Timestamp:** 2026-04-16 00:41:03
**Engine:** QSVM v1.0 (vectorized quantum features + LinearSVC)
**Input:** `../Planck-99/someDEV/IoTsyscalls.csv`  **Qubits:** 8  **Hilbert dim:** 256

## Training Metrics

| Metric | Hold-out | 5-fold CV |
|--------|----------|-----------|
| **Accuracy** | **0.9595** | **0.9631** |
| **Precision** | **0.9707** | **0.9686** |
| **Recall** | **0.9482** | **0.9578** |
| **F1-Score** | **0.9593** | **0.9632** |
| ROC-AUC | 0.9825 | -- |

## Inference Results

| Metric | Value |
|--------|-------|
| Total Records | 1504 |
| TP/FP/TN/FN | 1265/54/184/1 |
| **Precision** | **0.9591** |
| **Recall** | **0.9992** |
| **F1-Score** | **0.9787** |
| **Accuracy** | **0.9634** |
| FPR | 0.2269 |
| Mean Latency | 55.060 us |
| Throughput | 3,315 rec/s |
| Train time | 0.0 s |
| Determinism_Rate | 1.0000 |

## Per-Record Audit Trail (first 100)

| # | Record | True | Predicted | Score | Latency (us) | Result |
|---|--------|------|-----------|-------|--------------|--------|
| 1 | `REC_0000000` | malware | ANOMALOUS | +2.9808 | 118.00 | TP |
| 2 | `REC_0000001` | malware | ANOMALOUS | +2.7100 | 51.40 | TP |
| 3 | `REC_0000002` | benign | BENIGN | -1.9756 | 50.20 | TN |
| 4 | `REC_0000003` | malware | ANOMALOUS | +5.9685 | 61.30 | TP |
| 5 | `REC_0000004` | benign | BENIGN | -2.0949 | 49.20 | TN |
| 6 | `REC_0000005` | benign | ANOMALOUS | +0.5304 | 49.30 | FP |
| 7 | `REC_0000006` | malware | ANOMALOUS | +6.5032 | 49.30 | TP |
| 8 | `REC_0000007` | malware | ANOMALOUS | +2.5553 | 45.60 | TP |
| 9 | `REC_0000008` | benign | BENIGN | -1.4179 | 48.10 | TN |
| 10 | `REC_0000009` | benign | BENIGN | -0.7727 | 49.40 | TN |
| 11 | `REC_0000010` | malware | ANOMALOUS | +6.4279 | 49.30 | TP |
| 12 | `REC_0000011` | malware | ANOMALOUS | +6.2330 | 49.20 | TP |
| 13 | `REC_0000012` | malware | ANOMALOUS | +5.2321 | 48.80 | TP |
| 14 | `REC_0000013` | malware | ANOMALOUS | +5.0396 | 48.90 | TP |
| 15 | `REC_0000014` | benign | BENIGN | -2.7936 | 96.70 | TN |
| 16 | `REC_0000015` | benign | BENIGN | -1.4484 | 83.30 | TN |
| 17 | `REC_0000016` | malware | ANOMALOUS | +6.2297 | 49.00 | TP |
| 18 | `REC_0000017` | benign | BENIGN | -3.6892 | 49.20 | TN |
| 19 | `REC_0000018` | malware | ANOMALOUS | +5.0763 | 48.80 | TP |
| 20 | `REC_0000019` | benign | BENIGN | -0.4928 | 49.30 | TN |
| 21 | `REC_0000020` | malware | ANOMALOUS | +5.8018 | 49.20 | TP |
| 22 | `REC_0000021` | malware | ANOMALOUS | +6.1279 | 49.30 | TP |
| 23 | `REC_0000022` | malware | ANOMALOUS | +3.0637 | 49.90 | TP |
| 24 | `REC_0000023` | malware | ANOMALOUS | +6.4821 | 48.70 | TP |
| 25 | `REC_0000024` | malware | ANOMALOUS | +12.4900 | 48.40 | TP |
| 26 | `REC_0000025` | benign | BENIGN | -1.5172 | 48.70 | TN |
| 27 | `REC_0000026` | malware | ANOMALOUS | +14.8301 | 49.30 | TP |
| 28 | `REC_0000027` | malware | ANOMALOUS | +13.8098 | 48.90 | TP |
| 29 | `REC_0000028` | malware | ANOMALOUS | +5.5097 | 48.50 | TP |
| 30 | `REC_0000029` | malware | ANOMALOUS | +3.2986 | 49.60 | TP |
| 31 | `REC_0000030` | malware | ANOMALOUS | +5.0763 | 50.00 | TP |
| 32 | `REC_0000031` | malware | ANOMALOUS | +6.8074 | 49.30 | TP |
| 33 | `REC_0000032` | malware | ANOMALOUS | +6.3629 | 52.90 | TP |
| 34 | `REC_0000033` | benign | BENIGN | -1.9451 | 32.60 | TN |
| 35 | `REC_0000034` | malware | ANOMALOUS | +14.4006 | 30.90 | TP |
| 36 | `REC_0000035` | benign | BENIGN | -0.4782 | 30.00 | TN |
| 37 | `REC_0000036` | malware | ANOMALOUS | +25.7613 | 30.00 | TP |
| 38 | `REC_0000037` | malware | ANOMALOUS | +6.4557 | 29.50 | TP |
| 39 | `REC_0000038` | malware | ANOMALOUS | +2.2258 | 28.90 | TP |
| 40 | `REC_0000039` | malware | ANOMALOUS | +5.8018 | 28.50 | TP |
| 41 | `REC_0000040` | malware | ANOMALOUS | +5.9222 | 28.40 | TP |
| 42 | `REC_0000041` | malware | ANOMALOUS | +6.2144 | 29.00 | TP |
| 43 | `REC_0000042` | malware | ANOMALOUS | +14.6723 | 28.30 | TP |
| 44 | `REC_0000043` | malware | ANOMALOUS | +13.6783 | 28.40 | TP |
| 45 | `REC_0000044` | benign | BENIGN | -1.2480 | 28.60 | TN |
| 46 | `REC_0000045` | malware | ANOMALOUS | +5.8703 | 28.50 | TP |
| 47 | `REC_0000046` | malware | ANOMALOUS | +6.3728 | 28.30 | TP |
| 48 | `REC_0000047` | malware | ANOMALOUS | +5.8018 | 28.30 | TP |
| 49 | `REC_0000048` | malware | ANOMALOUS | +6.9670 | 28.10 | TP |
| 50 | `REC_0000049` | malware | ANOMALOUS | +3.2989 | 28.00 | TP |
| 51 | `REC_0000050` | malware | ANOMALOUS | +5.4124 | 66.60 | TP |
| 52 | `REC_0000051` | malware | ANOMALOUS | +12.5952 | 44.60 | TP |
| 53 | `REC_0000052` | malware | ANOMALOUS | +5.5418 | 72.30 | TP |
| 54 | `REC_0000053` | malware | ANOMALOUS | +21.8006 | 28.70 | TP |
| 55 | `REC_0000054` | malware | ANOMALOUS | +6.0219 | 27.80 | TP |
| 56 | `REC_0000055` | malware | ANOMALOUS | +2.2861 | 28.00 | TP |
| 57 | `REC_0000056` | malware | ANOMALOUS | +2.4334 | 28.00 | TP |
| 58 | `REC_0000057` | malware | ANOMALOUS | +5.8067 | 28.20 | TP |
| 59 | `REC_0000058` | malware | ANOMALOUS | +12.4503 | 28.00 | TP |
| 60 | `REC_0000059` | malware | ANOMALOUS | +5.4059 | 28.00 | TP |
| 61 | `REC_0000060` | malware | ANOMALOUS | +2.4135 | 28.40 | TP |
| 62 | `REC_0000061` | malware | ANOMALOUS | +2.3296 | 28.00 | TP |
| 63 | `REC_0000062` | malware | ANOMALOUS | +11.8464 | 28.00 | TP |
| 64 | `REC_0000063` | malware | ANOMALOUS | +8.4815 | 28.20 | TP |
| 65 | `REC_0000064` | malware | ANOMALOUS | +5.4836 | 54.20 | TP |
| 66 | `REC_0000065` | benign | BENIGN | -0.4377 | 104.00 | TN |
| 67 | `REC_0000066` | malware | ANOMALOUS | +10.9807 | 32.90 | TP |
| 68 | `REC_0000067` | malware | ANOMALOUS | +6.2383 | 32.10 | TP |
| 69 | `REC_0000068` | benign | BENIGN | -1.0621 | 31.60 | TN |
| 70 | `REC_0000069` | malware | ANOMALOUS | +6.5788 | 53.20 | TP |
| 71 | `REC_0000070` | malware | ANOMALOUS | +6.3110 | 62.40 | TP |
| 72 | `REC_0000071` | malware | ANOMALOUS | +2.4334 | 29.40 | TP |
| 73 | `REC_0000072` | malware | ANOMALOUS | +4.7279 | 28.30 | TP |
| 74 | `REC_0000073` | malware | ANOMALOUS | +14.0252 | 27.80 | TP |
| 75 | `REC_0000074` | benign | BENIGN | -1.9602 | 39.80 | TN |
| 76 | `REC_0000075` | malware | ANOMALOUS | +6.3821 | 27.70 | TP |
| 77 | `REC_0000076` | malware | ANOMALOUS | +6.1727 | 27.90 | TP |
| 78 | `REC_0000077` | malware | ANOMALOUS | +6.7401 | 27.70 | TP |
| 79 | `REC_0000078` | malware | ANOMALOUS | +6.5917 | 27.70 | TP |
| 80 | `REC_0000079` | malware | ANOMALOUS | +21.5868 | 29.10 | TP |
| 81 | `REC_0000080` | malware | ANOMALOUS | +13.4487 | 28.80 | TP |
| 82 | `REC_0000081` | malware | ANOMALOUS | +6.5694 | 28.60 | TP |
| 83 | `REC_0000082` | malware | ANOMALOUS | +26.1945 | 28.90 | TP |
| 84 | `REC_0000083` | malware | ANOMALOUS | +13.7704 | 39.70 | TP |
| 85 | `REC_0000084` | malware | ANOMALOUS | +2.4135 | 30.00 | TP |
| 86 | `REC_0000085` | malware | ANOMALOUS | +6.5326 | 28.70 | TP |
| 87 | `REC_0000086` | malware | ANOMALOUS | +6.3213 | 28.50 | TP |
| 88 | `REC_0000087` | malware | ANOMALOUS | +12.9612 | 28.10 | TP |
| 89 | `REC_0000088` | malware | ANOMALOUS | +5.9962 | 28.40 | TP |
| 90 | `REC_0000089` | malware | ANOMALOUS | +5.3475 | 28.30 | TP |
| 91 | `REC_0000090` | malware | ANOMALOUS | +14.6369 | 28.40 | TP |
| 92 | `REC_0000091` | malware | ANOMALOUS | +3.6401 | 28.00 | TP |
| 93 | `REC_0000092` | malware | ANOMALOUS | +12.4950 | 28.80 | TP |
| 94 | `REC_0000093` | benign | BENIGN | -4.0914 | 28.80 | TN |
| 95 | `REC_0000094` | malware | ANOMALOUS | +14.0842 | 72.80 | TP |
| 96 | `REC_0000095` | malware | ANOMALOUS | +13.1549 | 47.80 | TP |
| 97 | `REC_0000096` | malware | ANOMALOUS | +3.6039 | 46.10 | TP |
| 98 | `REC_0000097` | benign | ANOMALOUS | +0.5080 | 29.00 | FP |
| 99 | `REC_0000098` | malware | ANOMALOUS | +26.1945 | 29.00 | TP |
| 100 | `REC_0000099` | malware | ANOMALOUS | +13.9653 | 28.60 | TP |

*... 1404 more records in audit_trail.json*

*AXIOM-QUANTUM v1.0*
