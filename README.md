## DomBpred:

DomBpred: protein domain boundary predictor using inter-residue distance and domain-residue level clustering



## Developer:

Zhongze Yu and Chunxiang Peng

College of Information Engineering

Zhejiang University of Technology, Hangzhou 310023, China

Email: zhongze0820@163.com, pengcx@zjut.edu.cn



## Contact:

Guijun Zhang, Prof

College of Information Engineering

Zhejiang University of Technology, Hangzhou 310023, China

Email: zgj@zjut.edu.cn



## INSTALLATION

- Python > 3.5
- HMMER (Jackhmmer is one of the HMMER toolkits, it's used to search the MSA of the target sequence from SDSL) (Download link: http://www.hmmer.org/)
- PSIPRED (it's used to predict the secondary structure of the target sequence) (Online server link: http://bioinf.cs.ucl.ac.uk/psipred/) (Download link: http://bioinfadmin.cs.ucl.ac.uk/downloads/psipred/)
- trRosetta(it's used to predict the distance profile of the target sequence) (Online server link: https://yanglab.nankai.edu.cn/trRosetta/)



## RUNNING

```+python
# DomBpred.py

# arguments:
#    input		Paths of various input files, including sequence file, msa file, ss2 file and distance file
#    output		Path of output result.

"""
optional arguments:
	-seq_path	The path of the target sequence to be decomposed.
	-msa_path	The path of the MSA file generated by jackhmmer of the target sequence.
	-ss2_path	The path of the predicted ss2 file of the target sequence to be decomposed.
	-dist_path	The path of the predicted distance file of the target sequence to be decomposed. Its dimension is L*L*1.
	-log		The path of DomBpred result. If this parameter is missing, it will be directly output to the console.
"""
```

- Predicting

python  ./DomBpred.pyc  -seq_path=./example/2cbla.fasta  -msa_path=./example/2cbla.txt  -ss2_path=./example/2cbla.ss2  -dist_path=./example/2cbla.npz  -log=./result.txt

- Use jackhmmer to search for msa

jackhmmer  --notextw  -A  ./XXXmsa.txt  XXX.fasta  SDSL.txt



## DISCLAIMER

The executable software and the source code of DomBpred is distributed free of charge as it is to any non-commercial users. The authors hold no liabilities to the performance of the program.

