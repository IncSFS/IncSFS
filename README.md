## Artifact
This is artifact evaluation of Submission 1456
We provide a Docker image that contains all necessary benchmarks, dependencies, and executable files required to reproduce our experimental results. The image has been tested successfully on our local machine.


## Start
```
$ docker pull annoymousforpaper/incsfsase:v1
docker run -it -name incsfs annoymousforpaper/incsfsase:v1 /bin/bash
docker exec -it incsfs /bin/bash
```

## Run an example
```
cd /home/example
./run_example.sh
```

## Viewing Results Directly
If you only wish to view the final tables/figures without re-running the experiments, you can directly execute the following scripts
### RQ1:Overall Performance Comparison
```
cd /home/script
python3 printAllTable.py
```

### RQ2:SILVA Benchmark Evaluation
```
cd /home/script
python3 printSILVATable.py
```
### RQ3:Trend Analysis
```
cd /home/script
python3 printTrendGraph.py

### RQ4:Analysis of Consistency
```
cd /home/script
python3 printNotEqual.py
python3 printEqualGraph.py
```

## Reproduce Experimental Results
To reproduce the results reported in our paper, follow the instructions below for each research question (RQ).
### RQ1:Overall Performance Comparison
```
cd /home/script
./run_incsfs.sh
python3 printAllTable.py
```
### RQ2:SILVA Benchmark Evaluation
```
cd /home/script
./run_silva.sh
python3 printSILVATable.py
```
### RQ3: Trend Analysis
```
cd /home/script
python3 ./run_trend.sh
python3 printTrendGraph.py
```
### RQ4:Analysis of Consistency
After running the script for RQ1, proceed to execute the following script to reproduce the result of RQ3
```
cd /home/script
python3 printNotEqual.py
python3 printEqualGraph.py
```
