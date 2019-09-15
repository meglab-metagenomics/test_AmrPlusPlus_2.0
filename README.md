# Testing AMR++ 2.0
Instructions for testing version 2 of MEGARes and AMR++ on Amazon Web Services

# Requirements:
    
    - Command-line tool with Secure Shell (ssh) capability. 
    - Internet access
    - PEM key file


# Step-by-step instructions:

```bash
# Start your command-line tool of choice (e.g. terminal, putty, mobaxterm, etc)

# Download MEG_AMR_AMI.pem file from this repository
$ git clone https://github.com/meglab-metagenomics/test_AmrPlusPlus_2.0.git

# Change permissions to the .pem file
$ chmod 400 MEG_AMR_AMI.pem

# Log into the amazon machine image using ssh and the .pem file:
$ ssh -i MEG_AMR_AMI.pem ec2-user@ec2-13-58-155-121.us-east-2.compute.amazonaws.com

# Navigate to directory with AMR++ pipeline code:
$ cd amrplusplus_v2/

# Run a test set of samples using the AMR++ pipeline
$ nextflow run main_AmrPlusPlus_v2.nf -profile MEG_AMI

# Explore results in the “test_results” directory:
$ cd test_results/

```
