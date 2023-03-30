# AlphaSeq Antibody Dataset 2

To support protein representation learning, we are publishing a second
dataset containing antibody sequences and quantitative
binding measurements to a known antigen.  Please refer to our paper [Machine Learning Optimization of Candidate Antibodies Yields Highly Diverse Sub-nanomolar Affinity Antibody Libraries](https://www.biorxiv.org/content/10.1101/2022.10.07.502662v1) for additional information on the method and design of these sequences.  

The initial AlphaSeq Antibody Dataset 1 can be found [here](https://github.com/mit-ll/AlphaSeq_Antibody_Dataset).
Additional information about the design of Dataset 1 and experimental set-up for quantitative binding
measurements can be found in our [Data Descriptor
Paper](https://www.nature.com/articles/s41597-022-01779-4). 

## Overview


The dataset presented here contains quantitative binding scores of scFv-format
antibodies against a SARS-CoV-2 target peptide collected via an AlphaSeq assay. We integrate target-specific binding affinities with
information from millions of natural protein sequences in a probabilistic machine learning framework to
design thousands of scFvs that are then empirically measured. This is the second dataset we're releasing that contains antibody sequences, antigen sequence and quantitative measurements and provides an opportunity to serve as a benchmark to evaluate antibody-specific representation models for machine learning.

The dataset is a csv file with the following entries:

| **Variable Name**        | **Description**           |
| ------------------------ | ------------- | 
| POI <sup>1</sup>    | Alphanumeric label corresponding to amino acid sequence. | 
| Sequence      | Single letter amino acid representation of scFv measured.      |  
| Target| Protein target represented by a text label for which the measured antibody interacted with.  Options are defined as target or non-target negative controls 1-3.   | 
| Assay     | Unique assay identifier. (All sequences here come from Assay B) | 
| Replicate     | Unique replicate identifier, ranging from 1 to 6 | 
| Pred_affinity     | Value representing the score from the AlphaSeq assay, as described in the methods section. Values estimate the protein-protein dissociation constant in nanomolar, on a log scale. Lower values indicate stronger binding. Blank values indicate poor binding.| 
| HC, LC     | Single letter amino acid sequence of the heavy chain (HC) or light chain (LC) | 
| CDR[H/L][1/2/3]     | Single letter amino acid sequence of a CDR region where H indicates heavy chain, L indicates light chain and the numerical value represents either CDR 1, CDR 2 or CDR 3.| 

<sup>1</sup> _Note:  The POI naming convention may only capture one of the methods used to generate the sequence. Multiple methods may have been used to generate the sequences that are not captured in the POI. Please see LINK for more information about the particular method used for a given sequence_






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

"This material is based upon work supported by the Under Secretary of Defense for Research and Engineering under Air Force Contract No. FA8702-15-D-0001. Any opinions, findings, conclusions or recommendations expressed in this material are those of the author(s) and do not necessarily reflect the views of the Under Secretary of Defense for Research and Engineering."

© 2023 Massachusetts Institute of Technology.

Subject to FAR52.227-11 Patent Rights - Ownership by the contractor (May 2014)
"Delivered to the U.S. Government with Unlimited Rights, as defined in DFARS Part 252.227-7013 or 7014 (Feb 2014). Notwithstanding any copyright notice, U.S. Government rights in this work are defined by DFARS 252.227-7013 or DFARS 252.227-7014 as detailed above. Use of this work other than as specifically authorized by the U.S. Government may violate any copyrights that exist in this work."

SPDX-License-Identifier: CC-BY-NC-SA-4.0


