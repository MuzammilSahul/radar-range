# EVALUATION OF RADAR RANGE

## Aim:
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through SCILAB

## Theory:
The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:
<img width="552" height="453" alt="image" src="https://github.com/user-attachments/assets/8fcfa748-7baf-4ded-80ed-36ff0fbf470e" />



## Procedure
1.	Set Up the SCILAB Environment: Ensure that SCILAB is installed on your system. 
2.	Define the Radar Range Equation Function: Create a function to calculate the maximum range using the Radar Range Equation.
3. Input Parameters for the Radar System: Define the input parameters such as transmitted power, transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power.
4.	Calculate the Maximum Range: Use the function to calculate the maximum range of the radar.
5.	Execute the Program: Run the Python script to calculate and display the maximum range of the radar.

## Program:
Gt = 48; 

Gr = 48;       

lambda = 0.08;  

sigma = 2;      

Pmin = 1e-10;

Pt = linspace(1,1000,100); 

Rmax1 = ((Pt .* Gt .* Gr .* lambda^2 .* sigma) ./ ((4*%pi)^3 .* Pmin)).^(1/4);

subplot(2,1,1)

plot(Pt, Rmax1)

Pt_const = 700; 

Pmin2 = linspace(1e-12,1e-8,100);

Rmax2 = ((Pt_const .* Gt .* Gr .* lambda^2 .* sigma) ./ ((4*%pi)^3 .* Pmin2)).^(1/4);

subplot(2,1,2)

plot(Pmin2, Rmax2)



## Output:

![WhatsApp Image 2026-03-30 at 17 58 01 (2)](https://github.com/user-attachments/assets/0c7197b9-03ae-4734-986c-ac933aa6d7a2)
![WhatsApp Image 2026-03-30 at 18 47 50](https://github.com/user-attachments/assets/61f41d6c-ea6c-4a6a-a5b1-a0f86d8ce2b2)


## Result:

Thus, the maximum range of a radar system using the Radar Range Equation is verified through a Python program.
