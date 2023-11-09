This repository contains the code for adaptiveMSA, a modified version of UPP that uses J-score instead of bitscore, along with a multi-armed bandit adaptive approach for assigning query sequences to HMMs in the UPP algorithm.
The repository for the original UPP code is here: https://github.com/smirarab/sepp

In order to install adaptiveMSA, follow the instructions for installing UPP in the flie tutorial/upp-tutorial.md, with the exception that  

`git clone https://github.com/smirarab/sepp.git`

should be replaced with:

`git clone https://github.com/ilanshom/adaptiveMSA.git` 

## Running the code

A default run for this modified version of UPP is called using the same command as UPP:

`run_upp.py -A 10 -B 1000 -M -1 -m molecule_type -s input`

The optional arguments we have added to UPP are described when the following command is typed into the terminal:
`run_upp.py -h`

We calso describe them here:

### kmer size
argument: `--kmersize k`
This determines the kmer size used by the algorithm for assigning query sequences to HMMs

### kmers to check
argument: `--kmers_to_check N`
This determines how many kmers in each round of the adaptive algorithm to sample from the query sequence in order to estimate the J-score for each of the HMMs for the current round of the adaptive algorithm.

### top sets to check
argument: `--top_sets_to_check T`
This determines how many of the top scoring HMMs for a query sequence to compute the J-score on after the adaptive estimation rounds are complete.  The HMM from this set with the best J-score computed from these top sets will be assigned to the query sequence.

### argument `--sample_rounds r`
This determines the umber of rounds of sampling in the adaptive estimation stage of the algorithm.










