# MLST pipeline

by Judith Bergadà Pijuan

This pipeline is a tool to perform the assemlby of paired-end sequencing reads
and to scan the resulting contig files against PubMLST typing schemes.
Given multiple paired-end sequencing reads (FASTQ files),
it provides a tab-separated table showing the matching PubMLST per paired-files,
their ST (sequence type), and their allele IDs.

## Installation

To use this pipeline, you need to install the following dependencies:
- SPAdes
- MLST

Later, you need to download the tool:
```bash
cd $HOME
git clone https://github.com/judithbergada/Pipeline_MLST
```

## Usage

The pipeline expects you to have the following folder:
- FASTQ folder: this is a folder containg only your sequencing reads (FASTQ files).
You must have all your FASTQ files here, and it is important that the pairs of files have the
same prefix in the name.

To get information about the usage, please try:

```bash
./mlstpipeline.sh -h
```

The MLST tool can be used with these parameters:

```
Usage: mlstpipeline     [-h or --help]
                        [-f or --fastqfolder]
                        [-o or --outname]
                        [-t or --threads]

Optional arguments:
    -h, --help:
                Show this help message and exit.
    -o, --outname:
                Name of your analysis.
                It will be used to name the output files.
                Default: mymlst.
    -t, --threads:
                Number of threads that will be used.
                It must be an integer.
                Default: 8.
Required arguments:
    -f, --fastqfolder:
                Path to the folder that contains ALL your FASTQ files.
                Only FASTQ files should be placed in it.
                You need forward and reverse paired-end reads.
```

Enjoy using the tool!

