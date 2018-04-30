# Simple variant annotation program

This is a prototype of variant annotation tool, written in Python.

Input: VCF

Output: VCF, with “ANN” annotation to the “INFO” field, if more than one alternate alleles, each alternate allele is separated by a comma.

Prerequisite: SnpEff (version >= 4.3t), please download and unzip SnpEff into a folder and provide the path of snpEff.jar to the program, if SnpEff is already downloaded, please provide the path of snpEff.jar to the program. SnpEff can be downloaded here:
http://sourceforge.net/projects/snpeff/files/snpEff_latest_core.zip

If first time running SnpEff, certain genome file will be downloaded automatically, which will take some time, after first time running, no more need of downloading genome file. 

This simple variant annotation tool is able to annotate variant with following information:
  1.	Type of variation (such as missense variant, synonymous variant, stop gained, stop loss, etc), complete list of type of variation can be seen in the file: ``ann_deleterious_order.txt``.
  2.	Depth of sequence coverage at the site of variation.
  3.	Number of reads supporting the variant.
  4.	Percentage of reads supporting the variant versus those supporting reference reads.
  5.	Allele frequency of variant from Broad Institute ExAC.
  6.	Most deleterious variant consequence from ExAC.

## Download
``git clone https://github.com/hliu47/Simple_variant_annotation_program.git``

## Sample usage
``python3 SimpleAnnotation.py -input ./Challenge_data.vcf -snpeff ./snpEff/snpEff.jar``

## Output file
``simple_annotation.vcf``

## Help
`` python3 SimpleAnnotation.py -h``
