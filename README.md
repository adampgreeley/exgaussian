# exgaussian
# Exponentially-modified Gaussian distribution error analysis


This repository contains code for analyzing Monte Carlo generated errors for Expontnially-Modified Gaussian (EMG) function parameters. It also contains the script used to generate the errors.

Mat-files (EMG_parameter_error_M##S##T##.mat) contain the results from Monte Carlo generated EMG parameter fits. The two-digit numbers following M, S, and T, correspond to the following EMG parameter values for mu, sigma, and tau respectively:

EMG Parameter     01      02      03      04      05      06      07      08      09      10      11      12      13 
-----------------------------------------------------------------------------------------------------------------------
    MU              0       1       2       4       8      16      32      64     128     256     512    1024    2048
    SIGMA        0.02    0.05    0.08    0.11    0.14    0.17    0.20    0.23    0.26    0.29    0.32    0.35    0.38
    TAU          0.02    0.05    0.08    0.11    0.14    0.17    0.20    0.23    0.26    0.29    0.32    0.35    0.38


The EMG parameter values above can also be found in each Mat-file in the variables: MU0, SIGMA0, and TAU0. These values define the parent EMG distribution from which Monte Carlo samples are drawn from. The number of samples (N) drawn from the parent EMG distribution is found in each Mat-file in the variable, SAMPLE. Samples of size N, were selected from the parent EMG distribution 10,000 times. The resulting EMG parameter fits are stored in their respective arrays (i.e, MU, SIGMA, and TAU). The rows of each array correspond to the number of samples the parameter was fitted to (i.e., the value in the corresponding rows of the vector "SAMPLE"), and the columns correspond to each of the 10,000 samplings of the parent EMG distribution.


