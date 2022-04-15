# MechaCar Statistical Analysis



## Linear Regression to Predict MPG

In this section we are designing a **Linear Model** to predict the **mpg** of MchaCar prototypes.

The data has 6 variables which we are going to use for our model, so we are talking about a multiple linear regression. To be more precise in our analysis outputs we are going to review three points:

### 1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

Firstly we provide the *lm() function* with the variables and data needed as shown below.

<img width="735" alt="Captura de Pantalla 2022-04-15 a la(s) 11 32 27" src="https://user-images.githubusercontent.com/84519822/163596643-85c0ba3b-1a85-41d8-bbc7-765cdd6782f4.png">

Eventually we obtained the linear regression model with interception and slopes as you may see in the following image.

<img width="669" alt="Captura de Pantalla 2022-04-15 a la(s) 11 31 52" src="https://user-images.githubusercontent.com/84519822/163596664-fa2af928-b4fa-4fe1-b26a-1274725d476f.png">

The next step to be able to provide the information of which variables provided non-random amount of variance to the mpg values we applied the *summary() function* and got this:


<img width="476" alt="Captura de Pantalla 2022-04-15 a la(s) 11 32 40" src="https://user-images.githubusercontent.com/84519822/163596687-26eb8d49-90fd-4fd1-a301-0406c20f0b76.png">

As we know, each *Pr(>|t|)* represents the probability that each coeffincient contributes a random amount of variance to the linear model. According to our results, **Ground Clearance and Vehicle Length provide a non random amount of variance to the mpg values**. This implies that both variables have a significant impact on the mpg values.


### 2. Is the slope of the linear model considered to be zero? Why or why not?
As you will see in the results of point three, our *p-value* is *5.35e-11*. Assuming a significance level *0.05%* with our *p-value* is sufficient to reject the null hypothesis, which means that the slope of our linear model is not zero. 

### 3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

This model does predict effectively. If we observe the *r-squared* value we have a significant amount (*0.7149*). Nevertheless it might be useful to add another variables to the model, if Ground Clearance and vehicle Length are not convincing enough to the manufacturing experts. Additionally you can observe the *r-squared* value and *p-value* in the image below: 

<img width="447" alt="Captura de Pantalla 2022-04-15 a la(s) 11 32 51" src="https://user-images.githubusercontent.com/84519822/163596702-c8f2d472-95cb-4fb3-9e84-5ef78c5b4b5b.png">



## Summary Statistics on Suspension Coils

The purpose in this analysis is to to determine if the manufacturing process is consistent across production lots. The data we have isthe weight capacities of multiple suspension coils from different lots. 

The main issue is the following:
**The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?**

To start answering, we first need to take a look at our two table results: 

**Table 1: The Summary of all Three Lots**

<img width="334" alt="Captura de Pantalla 2022-04-15 a la(s) 13 06 00" src="https://user-images.githubusercontent.com/84519822/163605859-5e003587-db81-4771-82ff-11f545e70724.png">


**2. Table 2: The Summary of each Lot Individualy**

<img width="489" alt="Captura de Pantalla 2022-04-15 a la(s) 13 08 59" src="https://user-images.githubusercontent.com/84519822/163605917-1565e70a-11cf-4fa8-9ee5-9fad8dae3d6c.png">


Lets start from the basic. **Suspension coils Variance** must not exceed *100 PSI*, and this parameter is met in the first table where we observe all of the three lots variance to be *62.2935*. So concluding taking into account the three lots individually they are meeting the production requirements. 

Now, is there any **Lot** making noise individually, in oder words, not meeting the variance requirements? Lets first take a look at our second table. After diving in it we see immediatly a red light in **Lot 3** where the variance is *170.2861*. This is completely not meeting the required output. **Lot1** and **Lot3** have quite a low variance value and this helps to agree all tests as one agreed with the expectations, nevertheless it is neccesary to pay attention to **Lot3**. 



## T-Tests on Suspension Coils

While testing test for all lots, there is evidence to reject the null hypothesis and we can confirm that the means are statiscally different. You can see the *p-value* (image below) being lower than an assumpted significance level of *0.05%*.

<img width="306" alt="Captura de Pantalla 2022-04-15 a la(s) 13 47 00" src="https://user-images.githubusercontent.com/84519822/163622540-60428b2a-b40a-4803-b5c5-19fe796516fc.png">

For **Lot1** we observe there is not evidence to reject the null hypothesis, there for, we can state Lot 1 is not statiscally different to the whole population. 

<img width="510" alt="Captura de Pantalla 2022-04-15 a la(s) 14 10 45" src="https://user-images.githubusercontent.com/84519822/163622594-e8078b78-6cb7-45ed-89ef-3cd4c24b9db5.png">


For **Lot2** we observe it is exactly as with **Lot1** there is not evidence to reject the null hypothesis, there for, we can state Lot 2 is not statiscally different to the whole population. Take a closer look to the results in the following picture. 

<img width="517" alt="Captura de Pantalla 2022-04-15 a la(s) 14 10 56" src="https://user-images.githubusercontent.com/84519822/163622608-26593656-c66e-4320-8280-4a7034deccca.png">


Again for **Lot3** there is not evidence to reject the null hypothesis, there for, we can state Lot 2 is not statiscally different to the whole population. Take a closer look to the results in the following picture. Though there is something important to point out, because in this lot the *p-value* is quite larger than those in the other lots. 

<img width="499" alt="Captura de Pantalla 2022-04-15 a la(s) 14 11 08" src="https://user-images.githubusercontent.com/84519822/163622575-c419089d-c5c8-42c0-96d5-261972f7ad24.png">


