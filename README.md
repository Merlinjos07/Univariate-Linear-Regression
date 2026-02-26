# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```

import numpy as np
import matplotlib.pyplot as plt
x=np.array([0,1,2,3,4,5,6,7,8,9])
y=np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()


```


```

xm=np.mean(x)
ym=np.mean(y)

num=0
den=0
for i in range(len(x)):
    num +=(x[i]- xm)*(y[i]-ym)
    den +=(x[i]-xm)**2
m=num/den
c=ym-m*xm
print(m,c)

```



```

yp=m*x+c
print(yp)
plt.scatter(x,y)
plt.plot([min(x),max(x)],[min(yp),max(yp)],color='red')
plt.show()
```

## Output

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2211d8eb-c084-4968-934a-8bcc3408b20f" />


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/78bb1aa0-74b8-4c67-a197-abe0b910ed2b" />


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/457db1d2-6fbe-44d8-8d45-c7ca7028b2e6" />




## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
