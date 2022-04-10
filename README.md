# FastBGT_AD
This work is based on Apache Spark, please configure spark enviroment using appropriate Spark configuration files for your own settings. Note: For ```N <= 20```, please assign at least 32g memory for the driver and each executor by doing ```--driver-memory 32g``` and ```--executor-memory 32g``` For ```N >= 20```, please consider assigning all available memories for driver and executor. Ex. ```N=30``` requires at least 128g memory.

To run statitical analysis using FastBGT (e.g, N subjects, 9 risk patterns: 0.02, 1-mix, 2-mix, 3-mix, 4-mix, 0.05, 0.1, 0.15, 0.2, each with 4 tree schemes), Please launch applications through bgtf_start_statistical_analysis.sh following the example below:

```./bgtf_start_statistical_analysis.sh <N> <Risk Pattern> <Tree Schemes>```

For ```<Risk Pattern>```

1 : 0.02

2 : 1-mix

3 : 2-mix

4 : 3-mix

5 : 4-mix

6 : 0.05

7 : 0.1

8 : 0.15

9 : 0.2

For ```<Tree Schemes>```

1 : Multi-tree

2 : Single-tree

3 : Hybrid tree

4 : Hybrid tree with Cross Pruning

The simulation will generate a set of statistical and performance evaluation summary, named by ```<N>-<Risk-Pattern>-<Test Selection Rule>-<MM-DD-YYYY HH-MM-SS>.csv```, indicating which pool setting is used for the set of statistical analysis with an attached time stamp.



To run BHA using FastBGT (e.g ```N``` subjects with 9 prior risk patterns). Please launch applications through bgtf_start_BHA.sh following the example below:

```./bgtf_start_BHA.sh <N>```


The simulation will generate a set of statistical and performance evaluation summary, named by ```LatticeBenchmark-N=<N>-<MM-DD-YYYY HH-MM-SS>.csv```, indicating which ```N``` is used for the set of simulaitons with an attached time stamp.