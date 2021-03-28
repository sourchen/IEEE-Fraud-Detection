# IEEE CIS fraud detection

### Goals
* classify users into "fraudlent" or "not fraudlent"
* detect fraud from customer transactions, and prevent them in the future

### introduciton to IEEE-CIS
* IEEE-CIS works across a variety of AI and machine learning areas, including deep neural networks, fuzzy systems, evolutionary computation, and swarm intelligence. Today they’re partnering with the world’s leading payment service company, Vesta Corporation, seeking the best solutions for fraud prevention industry.

### Demo 
![shiny](modelResultPlot.png)
* Online Reactive Visual Graphs via Shiny
* [Link to Shiny Demo]( https://sourlab.shinyapps.io/datascience/)
* [Link to Shiny Demo Video](https://reurl.cc/Ag1QrK)


#### Data
* The data is broken into two files **identity** and **transaction**, which are joined by `TransactionID`.
* The binary target is `isFraud`.

#### **Categorical Features - Transaction**
- `ProductCD`
- `card1` - `card6`
- `addr1`, `addr2`
- `P_emaildomain`
- `R_emaildomain`
- `M1` - `M9`

#### **Categorical Features - Identity**
- `DeviceType`
- `DeviceInfo`
- `id_12` - `id_38`

##### Note
* In the original data, not all transactions have corresponding identity information.


#### **Files**
- train_{transaction, identity}.csv - the training set
- test_{transaction, identity}.csv - the test set (you must predict the `isFraud` value for these observations)
- sample_submission.csv - a sample submission file in the correct format

#### **Model Tried**
- Null model
- LightGBM Regressor
- KNN
- SVM

#### **Reference** 
- Beginner's random forest example
https://www.kaggle.com/yoongkang/beginner-s-random-forest-example
- Beginner memory reduction techniques
https://www.kaggle.com/yoongkang/beginner-memory-reduction-techniques
- IEEE Fraud Detection EDA Step1
https://www.kaggle.com/sunghun/ieee-fraud-detection-eda-step1#3.-transactionAmt
- Data description
https://www.kaggle.com/c/ieee-fraud-detection/discussion/101203
-  LightGBM starter with R [0.9493+] LB
https://www.kaggle.com/duykhanh99/lightgbm-starter-with-r-0-9493-lb
