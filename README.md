# satelome

## Installation instruction

### 1. Install conda

```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

```bash
bash Miniconda3-latest-Linux-x86_64.sh
```

### 2. Create conda environment

```bash
conda create -n satelome python=3.9
```

### 3. Activate conda environment

```bash
conda activate satelome
```

### 4. Install requirements

```bash
pip install -r requirements.txt
```

## Toolset desciption

**main.py** - from fasta file to trf file
**trf_parse_raw** - from trf file to parsed trf with normalised monomer and joined overlapping repeats 

## Download test dataset

```bash
curl -OJX GET "https://api.ncbi.nlm.nih.gov/datasets/v2alpha/genome/accession/GCF_000146045.2/download?include_annotation_type=GENOME_FASTA,GENOME_GFF&filename=GCF_000146045.2.zip" -H "Accept: application/zip"
unzip GCF_000146045.2.zip
rm GCF_000146045.2.zip
```

## Backlog

Hypotesis to check:

Part A.

- large tandem repeats flanks contigs in centromere and telomere regions
- contig flanking is a good diagnostic feature for large tandem repeats searching

Tools to implement:

- tools that analazed genome dataset and search TR that flanks contigs
- and annotate that repeats
- and mark contigs that flank centromeric region

Part B.

- inside primates/carnivora/rodents/anumals exist taxon specific large tandem repeats
- inside primates/carnivora/rodents/anumals exist taxon-group specific large tandem repeats

Dataset to make:

- taxon to all large tandem repeats
- large tandem repeat to taxons
- large tandem repert to its annotation


## Project folder

/mnt/data/satelome 

Project unix group: satelome

```
    ### PART 3. Annotation and naming

    ### PART 4. Visualization

    # draw_chromosomes(settings, project)
    # draw_spheres(settings, project)
```

