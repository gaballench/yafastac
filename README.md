# yafastac
YAFASTAC: Yet Another FASTA Concatenator

This program in pure bash takes as input a path with the results from capturing UCES by `phyluce` and then concatenates with respect to locus. Then it writes to an output directory which is created as part of the code.                                                                               

# Installation

simply clone the github directory:                                                                                                

```
git clone https://github.com/gaballench/yafastac                                                                                              
```

then add it to the path (e.g., modify your `PATH` variable in `.bashrc` or elsewhere, google it or ask when in doubt), and make it executable if it is not yet:                                                                               
```
cd yafastac; chmod +x yafasta                                                                                                                  
```

# Usage

Arguments are `input_path`, `output_path`, `threshold`, `remove_files`, and `verbose`

```
yafastac input_path output_path threshold remove_files verbose
```


Arguments `input_path` and `output_path` are paths where the exploded uce FASTA files from phyluce are located, often in multiple directories, and where we want to store the concatenated UCE fasta files.

Argument `threshold` sets the minimum number of taxa that a given UCE should have with respect to the whole taxon sampling to be incuded in the final dataset. It is a float number e.g. 0.7 for generating a dataset where UCEs are included only if they have 70% or more of the complete taxon sampling.

Argument `remove_files` removes those UCE fasta files that do not meet the threshold above, which are renamed as `.REMOVE`. Possible values are 0 (don't remove) or 1 (remove).

Argument `verbose` prints several useful strings which are meant for debugging. It is useful however to turn it on and then redirect the output to a text file for examining later. Possible values are 0 (do not print information to screen) or 1 (print it).

An example using a threshold of 75%, _removing_ the UCEs that don't meet the threshold, and being verbose while redirecting the text output to a log file would be:

```bash
yafastac multiple_runs final_uces 0.75 1 1 > logfile.txt
```

An example using a threshold of 50%, _preserving_ the UCEs that don't meet the threshold, and being verbose while redirecting the text output to a log file would be:

```bash
yafastac multiple_runs final_uces 0.75 0 1 > logfile.txt
```

An example using a threshold of 80%, _preserving_ the UCEs that don't meet the threshold, and _not being_ verbose thus not generating any text and no need for a log file:

```bash
yafastac multiple_runs final_uces 0.75 0 0
```

# Citation

If this is useful please cite it as resource online:

```
Ballen, G.A. 2025. YAFASTAC: Yet Another FASTA Concatenator. Version 0.2.1. Url: https://github.com/gaballench/yafastac. DOI https://doi.org/10.5281/zenodo.15083923.
```
