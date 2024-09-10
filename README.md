# Fine Grained Time Series Forecasting of Energy Demand
[→Colab Notebook](https://colab.research.google.com/drive/1R1FFWLYn06mv4ePZDjAsePn6pXLX5Omy?usp=sharing#scrollTo=WUbAEd85M40c)

<img src="https://user-images.githubusercontent.com/75590579/167874801-5005404a-6d06-408a-874b-0f45991e98f5.png" alt="drawing" width="600"/>

### Problem Analysis:
Reading the book "Blackout" by Marc Elsberg I realized, that the power grid might be more fragile than I thought. For the first time I consciuosly was confronted with the problem of balancing the supply and demand of electric power in the grid.

The power demand varies because of consumer habits, industrial workhours, air temperature and many more factors.

Do the energy companies have to match this varying demand?

Is a constant power output in form of a base load by various power plants enough ?

**Background**: In an alternating current grid a surpassing demand (Demanded Load> Supplied Load) will be balanced by the drop of the frequency in the grid. As a consequence the connected appliances like generators e.g. a turbine as well as the consumers have to operate with reduced frequency. In the european grid with a base frequency of 50Hz a frequency change of maximal +0.5Hz or -0.5Hz is allowed. Frequencies below or above this range lead to emergency shutdowns of generators and in severe cases ultimately to partial blackouts.
### The Data
The dataset from [Kaggle](https://www.kaggle.com/robikscube/hourly-energy-consumption) contains the load development of several regions in the US. Trying to understand the data from a standpoint of a energy provider, I was interested in single regions only. Different regions were not compared or merged together. In the following only the "AEP_hourly.csv" dataset was used. AEP is a energy company in the US: https://en.wikipedia.org/wiki/American_Electric_Power

In the following models were trained with different forecasting horizons.Horizons were: 1h, 6h, 24h and sometimes even higher. To stay consistent the majority of models was evaluated and compared using a forecast horizon of 6h.
### Overview of the Notebook:

**1. Data Exploration and Preparation**

**2. Choosing a measure of loss**

**3. Testing Phase 1**

    Intro to Visualization Of Results
    
    Primitive Lag Model
    
    SARIMA
    
        SARIMA 6h
        
    Support Vector Regression SVR
    
        SVR 6h
        
    Lasso
    
        Lasso 6h
        
    Random Forest
    
        GridSearch
        
        Random Forest 6h
        
**4. Testing Phase 2**

    RNN
    
        RNN 6h
        
    LSTM
    
    Autoencoder LSTM
    
        Autoencoder 6h Reference
        
        Autoencoder Feature-GridSearch
        
        Autoencoder with Features 6h
        
**5. Testing Phase 3**

        Autoencoder Hyperparameter-GridSearch
        
        Autoencoder fully tuned 6h
        
**6. Evaluation/Comparison of the model predictions**

**7. Lessons Learnt**

**8. Bonus: FFT Longterm Prediction Trial**




