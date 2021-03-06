# BayesNet-and-Inference-Algorithm


ASSIGNMENT Task.

The goal of this programming assignment is to understand the relative properties of the inference
algorithm. In order to do so, you are required to design the alarm Bayes net presented in the class and
shown in Figure 14.
2 from the Russell and Norvig book. Use the parameters of the CPTs from the
Figure. Implement exact inference by enumeration, prior sampling, rejection sampling and likelihood
weighting.
Your program should take a set of strings as input. They will appear as the following: [< N1, V 1 >, ..., < NN, V N >] [NQ1, ..., NQM]. The ﬁrst set of strings is the evidence set and the next is the query. For simplicity use the node indexes as A, B, E, J, M corresponding to alarm, burglary,
earthquake, John and Mary calling. An example input would be:
[< A, t >< B, f >][J] which queries for John calling given that alarm is true and burglary is false.
Similarly [< E, t >< J, t >][M, A] which queries for Mary calling and Alarm given that earthquakeand John calling are true.
Correspondingly the output is now a set of strings [
< NQ1, P1 >< NQ2, P2 >]. So the outputcorresponding to the previous cases could be [< J, 0.9 >] and [< M, 0.08 >< A, 0.96 >]1.
In addition to turning in the code, I require a writeup which has tables of the form shown below.
As you can see, you vary the number of samples from 1 to 10000 and then run the diﬀerent algorithms.
This will explain how the probabilities vary with the number of samples. Note that the last row in
the table is the result of the enumeration algorithm. You should run each sampling algorithm 10
times for each number of samples. For example run prior sampling 10 times and average the inferred
probability over the test queries.
Show 3 speciﬁc cases:

1. Alarm is false, infer Burglary and JohnCalls being true.
2. JohnCalls is true, Earthquake is false, infer Burglary and MaryCalls being true.
3. MaryCalls is true and JohnCalls is false, infer Burglary and Earthquake being true.

So your report must have 6 tables (3 sets of 2 tables corresponding to the queries). 
