# Structural variant PacBio vcf

 - A multi-sample structural variant callset was produced by merging single-sample pbsv callsets with JASMINE v1.1.4 (https://doi.org/10.1101/2021.05.27.445886) using jasmine --output-genotypes.
 - This file is then filtered to 2+ unrelated individuals according to these rules: (1) match one other unrelated CMH SV (merged by Jasmine) or (2) match one Decode or HPRC SV using svpack match with default setting.


