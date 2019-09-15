# test_AmrPlusPlus_2.0
Instructions for testing version 2 of MEGARes and AMR++ on Amazon Web Services

# Requirements:
    
    - Command-line tool with Secure Shell (ssh) capability. 
    - Internet access
    - PEM key file


Step-by-step instructions:
    1. Start the command-line tool
    2. Log into the amazon machine image using ssh and the .pem file:
$ ssh -i MEG_AMR_AMI.pem ec2-user@ec2-13-58-155-121.us-east-2.compute.amazonaws.com
    3. Navigate to directory with AMR++ pipeline code:
$ cd amrplusplus_v2/
    4. Run a test set of samples using the AMR++ pipeline
$ nextflow run main_AmrPlusPlus_v2.nf -profile MEG_AMI
    5. Explore results in the “test_results” directory:
$ cd test_results/
