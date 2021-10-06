# Replicated PacBio SNV vcf

 - A multi-sample small variant callset was produced by running GLnexus v1.2.7 (https://doi.org/10.1093/bioinformatics/btaa1081) on all single-sample DeepVariant gVCF files using glnexus_cli --config DeepVariant_unfiltered and converting the resulting BCF to VCF with bcftools viewv1.10.
 - This vcf is then filtered to 2+ unrelated individuals according to these rules: (a) match one other unrelated CMH variant or (2) match a variant in a HPRC sample.
 - The vcf is split by chromosome into 24 seperate files (chr 1-22, X, Y).
