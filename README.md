# Try IDA

### 2 sets given
x=c(156,190,179,141,173,159,137,174,146,152,202)  
y=c(202,206,174,195,187,180,161,171,181,176,203)  

mean(x) <= mean  
sd(x) <= standard deviation  
std.error(x) <= standard error of mean  {library(plotrix)}  
var(x)/var(y) <= Fcalc  
N-1 <= Degree of Freedom(dof), where N=sample size  
qf(p=0.95, df1=(dofX), df2=dofY) <= critical F-crit, where confidence=95(given) and dofX= degree of freedom of x set  (lower.tail=FALSE)-default TRUE  
```TRUE= probability to left of p , FALSE= probability to right of p```  

