# Analysis-of-Ebola-Epidermic-in-West-Africa-using-ODE-s-and-PDE-s
This project analyzes Ebola Epidemic in West Africa. In this project, the dataset was obtained from World Health Organization (WHO). Dataset contains variables such as countries, confirmed, probable, annd suspected cases and deaths. In my analysis, I will focus on creating a SIR model using ODE'S and PDE's. The SIR model we compose of Susceptible, Infected and Removed individuals because my dataset has only infected and dead people. 


Assumptions are as follows:   

1. People from susceptible group can only leave this group by being infected. For an infected person to leave the group. he or she has either recover from the disease and acquired immunity or has died.   


2. Transmission rate and death rate are the same for all people and they should be positive values.   


3. People in the population make random contact with one another.   


4. There is no vaccination available   


5. There is a closed environment where individuals are not allowed to leave or enter 


6. We do not consider child birth or recovered individuals   


Equations are as follows:   

N = S + I + R   


dS/dt = −α/ N ∗S(t) ∗I(t)   


dI/ dt = α/N ∗S(t) ∗I(t) −λ ∗I(t)   


dR/dt z = λ ∗I(t)  


In addition, I will concentrate on estimating parameters on two countries; Sierra Leone and Guinea. Further, I will use as nonlinear model fit to fit my dataset of the two countries sand obtain the transmission and death rate. Moreover, I will look into the residuals to see error rate.   


For PDE's, I will only create SIR model that focus on spatial mobility.


My assumptions are as follows: We will assume that the spatial mobility is governed by random diffusion coefficients DS , DI , and DR for Susceptible, Infected, and Removed group. Further, we will assume that the spatial position is a bounded one-dimensional environment, [0,L] with L > 0. So the number of susceptible individuals at location x in time t would be S = S(t,x). the number of infected individuals at location x in time t would be I = I(t,x) and the number of Removed individuals at location x in time t would be R = R(t,x). Lastly, we assume that we have homogeneous Neumann boundary conditions which represents a closed environment where there is no birth, people can’t leave or enter the population, and we only consider people who died from the virus.   


Equations are as follows:  


dS/dt = −α/N ∗S(t) ∗I(t) + D_{S} * S_{xx} 



dI/ dt = α/N ∗S(t) ∗I(t) −λ ∗I(t) + D_{R} * I_{xx }   



dR/dt = λ ∗I(t) + D_{R} * R_{xx}  



S_{x}(t,0) = S_{x}(t,L) = I_{x}(t,0) = I_{x}(t,L) = R_{x}(t,0) = R_{x}(t,L) = 0
