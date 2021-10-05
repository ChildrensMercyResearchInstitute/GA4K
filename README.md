# Genomic answers for kids - filtered PacBio vcf files

Small Variants: 
 - A multi-sample small variant callset was produced by running GLnexus v1.2.7 (https://doi.org/10.1093/bioinformatics/btaa1081) on all single-sample DeepVariant gVCF files using glnexus_cli --config DeepVariant_unfiltered and converting the resulting BCF to VCF with bcftools viewv1.10.
 - This file is then filtered to 2+ unrelated individuals according to these rules: (a) match one other unrelated CMH variant or (2) match a variant in a HPRC sample.

Structural Variants: 
 - A multi-sample structural variant callset was produced by merging single-sample pbsv callsets with JASMINE v1.1.4 (https://doi.org/10.1101/2021.05.27.445886) using jasmine --output-genotypes.
 - This file is then filtered to 2+ unrelated individuals according to these rules: (1) match one other unrelated CMH SV (merged by Jasmine) or (2) match one Decode or HPRC SV using svpack match with default setting.
