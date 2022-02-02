# Try IDA

### 2 sets given
x=c(156,190,179,141,173,159,137,174,146,152,202)  
y=c(202,206,174,195,187,180,161,171,181,176,203)  

mean(x) <= mean  
sd(x) <= standard deviation  
std.error(x) <= standard error of mean  {library(plotrix)}  
var(x)/var(y) <= Fcalc  
N-1 <= Degree of Freedom(dof), where N=sample size  


### Calculating the Confidence Interval

- n= Sample Size
- σ= standard deviation, s= estimated standard deviation
- μ= mean, x= estimated mean  
- u= critical value  

#### CI on Mean of a Normal Distribution, Variance Known 
[x-(σ/sqrt(n))*u || x+(σ/sqrt(n))*u]  
To calculate u :  
suppose we are given 99% confidence interval => so 1-α= 1-0.95=0.05, here 0.05 is α => ```qnorm(0.05)``` is the value of u

#### CI on Mean of a Normal Distribution, Variance Unknown     
[x-{(s/sqrt(n))*t(n-1,1-(α/2))} || x+{(s/sqrt(n))*t(n-1,1-(α/2))}]      
To calculate t(n-1,1-(α/2)) :    
suppose we are given 99% confidence interval => so 1-α= 1-0.95=0.05, here 0.05 is α => ```qt((1-(α/2)),n-1)``` is the value of t 

#### CI on Variance of a Normal Distribution, Mean
``` Answer comes in the form of Variance, so always take SQRT() for Std. Deviation```
##### Mean Knownt
##### Mean Unknown








------***********-------***********-------***********-------***********-------***********-------***********-------  
qf(p=0.95, df1=(dofX), df2=dofY) <= critical F-crit, where confidence=95(given) and dofX= degree of freedom of x set  ```(lower.tail=FALSE)-default TRUE```    
```TRUE= probability to left of p , FALSE= probability to right of p```  
1-pf(1.996737, 10, 10) <= Pvalue corresponding to Fcalc ```1-pf(Fcalc, df1, df2)```  

## Mock Exam P1   
```Q3: Body temperature was measured by telemetry every 10 minutes for a female beaver ``` 
- ``` Load the data set beaver1 in the package datasets ```
- Installing Package: Package => Install Pacakage => Germany(Gottingen){If not selected} => Required Package  
- On console => library(packageName)  
- Loading the dataset => data(datasetName)  OR datasetName{directly name}
- summary(datasetName)  <= to know about the given data  
- ``` mean of the variable temp```    
- b=beaver1 <= variable name   
- b$temp <= accessing the column value  
- mean(b$temp) <= mean of values  
- ```  construct a 95% two-sided confidence interval for the population mean ```  
- t.test(b$temp, conf.level=0.95)
