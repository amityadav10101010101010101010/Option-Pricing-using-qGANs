# Option-Pricing-using-qGANs
A quantum Generative Adversarial Network (qGAN) can facilitate the pricing of a European call option. More specifically, a qGAN can be trained such that a quantum circuit models the spot price of an asset underlying a European call option. The resulting model can then be integrated into a Quantum Amplitude Estimation based algorithm to evaluate the expected payoff - see European Call Option Pricing. 

The Black-Scholes model assumes that the spot price at maturity Sₜ for a European call option is log-normally distributed. Thus, we can train a qGAN on samples from a log-normal distribution and use the result as an uncertainty model underlying the option. In the following, we construct a quantum circuit that loads the uncertainty model. The circuit output reads
![image](https://user-images.githubusercontent.com/56102543/176603871-c8a287a5-2d17-4fee-b9b5-84d74a1996e5.png)

where the probabilities <math xmlns="http://www.w3.org/1998/Math/MathML">
  <msubsup>
    <mi>p</mi>
    <mrow data-mjx-texclass="ORD">
      <mi>&#x3B8;</mi>
    </mrow>
    <mrow data-mjx-texclass="ORD">
      <mi>j</mi>
    </mrow>
  </msubsup>
</math>, for , represent a model of the target distribution.
 Then the trained uncertainty model can be used to evaluate the expectation value of the option’s payoff function with Quantum Amplitude Estimation.
 Next, we plot the trained probability distribution and, for reasons of comparison, also the target probability distribution.
 
 ![image](https://user-images.githubusercontent.com/56102543/176602710-401fd5cb-bcbf-470a-aa83-0ec8ba7b5d78.png)

 After that, the trained uncertainty model can be used to evaluate the expectation value of the option’s payoff function analytically and with Quantum Amplitude Estimation.

![image](https://user-images.githubusercontent.com/56102543/176602785-2eda2e7b-9827-4c80-8254-1c85bf9e7af4.png)
 
 The Result we have recieved were.
 Exact value:        	0.9805
Estimated value:    	0.9638
Confidence interval:	[0.8495, 1.0781]
