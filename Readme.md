# First Pliot results (Under-Dev)

Okay, This is the first results of R&D on unseen dataset that reachs to 51 times of the max training squence count, the same data been used to train (Planck-99)[https://github.com/Division-36/Planck-99_PublicBenchmarks] , Planck already is the current SOTA but I made Axiom-Qsecurity Because I was bored as I said in my github profile... Enjoy


## Model Sizes
```
_production.pkl 4.5 Kb
_production.h   915 B (yeah it's in bytes not KB, you need time to realize that)
```

Results
➜  Axiom-Qsecurity python benchmark.py --csv ../Planck-99/someDEV/IoTsyscalls.csv --load-model _production.pkl

+==============================================================================+
|  AXIOM-QUANTUM v1    |  Security Audit Engine  [QSVM + C ENGINE]            |
|  Vectorized Quantum Features | LinearSVC | ~100% Precision | Fast path      |
+==============================================================================+

  Loading: ../Planck-99/someDEV/IoTsyscalls.csv
  Loaded 1504 records (1266 malware, 238 benign)

  Loading pre-trained model: _production.pkl
  Model OK | acc=0.9595  prec=0.9707  mode=fast


  +-- Compiling C Engine -------
  Compiling C engine from model ...
  [C Engine] Generating C source ...
  [C Engine] Source written: axiom_engine.c (17,056 chars)
  [C Engine] Compiled in 14167 ms -> axiom_engine.so
  [C Engine] Shared library loaded
  C engine ready in 15064 ms
  [C Engine] Generating C source ...
  [C Engine] Source written: axiom_engine.c (17,056 chars)
  [C Engine] Compiled in 4064 ms -> axiom_engine.so
  [C Engine] Shared library loaded
  Demo binary: benchmarks/run_20260416_004103/axiom_demo

  +-- Batch Inference (1504 records) -------
  Batch inference (1504 records) ...
  Done: 453.6 ms | 55.060 us/rec | 3,315 rec/s


  +-- C Demo ---------------------------------------------------

  [BENIGN  ] features=[REDACTED]
    AXIOM-QUANTUM v3.1 C Inference Engine
    Features [ exec net io mem priv stealth bgent div ]:
      [REDACTED]

      Decision  : BENIGN
      SVM Score : -11.504249
      Latency   : 975500 ns  (975.500 us)

    Batch 100000 records: 3832.7ms | 38.327 us/rec | 26091 rec/s

  [MALWARE ] features=[REDACTED]
    AXIOM-QUANTUM v3.1 C Inference Engine
    Features [ exec net io mem priv stealth bgent div ]:
      [REDACTED]

      Decision  : ANOMALOUS (MALWARE)
      SVM Score : +32.211083
      Latency   : 129500 ns  (129.500 us)

    Batch 100000 records: 4551.5ms | 45.515 us/rec | 21971 rec/s
  +--------------------------------------------------------------

  Writing artifacts ...
  Generating charts ...
  Charts done
==================================================================================
  AXIOM-QUANTUM v3.1  |  run_20260416_004103
==================================================================================

  Metric                                Value   Metric                        Value
..................................................................................
  Total Records                          1504   True Positives                 1265
  Malware in dataset                     1266   False Positives                  54
  Benign in dataset                       238   True Negatives                  184
                                                False Negatives                   1
..................................................................................
  CV Accuracy                          0.9631   Accuracy                     0.9634
  CV Precision                         0.9686   Precision                    0.9591
  CV Recall                            0.9578   Recall                       0.9992
  CV F1                                0.9632   F1-Score                     0.9787
..................................................................................
  Mean Latency                      55.060 us   Throughput               3,315 rec/s
  Train time                            0.0 s   C compile                  15064 ms
  FPR                                  0.2269   Det.Rate                     1.0000
----------------------------------------------------------------------------------

  Output -> /mnt/c/Users/dell/Desktop/Axiom-Qsecurity/benchmarks/run_20260416_004103
==================================================================================
