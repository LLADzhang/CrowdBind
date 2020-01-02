# Description
This repo hosts the one-month mobility trace of 62 users at Purdue University. This mobility trace was collected by installing our Android application on users' smartphones and the app periodically sampled users' location. 

## Cite the paper
The mobility trace was used to evaluate our EWSN 2020 paper "CrowdBind: Fairness Enhanced Late Binding Task Scheduling in Mobile Crowdsensing". If you find our mobility trace useful in your scientific publication, please consider citing 
```
@inproceedings{Zhang2019CrowdBindFE,
  title={CrowdBind: Fairness Enhanced Late Binding Task Scheduling in Mobile Crowdsensing},
  author={Heng Zhang and Michael A Roth and Rajesh K. Panta and He Wang and Saurabh Bagchi},
  year={2019}
}
```
## Command to use
* "gunzip trace.npy.gz" to get a file called "trace.npy"
* In python3, use "numpy.load('trace.npy')" to load the mobility trace. 

## How the data looks like
This mobility trace is stored as numpy 2-d array. 
* The elements of each row: [('id', 'int'), ('latitude', 'float'), ('longitude', 'float'), ('timestamp', 'int')])
* The first element of each row is the id of a user. For user privacy concern, we use 0 to 61 to denote those 62 users. Note that some users may have some missing datapoints. This may due to different factors such as user turned off phone at night, user has limited network access, or user quitted the data collection campaign for personal reasons. We did not restrict user's normal activities during the data collection.
