# Bayesian-Optimization
Use BO framework to optimize Peak CV,Intensity CV and Intensity ave independently

Input parameter: Tip Height 0.5-50(mm),Dispense Speed 20-500(ul/s),AS Spin Speed 500-7000(rpm),AS Volume 50-300(ul),Timing AS 2-18(s)

It contains four parts:
* define parameter space
* build ML model
* build BO framework
* output next candidate

In building ML model section,we use RandomForest and GaussianProcess to build BO loop respectively.The parameters of two models are empirically tuned.

In building BO framework,we use NegativeLowerConfidenceBound as acquisition function and choose different beta to acquire multiple recommend candidates.
