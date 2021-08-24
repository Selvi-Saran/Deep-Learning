# Deep-Learning
   
   This is a predictive maintenance project whether the engine will fail in a certain time period or not .
   
The dataset consists of the following three files: 

Training data	: It contains the aircraft engine run to failure data.

Testing data: 	It contains the aircraft engine operating data without failure events recorded

Ground truth data:	Here, the information about the true remaining cycles for each engine in testing data is available

Training data:

•	According to the data description provided at the data source, the training data consists of multiple multivariate time series with cycle as the time unit, together with 21 sensor readings for each cycle.

•	 Each time series can be assumed as being generated from a different engine of the same type. Each engine is assumed to start with different degrees of initial wear and manufacturing variation, and this information is unknown to the user.

•	In this simulated data, the engine is assumed to be operating normally at the start of each time series. It starts to degrade at some point during the series of the operating cycles. This degrades the progresses and grows in magnitude. When a predefined threshold is reached, then the engine is considered unsafe for further operation.

•	 In other words, the last cycle in each time series can be considered as the failure point of the corresponding engine. Taking the sample training data as an example, the engine with id=1 fails at cycle 192, and engine with id=2 fails at cycle 287.

 Testing data:

•	It has the same data schema as the training data.

•	The only difference is that the data does not indicate when the failure occurs (in other words, the last time period does NOT represent the failure point).
•	Taking the sample testing data, the engine with id=1 runs from cycle 1through cycle 31. It is not shown how many more cycles this engine can last before it fails.

Ground truth data:

•	It provides the number of remaining working cycles for the engines in the testing data.

•	Taking the sample ground truth data shown as an example, the engine with id=1 in the testing data can run another 112 cycles before it fails


Since this is a time series data, use Long Short-Term Memory (LSTM) to classify weather the engine will fail in a certain time period or not.

