# Intro2Biophysics
This page presents the code needed to solve the Problem Set \#2 in "Introduction to Biophysics" course. All the files connected to the PS2 are modifications of the initial code from [PNelson code](https://github.com/NelsonUpenn/PNelson_code).

### PS2\_task3\_a.ipynb
This file outputs the number of mistakes and total time of translation for several mRNAs for 3 different models: the Hopfield-Ninio model where selectivity is through unbinding (HN), a model that discriminates mainly by forward rates (FRD), and a model that uses *in vitro* measured rates (Realistic).

For this part I rewrote the definition of the **ribosim** function by adding the parameters for the FRD model. Also I noticed some mistakes in the parameters of HN model (<img src="https://render.githubusercontent.com/render/math?math=k_{add,c}"> was 0.01 instead of 0.001 and <img src="https://render.githubusercontent.com/render/math?math=\phi_{-1}"> was 5 instead of 94). I put <img src="https://render.githubusercontent.com/render/math?math=\phi_{-1}=94"> as it should be and <img src="https://render.githubusercontent.com/render/math?math=k_{add,c}=0.005"> because with the right value the calculations were too long..

*here I needed to use the numpy version 1.16.1 to exlude an error with np.load comand



### PS2\_task3\_b.ipynb
This code outputs the number of mistakes and average translation rate (for one certain chain and with the respect to the number of experiments) for 3 mentioned models.

For this part I put <img src="https://render.githubusercontent.com/render/math?math=k_{add,c}=10^3"> for all 3 models. I calculated the average rate for each mRNA chain by considering 

 <img src="https://render.githubusercontent.com/render/math?math=\text{rate}_i = \dfrac{\text{length of the chain}_i}{\text{total translation time for the chain}_i}">

I wrote this value to the array **rate**. Also I calculated and output the average rate with the respect to the number of experiments (number of chains), so 

<img src="https://render.githubusercontent.com/render/math?math=\text{ave\_rate} = \frac{\sum_i\text{rate}_i}{\text{number of chains}}">



### PS2\_task3\_c.ipynb
This code outputs plot which depicts the function of wrong AAs VS a function of the average rate on a semi-log scale. I increased the number of chains to highlight that values are distributed in a distinguishable separate areas. 



### PS2\_task6\_2d.ipynb
This code shows modelling of 2D self-avoiding random walk up to 200 steps. 



### PS2\_task6\_3d.ipynb
Not necessary, but this code shows modelling of 3D self-avoiding random walk up to 2000 steps. 
