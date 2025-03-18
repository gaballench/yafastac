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
cd yafasta; chmod +x yafasta                                                                                                                  
```

# Usage

Arguments `input_path` and `output_path` are paths where the exploded uce FASTA files from phyluce are located, often in multiple directories, and where we want to store the concatenated UCE fasta files.

```
yafastac input_path output_path                                                                                                          
```                                                                                                                                             

# Citation

If this is useful please cite it as resource online:

```
Ballen, G.A. 2025. YAFASTAC: Yet Another FASTA Concatenator. Url: https://github.com/gaballench/yafastac
```
