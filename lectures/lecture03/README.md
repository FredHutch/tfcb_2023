---
controls: false
progress: false
enableMenu: false
enableChalkboard: false
enableTitleFooter: false
enableSearch: false
transition: slide
theme: night
customTheme: custom
---


# Lecture 3: Data and Project Management

## [Rasi Subramaniam](http://rasilab.fredhutch.org)

[Link to slides](https://fredhutch.github.io/tfcb_2023/lectures/lecture03/revealjs_slides/index.html)

---

## Reminders

The homework assignment is available today (October 5) and is due October 12 at 3:30pm.

---

## Learning objectives

- Learn basics of VScode, GitHub, and Markdown
- Identify minimum requirements for a reproducible computational project
- Apply good practices for file organization 
- Use `tidy` principles for tabular (`spreadsheet`-style) data

---

## Outline

1. Hands on demo of VSCode, GitHub, Markdown
2. Elements of reproducibility
3. File organization
4. Tidy data

<div style="font-size:18pt;margin-top:20px;">
This class requires Microsoft Excel or LibreOffice Calc (for opening `.xlsx` or `.csv` files).
</div>

## Helpful resources

- [VSCode Intro Video Series](https://code.visualstudio.com/docs/getstarted/introvideos)
- [Crash Course on Git and GitHub Video](https://www.youtube.com/watch?v=RGOj5yH7evk)
- [Markdown Syntax Guide](https://guides.github.com/features/mastering-markdown/)

---

## Minimum elements for computational reproducibility

- *Annotated* data from experiments or simulations
- *Documented* code for data analyses
- *Defined* software environments
- *Standardized* organization of above 3 elements

<div style="font-size: 60%; text-align: left; margin-top: 50px;">

</div>

---

## 1 project = 1 GitHub repository

- Code
- Data*
- Lab notebook
- Presentations
- Manuscripts
- Grants & fellowships
- Discussion

---

## Different locations for data at different analysis stages

- **Raw data**: can be very large, store in cloud eg. [AWS S3](https://aws.amazon.com/s3/) or public repositories eg. [Zenodo](https://zenodo.org/), [SRA](https://www.ncbi.nlm.nih.gov/sra)
- **Intermediate data**: can be large or small, store in temporary scratch space
- **Tables underlying figures or samples**: small, store in GitHub

---

## Store sample annotations with data

Raw data without annotations cannot be analyzed

```
data/sample1.fastq
data/sample2.fastq
data/sample3.fastq
data/sample_annotations.tsv
```

`sample1.fastq`

```
@SRR21277963.1
GGAGTAACAGAAGTGAGAACCAGCTTATCAGAAAAAAAGTTTGAATTATG
+SRR21277963.1
AAGAGGGGAGGGAGGGGIAGGGGGGA.GGGGAGGGGIGIGGII<A<GGAA
```

`sample_annotations.tsv`

```
sample  srr_id       sample_id  sample_name
sample1 SRR21277963  104p8      dicodon_facs_off_low_2
sample2 SRR21277964  104p7      dicodon_facs_off_high_2
sample3 SRR21277965  104p6      dicodon_facs_on_low_2
```

---

## Benefits of GitHub

- Version control (file history, track changes)
- Collaboration (branches, merging, issue comments, discussion)
- Project management tools (project board, issues, milestones, labels)
- Link to Slack channel for notifications

<div style="font-size: 60%; text-align: left; margin-top: 50px;">

Example GitHub repositories: <br>
https://github.com/rasilab/ribosome_collisions_yeast (public) <br>
https://github.com/rasilab/bottorff_2022 (public) <br>
https://github.com/rasilab/micropeptide_immunity (private)

</div>

---

## Organization of GitHub repository

```
project_name
  |-- analysis/
  |-- experiments/
  |-- grants/
  |-- presentations/
  |-- manuscripts/
  |-- install/
  |-- .gitignore
  |-- README.md
```

- Use `README.md` to give an overview of the project and file organization
- Use `.gitignore` to ignore files that should not be tracked by git
- Use `install/` to define the software environment for analysis (can also use [GitHub Packages](https://docs.github.com/en/packages/learn-github-packages/introduction-to-github-packages) eg. see https://github.com/orgs/rasilab/packages)

---

## Organization of `analysis` folder

```
analysis
    |--USER
        |--ANALYSIS_TYPE (eg. riboseq)
            |--YYYY-MM-DD_short_desc
                |--README.md
                |--data 
                    |--gencode
                        |--gencode.v26.gtf.gz
                    |--fastq
                        |--SRRnnnnnn.fastq
                |--scripts
                    |--analyze_riboseq.ipynb
                    |--download_from_sra.ipynb
                    |--run_analysis_pipeline.smk
                |--annotations 
                    |--sample_annotations.csv
                |--tables
                    |--summary_table_1.csv
                    |--summary_table_2.csv
                |--figures
                    |--summary_figure_1.pdf
                    |--summary_figure_2.pdf
```                

- `.gz` and `.fastq` files are usually in `.gitignore`
- `README.md` should give an overview of the analysis, data source etc. and how to reproduce it
- Ideally, every data file should be downloaded programmatically from permalinks

---

## Naming conventions

- **Project repo**: Short, descriptive, understandable
- **File names**
  - No caps, no spaces, no special characters other than `_` and `-`
  - Date format: `YYYY-MM-DD`
  - No version numbers or names such as `rasi_v20` (GitHub does this automatically)
- **Experiment labels**
  - `exp001`, `exp002` etc.
  - Use in filenames, sample annotations, issues
- **Sample labels** 
  - `16p1`, `16p2` ... `20t1`, `20t2` etc... 
  - Include experiment number (16, 20), type of sample (p, t), and sample number (1, 2)
  - Use on Eppendorf tubes, lab notebook etc.
  - Create a table of sample annotations in your lab notebook record

<aside class="notes">
Documenting data can be a time-consuming process, but is often required to submit data to repositories. Since data publishing is a requirement for most academic research as a part of publication, keeping track of this information early on can save you time later, and increase the chances of other researchers using your data later (which means more citations for you).
</aside>

---

## Tidy data

<div style="font-size: 80%; text-align: left; margin-top: 50px;">

>A standard method of displaying a multivariate set of data is in the form of a data matrix in which rows correspond to sample individuals and columns to variables, so that the entry in the ith row and jth column gives the value of the jth variate as measured or observed on the ith individual.

<div style="text-align: right;font-size:80%"> 

[Hadley Wickham](https://twitter.com/hadleywickham) 

</div>
</div>

1. Each variable forms a column
2. Each observation forms a row
3. Each type of observational unit forms a table


<aside class="notes">
Data in this form is much easier to deal with programmatically. This is also
known as a _data frame_. See [this](https://r4ds.had.co.nz/tidy-data.html)
tutorial for an `R`-centric overview of tidy data.
</aside>

---

## Tidy data examples


<div style="text-align: left; margin-top: 50px;">

* Examples from [Park & Subramaniam 2019](https://github.com/rasilab/ribosome_collisions_yeast): [data](https://github.com/rasilab/ribosome_collisions_yeast/blob/master/data/western/quantification.tsv), [annotations](https://github.com/rasilab/ribosome_collisions_yeast/blob/master/data/flow/10xaag_wt/annotations.tsv)

* Example from [Table 2 in Bedford et al. 2014](https://bedford.io/papers/bedford-flux/), available as an [Excel table in the course repo](tables/influenza-evolutionary-parameters.xlsx)

* Follow same naming principles for columns as for files: No caps, no spaces, no special characters, use only `_` and `-` if necessary.

</div>

<aside class="notes">

Saving data as plain text files is necessarily to process this data with either R or Python. You can export from Excel to `.csv` (comma-delimited) or `.tsv` (tab-delimited). A few things to note when exporting data files in these formats:

- Beware that [line endings](https://support.nesi.org.nz/hc/en-gb/articles/218032857-Converting-from-Windows-style-to-UNIX-style-line-endings) differ between Windows and Unix (including Mac), though the text editors we recommend for this class can deal with this
- Exporting from Excel only works for the currently displayed spreadsheet. If you have multiple sheets, you'll need to export multiple times.

</aside>

---

## Exercise on tidy data

Split into small groups of 3-4 people to work from an HI (haemagglutination-inhibition) table and convert to tidy data. Data available as an [Excel table in the course repo](tables/influenza-titer-data.xlsx).

---

## Further reading


* [Good enough practices for scientific computing](https://swcarpentry.github.io/good-enough-practices-in-scientific-computing/)

* [Practical computational reproducibility in the life sciences](https://pubmed.ncbi.nlm.nih.gov/29953862/)

* [Reproducibility standards for machine learning in the life sciences](https://pubmed.ncbi.nlm.nih.gov/34462593/)

* [`R`-centric overview of tidy data](https://r4ds.had.co.nz/tidy-data.html)
