# distMAVE
The distMAVE method is designed for the massive datasets with hundreds of thousands of observations stored on one machine. The classical MAVE (minimum average variance 
estimation) method can be very time consuming when we generalize its application to nowadays large data acquired on one machine, because its minimization problem can be 
decomposed into two quadratic programming problems and the computational complexity is about O(N^2), where N is the whole sample size. To address this issue, we partition 
the N data observations into m machines with equal sample size n=N/m. The core idea is that we randomly selected n samples from the whole dataset, and assign them to each 
machine, instead of using the samples stored across different local machines. Our proposed distMAVE algorithm performs the classical MAVE method on each subset and then 
combines all the m estimators suitably into an aggregated estimator. Theoretical results show that the final CMS estimator is root-N consistent, which means that the 
divide-and-conquer approach for the CMS directions has the same statistical efficiency as using all the data observations. In addition, simulation studies and a real data 
analysis demonstrate that our proposed distMAVE method can reduce calculation time by a large margin while retaining high estimation accuarcy.
