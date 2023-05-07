Download Link: https://assignmentchef.com/product/solved-fin5350-final-project
<br>
Create a Python module in a file names options.py. A sample file is included in the folder for this project. You will add to this module as you progress through the final project. You will import it into various notebooks that will contain your answers to the problems below.

<h1>Part I: The European Binomial Option Pricing Model</h1>

Write a Jupyter notebook named Part-One.ipynb to solve the following problems. You should import the options.py module in the first code cell of the notebook as follows: import options as opt

<h2>Problem 1</h2>

<ul>

 <li><strong>(a) </strong>Complete the function european_binomial_pricer in the options.py module to implement the multiperiod European binomial option pricing model. This step is to be completed before you import the module into your notebook.</li>

 <li><strong>(b) </strong>Verify that it works for both call and put options with <em>n </em>= 1 (i.e. a single period). Compare against a hand-written solution. Assume the following:

  <ul>

   <li>Let <em>S</em><sub>0 </sub>= $100</li>

   <li>Let <em>K </em>= $105</li>

   <li>Let <em>r </em>= 8%</li>

   <li>Let <em>T </em>= 1 year</li>

   <li>Let <em>δ </em>= 0<em>.</em>0 (i.e. no dividends)</li>

   <li>Let <em>σ </em>= 20%</li>

  </ul></li>

 <li><strong>(c) </strong>Verify that it works for both call and put options with <em>n </em>= 3. Compare against a hand-written solution. Use the same parameters as above in <strong>(b)</strong>.</li>

 <li><strong>(d) </strong>What happens if you set <em>n </em>= 200? Solve for both the call and put prices. <strong>DO NOT </strong>try to solve by hand! Again, use the parameter values from <strong>(b)</strong>.</li>

</ul>

<h2>Problem 2</h2>

<ul>

 <li><strong>(a) </strong>Use the functions included in options.py to price the call and put option from <strong>Problem 1 </strong>part <strong>(b) </strong>with the Black-Scholes option pricing model. See McDonald Chapter 12 for background on the Black-Scholes option pricing model.</li>

 <li><strong>(b) </strong>Use the european_binomial_pricer function with the following values: <em>n </em>= 20<em>,</em>40<em>,</em>60<em>,</em>80<em>,…,</em>200 (i.e. increment by 20). Compare to the Black-Scholes prices obtained above. Make a table to report the results. What can you say about the European Bimomial model relative to the Black-Scholes model? Discuss the convergence of the European Bimomial to the Black-Scholes model.</li>

</ul>

<h1>Part II: The American Binomial Option Pricing Model</h1>

Write a Jupyter notebook named PartTwo.ipynb to solve the following problems. You should import the options.py module in the first code cell of the notebook as follows: import options as opt

<h2>Problem 1</h2>

<ul>

 <li>Using the functions european_binomial_call and european_binomial_put as starting points, implement the functions american_binomial_call and american_binomial_put. These functions should solve the optimal stopping problem implicit in the American option pricing problem. Write your solutions in the options.py module. This step is to be completed before you import the module for the problems below.</li>

</ul>

<h2>Problem 2</h2>

<ul>

 <li><strong>Set-up: </strong>Let <em>S</em><sub>0 </sub>= $100, <em>K </em>= $95, <em>r </em>= 8% (continuously compounded), <em>σ </em>= 30%, <em>δ </em>= 0, <em>T </em>= 1 year, and <em>n </em>= 3.</li>

 <li><strong>(a) </strong>Verify that the binomial option price for an American call option is $18<em>.</em> Verify that there is never early exercise; hence a European call would have the same price. Compare your Python solution to a hand-written solution.</li>

 <li><strong>(b) </strong>Show that the binomial option price for a European put option is $5<em>.</em> Verify that put-call parity is satisfied.</li>

 <li><strong>(c) </strong>Verify that the price of an American put is $6<em>.</em></li>

 <li><strong>(d) </strong>Repeat each of the above for <em>n </em>= 200. How can you be sure there is never early exercise of the American call from part <strong>(a)</strong>? <strong>DO NOT </strong>attempt to solve this part by hand!</li>

</ul>

<h2>Problem 3</h2>

<ul>

 <li>Repeat the previous problem assuming that the stock pays a continuous dividend of 8% per year (continuously compounded).</li>

 <li>Calculate the prices of the American and European puts and calls.</li>

 <li>Which options are early-exercised? Explain your answer.</li>

</ul>

<h1>Part III: Simulating Binomial Trees</h1>

Write a Jupyter notebook named PartThree.ipynb to solve the following problems. Make sure to import the options.py module at the top of your notebook. You should know how to do that by now, so I won’t belabor the point.

<h2>Problem 1</h2>

<ul>

 <li>Complete the function binomial_path in the options.py module that simulates a binomial path.</li>

 <li>This step is to be completed prior to being imported for the problem below.</li>

</ul>

<h2>Problem 2</h2>

<ul>

 <li><strong>Set-up: </strong>Let <em>S</em><sub>0 </sub>= $100, <em>r </em>= 8% (continuously compounded), <em>σ </em>= 30%, <em>δ </em>= 5%, and <em>T </em>= 1 year.</li>

 <li>Set <em>n </em>= 252 (i.e. roughly the number of trading days per year so that each sub-period is a single day).</li>

 <li>Simulate a binomial path using your new function.</li>

 <li>Use the Matplotlib.pyplot function plot to make a plot of your simulated path. Label your axes appropriately.</li>

</ul>

<h2>Extra Credit</h2>

<ul>

 <li><strong>Set-up: </strong>Let <em>S</em><sub>0 </sub>= $41<em>.</em>0, <em>K </em>= $40<em>.</em>0, <em>T </em>= 1 year, <em>σ </em>= 30% per annum, <em>r </em>= 8% per annum, <em>δ </em>= 0.</li>

 <li>Price both European call and put options with the Black-Scholes model and the European Binomial model with <em>n </em>= 200 time steps.</li>

 <li>Now write a function that prices the European call and put via Monte Carlo simulation.

  <ul>

   <li>The solution should use your binomial path simulation to simulate <em>M </em>= 10<em>,</em>000 simulated paths through the tree.</li>

   <li>This will give you <em>M </em>different terminal stock prices.</li>

   <li>Get the corresponding option payoffs using the payoff function.</li>

   <li>Take an average of the option payoffs with the Numpy method np.mean.</li>

   <li>Discount this value to time zero and compare it with the Black-Scholes and European Binomial model prices.</li>

   <li>Also calculate the standard error of the simulation with np.std and divide by np.sqrt(M).</li>

   <li>Repeat for <em>M </em>= 25<em>,</em>000;50<em>,</em>000;75<em>,</em>000;and;100<em>,</em></li>

   <li>Make a table to report the data (both discounted mean and standard errors).</li>

  </ul></li>

</ul>