# Novel GAA - like protein: Find-a-Gene analysis in Homo sapiens

] **Template:** replace every item in angle brackets `[ ]`, then delete this line. See [GETTING_STARTED.md](GETTING_STARTED.md) for how to add files.

BIFX-550 Computational Functional Genomics, Hood College, Fall 2026
Author: Kate Kruczynski (Katopotat0)

## Summary

This repository contains the needed files, methods, and final results for a project to find a novel gene from a starting protein of interest. The starting protein for this analysis is human GAA - alpha glucosidase, an important enzyme for the breakdown of glycogen into glucose. The basic structure of this protein is very conserved within most lifeforms as processing glycogen is an essential function of metabolism. The novel protein which I located was an "unnamed protein product" from a very newly sequence insect species, Pseudaplemonus limonii. This insect does not have an established common name in English, although there are common German and Dutch names for it. The Dutch name is Lamsoorspitsmuisje "Sea Lavender Shrew" referring to its habitat and likely its resemblance to the rodent known as a shrew. I refer to it as the Lavender Weevil within this analysis for clarity and brevity. 

| Item | Value |
|---|---|
| Starting protein | GAA-alpha glucosidase|
| Starting species | Homo sapiens |
| Starting accession |UniProt: P10253 |
 |
| Novel candidate |  unnamed protein product; chromosome 10; locus_tag="PSELIMO101_LOCUS3883"; 1040 aa |
| Source organism | Pseudaplemonus limonii |
| Source nucleotide record | CAR8053950.1  |
| Novelty evidence | [BLASTp top hit in nr: Predicted annotation, 407/853(48%)% identity, 0.0 E-value] |
| Structure prediction | [Tool; mean pLDDT or QMEAN] |
| Closest PDB entry | [PDB ID] |

## Repository structure

```
.
├── README.md           project summary (this file)
├── data/               sequences in FASTA format
├── scripts/            commands, notebooks, and the analysis log
├── results/
│   ├── blast/          tBLASTn and BLASTp output
│   ├── msa/            multiple sequence alignment
│   ├── tree/           phylogenetic tree files and images
│   └── structure/      predicted models, images, PDB comparison
└── report/             bifx550c written report (Word)
```

## Workflow

| Step | Task | Tool | Output |
|---|---|---|---|
| 1 | Choose a starting protein | UniProt or NCBI Protein | `data/` |
| 2 | Search for a candidate novel gene | tBLASTn against WGS or TSA | `results/blast/` |
| 3 | Retrieve and translate the ORF | GenBank record, ORF translation | `data/` |
| 4 | Confirm novelty | BLASTp against nr | `results/blast/` |
| 5 | Multiple sequence alignment | [Clustal Omega, MUSCLE, MAFFT, or T-Coffee] | `results/msa/` |
| 6 | Phylogenetic tree | [MEGA or IQ-TREE; method] | `results/tree/` |
| 7 | Structure prediction and comparison | [AlphaFold, ColabFold, or SWISS-MODEL; Mol* or ChimeraX] | `results/structure/` |
| 8 | Selection analysis (optional) | [HyPhy or PAML] | `results/selection/` |
| 9 | Discussion | | `report/` |

Tool versions, access dates, and parameters for every step are recorded in [scripts/README.md](scripts/README.md).

## Key results

### Novelty
[What the BLASTp search against nr returned and why the candidate counts as novel.]

### Alignment and phylogeny
The Lavender Weevil gene shares the highly conserved WIDMNE motif with human GAA. 

### Structure
Alphafold Model - pTM = 0.85, plDDT > 90 for majority of structure.

## Limitations and next steps

[What the evidence cannot show, and what you would test next.]

## Reproducing this analysis

Inputs are in `data/`. Every step, with its tool, version or access date, parameters, input, and output, is listed in the analysis log in [scripts/README.md](scripts/README.md). Following that log in order reproduces the results in `results/`.

## Use of AI tools

[Name any AI tool that contributed materially and describe how, or write "None."]

## References

BIFX-550 Find-a-Gene template, github.com/ravichas/bifx550-find-a-gene-template.



Dohmen, E., Klasberg, S., Bornberg‐Bauer, E., Perrey, S. W., & Kemena, C. (2020). The modular nature of protein evolution: domain rearrangement rates across eukaryotic life. BMC Evolutionary Biology, 20(1), 30. https://doi.org/10.1186/s12862-020-1591-0

Kaur, J., Sharma, A., Sharma, M., Manhas, R. K., Kaur, S., & Kaur, A. (2019). Effect of α-glycosidase inhibitors from endophytic fungus Alternaria destruens on survival and development of insect pest Spodoptera litura Fab. and fungal phytopathogens. Scientific Reports, 9(1), 11400. https://doi.org/10.1038/s41598-019-47838-6
