# Simple variant annotation program

This is a prototype of variant annotation tool, written in Python.

## Input format
VCF

## Output format
VCF, with “ANN” annotation to the “INFO” field, if more than one alternate alleles, each alternate allele is separated by a comma."ANN" field is according to Variant annotations in VCF format.``http://snpeff.sourceforge.net/VCFannotationformat_v1.0.pdf``

## Prerequisite
  1. SnpEff (version >= 4.3t), download and unzip SnpEff into a folder and provide the path of snpEff.jar to the program, if SnpEff is already downloaded, provide the path of snpEff.jar to the program. SnpEff can be downloaded here.``http://sourceforge.net/projects/snpeff/files/snpEff_latest_core.zip``
  2. If first time running SnpEff, certain genome file will be downloaded automatically, which will take some time, after first time running, no more need of downloading genome file. 
  3. Python 3.6 or newer.
  4. Python packages: 
      1. pandas 0.22.0 or newer.
      2. numpy 1.13.1 or newer. 
      3. allel 1.1.10 or newer, install scikit-allel ``$ conda install -c conda-forge scikit-allel`` 
    
## Annotations this tool will do
This simple variant annotation tool is able to annotate variant with following information:
  1.	Type of variation (such as missense variant, synonymous variant, stop gained, stop loss, etc), complete list of type of variation can be seen in the file: ``ann_deleterious_order.txt``, these variation types are according to Sequence Ontology.``http://www.sequenceontology.org/``
  2.	Depth of sequence coverage at the site of variation.
  3.	Number of reads supporting the variant.
  4.	Percentage of reads supporting the variant versus those supporting reference reads.
  5.	Allele frequency of variant from Broad Institute ExAC.
  6.	Most deleterious variant consequence from ExAC.

## Download
``$ git clone https://github.com/hliu47/Simple_variant_annotation_program.git``

## Sample usage
``$ python3 SimpleAnnotation.py -input ./Challenge_data.vcf -snpeff ./snpEff/snpEff.jar -genome GRCh37.75``

## Output file
``simple_annotation.vcf``

## For help
``$ python3 SimpleAnnotation.py -h``

## Bug report
Please reach out to me ``hliu47@uic.edu`` for bug report.

## License
The MIT License.
