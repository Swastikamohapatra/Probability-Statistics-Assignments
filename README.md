# Brief Report on the Assignment

## Question 1
We created a probability density function from a geometric series, which was the Geometric Random Variable, and derived expressions for its mean, variance and their likelihood functions. We were then given some summary statistics, using which we found the parameters for the said distribution. We repeated the same for a Poisson distribution and compared the two models. Poisson seemed to be a better fit for the model since it has least variance and its central tendenices are closer to the expected values. 

## Question 2
We were tasked with builidng a function that returns the MLE of $log(\alpha)$, where $\alpha$ is a parameter of $\Gamma(\alpha,\sigma)$. We then demonstrated the theory of sampling distributions by sampling 20 random points from $\Gamma(\alpha, \sigma)$ and finding the MLE of $log(\alpha)$ using this sample. We repeat this process 1000 times and plot a histogram. It was observed that the column with modal frequency lies close to the expected value of MLE (log(1.5)=0.41). We also note that the gap between the $2.5^{th}$ and the $97.5^{th}$ percentile reduces as sample size increases, indicating that as $n$ increases, sampling distribution becomes more accurate to the true value.

## Question 3
We were tasked to fit a mixed probability model on the data with 3 combinations : Gamma and Normal, Gamma and Gamma and Lognormal and Lognormal. In each of the cases we estimated 5 parameters including $p$, and found the MLE using `optim` in `R`. We computed the AIC for the 3 models and reported the model with the least AIC as the best model, and using the same model. The density plot of the pdfs obtained were plotted over the histogram to visually see the goodness of fit.

## Question 4
We were tasked to fit different linear regression models on data given to us using different distributional assumptions on the errors. We considered 4 distriubtions: Normal, Laplace, Lognormal and Gamma, and for each of the 4 cases, we used `optim` in `R` to find the MLE of the parameters. We also calculated the BIC for the models and based on it, found that the model with $\epsilon_i \sim \text{Laplace}(0,\sigma^2)$ gave the lowest BIC. The regression lines were plotted over the scatter plot of the data to visually depict the goodness of fit.

## Question 5
We were tasked with estimating the parameters of a linear regression line between log returns of TCS and Nifty. We did the same in two ways, first by manual calculation using method of moments plug in estimators, i.e., $\beta_1 = Cov(X,Y)/Var(X)$, $\beta_0 = \hat{Y} - \beta_0*\hat{X}$ and $\sigma = \sqrt{(Var(Y) - \beta_0^2Var(X))}$. We cross verified our answers using the ouput from `lm` in `R`, and the outputs tallied. We also used our regression line to make a prediction on TCS returns based on Nifty returns.
