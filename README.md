# rnaseq-nf

# RNA-Seq analysis pipeline using Nextflow


This is a pipeline for processing RNA-Seq data using Nextflow, a popular workflow management system. The pipeline is designed to be run on a Linux-based operating system, such as Ubuntu, and has been tested on Windows using the Windows Subsystem for Linux (WSL).

## Installation

1. Install Nextflow by following the instructions [here](https://www.nextflow.io/docs/latest/getstarted.html#installation).

2. Install the required software dependencies:
   
   - FastQC
   - Cutadapt
   - STAR
   - RSEM
   - SAMtools
   - MultiQC

   These can be installed on Ubuntu using the `apt-get` package manager. For example, to install FastQC, you would run:


You can also install these dependencies using a package manager such as `conda` or `bioconda`.

3. Clone the repository:


## Usage

1. Edit the `nextflow.config` file to specify the input data and other parameters.

2. Run the pipeline:


This will launch the pipeline and start processing the input data.

3. To resume a previous run of the pipeline, add the `-resume` option:

4. After the pipeline finishes running, the results will be available in the `results` directory.

## Workflow

The pipeline consists of the following steps:

1. **Quality control:** Perform quality control on the raw RNA-Seq reads using FastQC.

2. **Preprocessing:** Remove adapter sequences and low-quality reads using Cutadapt.

3. **Alignment:** Align the preprocessed reads to the reference genome using STAR.

4. **Quantification:** Quantify gene expression using RSEM.

5. **Post-processing:** Merge the results from multiple samples and generate summary reports using MultiQC.

## Credits

This pipeline was created by [Sejyoti Chakraborty](https://github.com/sejyoti) and is based on the [RNA-Seq pipeline](https://github.com/nf-core/rnaseq) developed by the [nf-core](https://nf-co.re/) community.

## License

This pipeline is licensed under the [MIT License](https://github.com/sejyoti/rnaseq-nf/blob/main/LICENSE).
