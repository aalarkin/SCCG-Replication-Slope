# SCCG-Replication-Slope
Analysis of single copy core gene coverage to calculate strain-specific microbial replication

Author: <br />
Alyse Larkin (larkinsa@uci.edu) <br />
Assistant Project Scientist <br />
Department of Earth System Science <br />
University of California, Irvine 

## Summary
Here we provide the R code necessary to reproduce the analysis described in Larkin *et al.* 2022, *ISME J*, "Basin-scale biogeography of *Prochlorococcus* and SAR11 ecotype replication." Specifically, we provide: 
- A function to calculate the terminus of replication using the median circular minimum as first described by Korem *et al.* 2015 
- A function to simultaneously fit forward and reverse linear functions to gene coverage patterns such that the slopes of the forward and reverse (i.e., "right hand" and "left hand") functions are equal 
- An example application of these functions to a marine dataset using the *Prochlorococcus* ecotype HLI 

If users wish to apply this code to their own datasets, users should first obtain: 
- A Sample x Gene matrix containing the coverage values of single cope core genes. We **strongly** recommend that coverage values be based on rarefied reads, such that the same number of reads are used for every sample in the dataset. 
- A single column matrix containing the start locations for every gene based on a reference genome 


## Requirements
For this example code we use a Jupyter notebook, which provides a convenient way to share and run scripts. Jupyter notebooks comes automatically with the Anaconda python platform. 

### Setup
1. Go to the main page of this Github respository (<https://github.com/aalarkin/SCCG-Replication-Slope/>), click on "*clone or download*" in the top-right corner, and select "*Download ZIP*" to download the whole repository on your computer. Keep track of where you are downloading the file. Unzip the respository if your browser has not done it automatically.

2. Download the latest version of Anaconda for your operating system: <https://www.continuum.io/downloads> and follow the instructions to install.

3. This code uses R, therefore you will need to install the R kernel. For this, go to command line and type
```
conda install -c r r-essentials
```

4. Open Jupyter notebook: In command prompt or the Anaconda prompt in Windows, navigate to where you downloaded this repository and type in
```
jupyter notebook
```
This should open up Jupyter on your browser from the directory that you navigated to above. On the main page of the respository on Jupyter, click on this notebook. 

NOTE: Depending on your operating system and the current version of Anaconda, you may run into some R kernal dependency issues. If this is the case, you can you use either Anaconda or Miniconda to create a conda environment using the environment dependencies provided in this GitHub repository. To create a conda environment, navigate to the directory containing this repository and type
```
conda env create --name mypython3r4 -f environment.yml
```
After you have created your conda environment you may need to close your command prompt before continuing with the following
``` 
conda activate mypython3r4

jupyter notebook
```

5. To run the example code, just click on the cell and press `Cntr + Enter` to run it, or just use the *run* button from the menu on top.

## License
Shield: [![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
