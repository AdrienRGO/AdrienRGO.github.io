# DPAE & ESSA Times Series Forecasting

## **1. About this project**

This school project was proposed to **handle time series**. The code is available [here](https://github.com/AdrienRGO/DPAE_ESSA_Times_Series_Forecasting).


In this project, we face **two databases**: 

  - **Monthly pre-employment declarations** *(DAPE)* of more than one month, France (2000 - 2022) : [Tableau_DPAE_CSV.csv](https://github.com/AdrienRGO/DPAE_ESSA_Times_Series_Forecasting/blob/main/Tableau_DPAE_CSV.csv)
  
  <div id="DAPE" align = "center">
    <img src="https://user-images.githubusercontent.com/105392989/176622151-ed4ae0c9-a0ef-4631-a24b-3ddfb8112f44.png" width="850">
  </div>
  
  - **Estimates of salaried employment** by sector of activity (EESSA), 80 sectors, 1970 - 2022 : [EESSA.csv](https://github.com/AdrienRGO/DPAE_ESSA_Times_Series_Forecasting/blob/main/EESSA.csv)
  
  <div id="EESSA" align = "center">
    <img src="https://user-images.githubusercontent.com/105392989/176622216-d78bfeeb-544b-4933-a0d8-f67b28ac37c8.png" width="850">
  </div>
  
This project will be addressed in several points, namely: 

  1. A **pre-processing of the data** including cleaning, formatting and visualizing the data
  2. Evaluate the **seasonality** and the **correlation** of time series
  3. Time series forecasting using the **exponential smoothing** method.
  4. An **evaluation of the prediction** previously made
  5. Comparison of this prediction with **other methods** 

This project was done in a school context with two other classmates.

## **2. A first visual and statistical approach**

Before attacking the problem as a whole, it is **crucial** to know **what data we are manipulating**. This is why we are interested in the manipulation of dataframes to observe certain characteristics.   
Moreover, this allows us to observe general statistics quite easily, especially with **white boxes** or **graphs that show the evolution over time**.

<div id="first approach" align = "center">
    <img src="https://user-images.githubusercontent.com/105392989/176622520-2567cd78-cace-49fe-910c-edbda6847bb6.png" width="850">
    <br></br>
    <img src="https://user-images.githubusercontent.com/105392989/176622637-e59f01c2-4ed8-46d8-abf9-4b441d266333.png" width="850">
</div>

## **3. Seasonality and trend**

In this section, multiple tools are used such as : 

  **1. The pivot**
  
  <div id="pivot" align = "center">
    <img src="https://user-images.githubusercontent.com/105392989/176622883-577f9d56-119c-4dfc-a2a2-2f4edb08229f.png" width="850">
  </div>

  **2. Autocorrelation**
  
  <div id="autocorrelation" align = "center">
    <img src="https://user-images.githubusercontent.com/105392989/176622952-77f0db08-4822-446d-ab73-99057aca63a0.png" width="850">
  </div>

  **3. Seasonal decomposition** 
  
  <div id="seasonal decomposition" align = "center">
    <img src="https://user-images.githubusercontent.com/105392989/176623121-922ce049-80d9-46ab-bd43-d524c86cf5d4.png" width="850">
  </div>

  **4. Correlation study between two different signals**

## **4. Models used for prediction**

As in machine learning, it is essential to **split our data into two parts**, namely a training part and a test part to **check if the prediction made is correct**.  
This simply allows us to **measure the error** and therefore the **relevance** of the implemented model!

<div id="prediction" align = "center">
    <img src="https://user-images.githubusercontent.com/105392989/176623576-e2bcd2b8-e950-4086-aaaf-eb29e14c6ab2.png" width="850">
</div>

We therefore used **five models**, namely : 

  **1. Simple exponential smoothing *(SES)***
  
  <div id="SES" align = "center">
    <img src="https://user-images.githubusercontent.com/105392989/176623701-305c6f2c-ddbf-430b-adf1-fb8819e10cad.png" width="850">
  </div>

  **2. Holt Winter seasonal model**
  
  <div id="Holt Winter" align = "center">
    <img src="https://user-images.githubusercontent.com/105392989/176623927-374ba663-2406-4636-947a-2e37768fa8cf.png" width="850">
  </div>
  
  **3. Autoregressive integrated moving average *(ARIMA)***
  
  <div id="ARIMA" align = "center">
    <img src="https://user-images.githubusercontent.com/105392989/176624019-023ed933-b146-4165-842f-d54fdcd71928.png" width="850">
  </div>
  
  **4. Seasonal autoregressive integrated moving average *(SARIMA)***
  
  <div id="ARIMA" align = "center">
    <img src="https://user-images.githubusercontent.com/105392989/176624107-ffa40caf-cc3b-4262-89a3-9a23ec1ff693.png" width="850">
  </div>
  
  **5. None seasonal Holt Winter's exponential smoothing**
  
  <div id="ARIMA" align = "center">
    <img src="https://user-images.githubusercontent.com/105392989/176624349-981edc65-5d78-4433-b0f2-f9b396b288b8.png" width="850">
  </div>