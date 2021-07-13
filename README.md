# AlphaSeq Antibody Dataset

To support protein representation learning, we are publishing a publicly-available dataset containing antibody sequences and quantitative binding measurements to a known antigen.  Additional information describing how this data was generated can be found [link to paper].

## Overview

The dataset presented here contains quantitative binding scores of scFv-format antibodies against a SARS-CoV-2 target peptide collected via an AlphaSeq assay and can be used in support of the development and benchmarking of machine learning models.  Starting from three seed sequences identified from a phage display campaign using a human naïve library, sets of 29,900 antibodies were designed in silico by creating all k=1 mutations and random k=2 and k=3 mutations throughout the complementary-determining regions (CDRs).  Diversity was introduced in the heavy chain CDRs for seed sequence 1, in the light chain CDRs for seed sequence 2, and independently in the heavy and light chain CDRs of seed sequence 3, for a total of 4 sets.  Of the 119,600 designs, 104,972 were successfully built in to the AlphaSeq library and were subsequently measured with 71,384 designs resulting in a predicted affinity value for at least one of the triplicate measurements.  Data include antibodies with predicted affinity measurements ranging from (-1.43 to 7.35).  To our knowledge, this dataset is the largest, publicly-available dataset that contains antibody sequences, antigen sequence and quantitative measurements and provides an opportunity to serve as a benchmark to evaluate antibody-specific representation models for machine learning.

The dataset is a csv file with the following entries:

| **Variable Name**        | **Description**           |
| ------------------------ | ------------- | 
| POI     | Alphanumeric label corresponding to amino acid sequence. | 
| Sequence      | Single letter amino acid representation of scFv measured.      |  
| Target| Protein target represented by a text label for which the measured antibody interacted with.  Options are defined target or negative controls 1-3.   | 
| Assay     | Unique assay identifier, either 1 or 2. | 
| Replicate     | Unique replicate identifier, either 1, 2 or 3 | 
| Pred_affinity     | Value representing the score from the AlphaSeq assay, as described in the methods section. Values estimate the protein-protein dissociation constant in nanomolar, on a log scale. Lower values indicate stronger binding. | 
| HC, LC     | Single letter amino acid sequence of the heavy chain (HC) or light chain (LC) | 
| CDR[H/L][1/2/3]     | Single letter amino acid sequence of a CDR region where H indicates heavy chain, L indicates light chain and the numerical value represents either CDR 1, CDR 2 or CDR 3.| 




## Citation

TODO: zenodo DOI




## License


Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg



## Disclaimer

DISTRIBUTION STATEMENT A. Approved for public release. Distribution is unlimited.

This material is based upon work supported by the United States Air Force and Under Secretary of Defense for Research and Engineering under Air Force Contract No. FA8702-15-D-0001. Any opinions, findings, conclusions or recommendations expressed in this material are those of the author(s) and do not necessarily reflect the views of the United States Air Force and Under Secretary of Defense for Research and Engineering.

© 2021 Massachusetts Institute of Technology.

SPDX-License-Identifier: CC-BY-4.0

Delivered to the U.S. Government with Unlimited Rights, as defined in DFARS Part 252.227-7013 or 7014 (Feb 2014). Notwithstanding any copyright notice, U.S. Government rights in this work are defined by DFARS 252.227-7013 or DFARS 252.227-7014 as detailed above. Use of this work other than as specifically authorized by the U.S. Government may violate any copyrights that exist in this work.

