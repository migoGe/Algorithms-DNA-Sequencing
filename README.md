# Algorithms for DNA Sequencing
![](docs/double_helix.png)
* [Johns Hopkins University](https://www.jhu.edu/)

## [Week 1: DNA Sequencing, Strings and Matching](1_week)
### Lectures
1. [Introduction](1_week/docs/intro.pdf)
2. [Why Study This?](1_week/docs/why_study_this.pdf)
3. [DNA sequencing past and present](1_week/docs/DNA_seq_past_present.pdf)
4. [Genomes as strings, reads as substrings](1_week/docs/genomes_strings.pdf)
5. [String definitions and Python examples](1_week/docs/python_str_def_ex.pdf)
6. [How DNA gets copied](1_week/docs/DNA_copying.pdf)
7. [How second-generation sequencers work](1_week/docs/second_gen_parallel.pdf)
8. [Sequencing errors and base qualities](1_week/docs/seq_errors_base_qualities.pdf)
9. [Working with sequencing reads (FASTQ format)](1_week/docs/fastq_format.pdf)
10. [Sequencers give pieces to genomic puzzles](1_week/docs/pieces_fragmentary.pdf)
    * Unrelated humans have genomes of ~3 billion base pairs which are 99.8 - 99.9% similar
11. [Read alignment and why it's hard](1_week/docs/read_alignment_hard.pdf)
12. [Naive exact matching](1_week/docs/naive_exact_matching.pdf)

### Notes and Assignments
* [1_notebook.ipynb](1_week/1_notebook.ipynb)
    * [.html](1_week/1_notebook.html)
    
### Resources
* [ERR037900_1.first1000.fastq](1_week/ERR037900_1.first1000.fastq)
* [lambda_virus.fa](1_week/lambda_virus.fa)

## [Week 2: Preprocessing, Indexing, and Approximate Matching](2_week)
### Lectures
1. [Boyer-Moore: Basics](2_week/docs/boyer-moore.pdf)
2. [Boyer-Moore: Putting It All Together](2_week/docs/boyer-moore-together.pdf)
3. [Diversion: Repetitive Elements](2_week/docs/repetitive_elements.pdf)
4. [Preprocessing](2_week/docs/preprocessing.pdf)
5. [Indexing and K-mers](2_week/docs/indexing_kmers.pdf)
6. [Data Structures for Indexing](2_week/docs/data_structures.pdf)
7. [Hash Tables for Indexing](2_week/docs/hash_tables.pdf)
8. [Variations on K-mer Indexes](2_week/docs/indexing_variations.pdf)
9. [Indexing by Suffix](2_week/docs/suffix.pdf)
10. [Approximate Matching, Hamming, and Edit Distance](2_week/docs/approximate.pdf)
11. [Pigeonhole Principle](2_week/docs/pigeonhole.pdf)

### Notes and Assignments
* [2_notebook.ipynb](2_week/2_notebook.ipynb) 
    * [.html](2_week/2_notebook.html)
    
### Resources
* [bm_preproc.py](bm_preproc.py)
* [k-mer_index.py](k-mer_index.py)
* [chr1.GRCh38.excerpt.fasta](chr1.GRCh38.excerpt.fasta)

## [Week 3: Edit Distance, Assembly, and Overlaps](3_week)
### Lectures
1. [Edit Distance (part 1)](3_week/docs/edit_dist1.pdf)
2. [Edit Distance (part 2)](3_week/docs/edit_dist2.pdf)
3. [Edit Distance (part 3)](3_week/docs/edit_dist3.pdf)
4. [Edit Distance (part 4)](3_week/docs/edit_dist4.pdf)
    * Primary difference between edit distance and global alignment is the ability
    to apply a weighted penalty to substitutions and indels (insertion/deletions)
5. [Global and Local Alignment](3_week/docs/global_and_local_alignment.pdf)
    * Human transition to transversion ratio (aka. ti/tv) is ~2.1
        * purines
            * adenine
            * guanine
        * pyrimidines
            * cytosine
            * thymine
        * transitions occur for subsitutions in the same category
            * *examples:*
                * ```A -> G```
                * ```C -> T```
        * tranversions occur for subsitutions in different categories
            * *examples:*
                * ```A -> C```
                * ```G -> T```
    * Human substitution rate is ~1 in 1,000
    * Small-gap rate is ~1 in 3,000
        * aka. indels (insertion/deletions)
6. [De Novo Shotgun Assembly](3_week/docs/assembly_basics.pdf)
    * De Novo
        * starting from scratch
    * Shotgun
        * reads from all over the genome
7. [Overlaps and Coverage](3_week/docs/overlaps_and_coverage.pdf)
    * First rule of assembly
        * If the suffix of read A is similar to the prefix of read B then A and B might overlap in the genome
    * Second rule of assembly
        * More coverage leads to more and longer overlaps
8. [Overlap Graph](3_week/docs/overlap_graph.pdf)

### Resources
* [chr1.GRCh38.excerpt.fasta](chr1.GRCh38.excerpt.fasta)

## External Resources
* [Lectures](https://github.com/BenLangmead/ads1-slides)
* [Jupyter Notebooks](https://github.com/BenLangmead/ads1-notebooks)
* [Jupyter.org](https://jupyter.org/)
* [Fast Algorithms for Signal Processing](docs/Fast_Algorithms_for_Signal_Processing.pdf)

## Supplemental

* Jupyter Notebooks can be executed from the command line:

```
$ jupyter notebook 1_notebook.ipynb
[I 11:45:05.991 NotebookApp] The Jupyter Notebook is running at:
[I 11:45:05.991 NotebookApp] http://localhost:8889/?token=070644d6de70204df12235b2356476b577d0744b5df41422
[I 11:45:05.991 NotebookApp]  or http://127.0.0.1:8889/?token=070644d6de70204df12235b2356476b577d0744b5df41422
[I 11:45:05.991 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 11:45:05.998 NotebookApp] 
    
    To access the notebook, open this file in a browser:
        file:///Users/.../Library/Jupyter/runtime/nbserver-38748-open.html
    Or copy and paste one of these URLs:
        http://localhost:8889/?token=070644d6de70204df12235b2356476b577d0744b5df41422
     or http://127.0.0.1:8889/?token=070644d6de70204df12235b2356476b577d0744b5df41422
```