# Customer Segmentation on Auto Insurance Clients

## Overview

Not often do insurance companies get many new client very frequently and so the way these companies earn revenue is through monthly premiums for the protection policies that they provide. Having said this, insurance companies can expect to lose out some earnings through claims. So the challenge here for insurance companies is to keep Claims-to-Premium ratio low. One way to do this is by making recommendations to clients that is appropriate for their needs. The focus for this analysis is auto insurance.

**Goal**: Perform a segmentation analysis on current clients based on their car properties and insurance plan(s).

Some research questions and possible deliverables:
* What is the current state of the insurance business? 
* What does the customer lifetime value look like for this business?
* How does the distribution of insurance coverage plan enrolment look like?
* Does the type of coverage that clients enrol in depend on the type of vehicle they own?

## Prerequisite

The notebook, `bank_loan.ipynb`, is written in Python 3. The libraries that are used in this notebook are listed under the `requirements.txt` file. One can simply issue to following command to insure the proper libraries are installed:

```bash
pip3 install -r requirements.txt
```

## Description of Analysis

Generally, k-means is typically used for clustering analysis. However, k-means is appropriate for numerical features. For this analysis, we have both numerical and categorical features that describe clients (which in my opinion makes this analysis a bit more interesting!). From a bit of research on clustering approaches, I stumbled upon the k-prototypes approach which is designed to handle this type of problem. The library for k-prototypes can be found [here](https://github.com/nicodv/kmodes). It works very similar (if not, the same) type of problem. 

From the analysis, the "elbow" method showed that we can separate the clients into 4 distinct groups. Results showed that these 4 groups have very different average customer lifetime value and their most preferred coverage plan. This exercise is a great way to identify different groups of clients based on their CLV that can help insurance companies to determine which clients to renew their plan or make appropriate recommendation based on their needs that can increase their CLV. 
