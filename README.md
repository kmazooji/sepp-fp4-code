This repository contains the code for adaptiveMSA, a modified version of UPP that uses J-score instead of bitscore, along with a multi-armed bandit adaptive approach for assigning query sequences to HMMs in the UPP algorithm.
The repository for the original UPP code is here: https://github.com/smirarab/sepp

In order to install adaptiveMSA, follow the instructions for installing UPP in the flie tutorial/upp-tutorial.md, with the exception that  

`git clone https://github.com/smirarab/sepp.git`

should be replaced with:

`git clone https://github.com/ilanshom/adaptiveMSA.git` 

## Run Options

A default run for this modified version of UPP is called using the same command as UPP:

'run_upp.py -A 10 -B 1000 -M -1 -m molecule_type -s input'

### kmer size







