# datasets

Public datasets for bioinformatics, machine learning, and computational biology
teaching and research.

Maintained by [Sarangan Ravichandran, PhD, PMP](https://github.com/ravichas) —
Computational Biologist, Data Scientist, and Adjunct Faculty.

---

## Repository Structure

```
datasets/
├── bifx/                  # Bioinformatics (BIFX-550, BIFX-553, ...) course data
│   ├── sequences/         # FASTA reference genomes and genes
│   └── reads/             # FASTQ sequencing read files
├── ml/                    # Machine learning datasets
├── clinical/              # Clinical and biomedical datasets
└── README.md
```

---

## Datasets

### Bioinformatics (`bifx/`)

| File | Description | Source | Accession |
|------|-------------|--------|-----------|
| `sequences/NG_049243.1.fa` | Human RefSeq gene | NCBI RefSeq | [NG_049243.1](https://www.ncbi.nlm.nih.gov/nuccore/NG_049243.1) |
| `sequences/phix.fa` | Coliphage phi-X174 complete genome | NCBI GenBank | [J02482.1](https://www.ncbi.nlm.nih.gov/nuccore/J02482.1) |
| `reads/sample_reads.fastq` | First 1000 reads, SRR835775 | NCBI SRA | [SRR835775](https://www.ncbi.nlm.nih.gov/sra/SRR835775) |
| `reads/phix_reads.fastq` | First 1000 PhiX reads, ERR266411 | NCBI SRA / ENA | [ERR266411](https://www.ebi.ac.uk/ena/browser/view/ERR266411) |

---

## Usage

All files are publicly accessible via raw GitHub URLs. Use directly in Google Colab
or any environment with `wget`:

```bash
# Example — fetch PhiX174 genome
wget -q -O phix.fa \
  https://raw.githubusercontent.com/ravichas/datasets/main/bifx/sequences/phix.fa

# Example — fetch human gene NG_049243.1
wget -q -O NG_049243.1.fa \
  https://raw.githubusercontent.com/ravichas/datasets/main/bifx/sequences/NG_049243.1.fa
```

Or with NCBI Entrez Direct (`efetch`):

```bash
efetch -db nuccore -id J02482.1  -format fasta > phix.fa
efetch -db nuccore -id NG_049243.1 -format fasta > NG_049243.1.fa
```

---

## Data Sources & Credits

All sequence data is sourced from public NCBI and EBI databases and redistributed
here solely for educational use. Original accession numbers and source links are
provided in the table above.

- [NCBI RefSeq](https://www.ncbi.nlm.nih.gov/refseq/)
- [NCBI GenBank](https://www.ncbi.nlm.nih.gov/genbank/)
- [NCBI SRA](https://www.ncbi.nlm.nih.gov/sra)
- [EBI ENA](https://www.ebi.ac.uk/ena)

---

## Contributing

To add a new dataset, open an issue or pull request with:
- File(s) to add
- Description and original source
- Accession number or DOI if applicable

---

## License

Data files retain the license of their original source databases.
All original content in this repository (README, scripts) is released under
[MIT License](LICENSE).
