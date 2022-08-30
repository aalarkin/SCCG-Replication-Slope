# SCCG-Replication-Slope
Analysis of single copy core gene coverage to calculate strain-specific microbial replication

Author: <br />
Alyse Larkin (larkinsa@uci.edu) <br />
Assistant Project Scientist <br />
Department of Earth System Science <br />
University of California, Irvine 

## Summary
Here we provide the R code necessary to reproduce the analysis described in Larkin *et al.* 2022, *ISME J*, "Basin-scale biogeography of *Prochlorococcus* and SAR11 ecotype replication." Specifically, in we provide: 
- A function to calculate the terminus of replication using the median circular minimum as first described by Korem *et al.* 2015 
- A function to simultaneously fit forward and reverse linear functions to gene coverage patterns such that the slopes of the forward and reverse (i.e., "right hand" and "left hand") functions are equal 
- An example application of these functions to a marine dataset using the *Prochlorococcus* ecotype HLI 

If users wish to apply this code to their own datasets, users should first obtain: 
- A Sample x Gene matrix containing the coverage values of single cope core genes. We **strongly** recommend that coverage values be based on rarefied reads, such that the same number of reads are used for every sample in the dataset. 
- A single column matrix containing the start locations for every gene based on a reference genome 


## Requirements
For this example code we use a Jupyter notebook, which provides a convenient way to share scripts and run them right in the notebook. Jupyter notebooks comes automatically with the Anaconda python platform. 

** Steps for setting up: **
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

5. To run the example code, just click on the cell and press `Cntr + Enter` to run it, or just use the *run* button from the menu on top.
