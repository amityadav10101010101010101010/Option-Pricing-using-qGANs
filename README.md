# Option-Pricing-using-qGANs
A quantum Generative Adversarial Network (qGAN) can facilitate the pricing of a European call option. More specifically, a qGAN can be trained such that a quantum circuit models the spot price of an asset underlying a European call option. The resulting model can then be integrated into a Quantum Amplitude Estimation based algorithm to evaluate the expected payoff - see European Call Option Pricing. 
![image](https://user-images.githubusercontent.com/56102543/176602425-40c5602a-23ff-44d2-b35b-e8d48359fae3.png)
 Then the trained uncertainty model can be used to evaluate the expectation value of the option’s payoff function with Quantum Amplitude Estimation.
 Next, we plot the trained probability distribution and, for reasons of comparison, also the target probability distribution.
 ![image](https://user-images.githubusercontent.com/56102543/176602710-401fd5cb-bcbf-470a-aa83-0ec8ba7b5d78.png)

 After that, the trained uncertainty model can be used to evaluate the expectation value of the option’s payoff function analytically and with Quantum Amplitude Estimation.
 ![image](https://user-images.githubusercontent.com/56102543/176602785-2eda2e7b-9827-4c80-8254-1c85bf9e7af4.png)
 The Result we have recieved were.
 Exact value:        	0.9805
Estimated value:    	0.9638
Confidence interval:	[0.8495, 1.0781]
