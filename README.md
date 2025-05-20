# IoT-Based Smart Irrigation System Using Reinforcement Learning

This project helps farmers by using IoT and machine learning to decide how much water the crops need. It uses sensors to check the soil and weather conditions. Then it uses a learning algorithm to decide whether the field is **Very Dry**, **Dry**, **Wet**, or **Very Wet**, and automatically turns the water on or off.

---

## What the Project Does

- Reads data from sensors (temperature, humidity, etc.)
- Uses a learning method called **Reinforcement Learning (RL)** to predict field condition
- Automatically decides when to water crops
- Shows graphs of performance and predictions

---

## How the System Works

- **IoT devices** collect field data (like temperature and pressure).
- **RL Algorithm** learns from this data and predicts the field condition.
- Based on the prediction, it controls the water supply.
- It tries to make the correct decision to get **rewards**. Wrong decisions give **penalties**.

---

## Project Structure

```plaintext
.
├── DataSet/
│   ├── IrrigationScheduling.csv
│   └── TestData.csv
├── ScreenShot/
│   ├── ScreenShot1.png
│   ├── ScreenShot2.png
│   ├── ScreenShot3.png
│   ├── ScreenShot4.png
│   ├── ScreenShot5.png
│   ├── ScreenShot6.png
│   ├── ScreenShot7.png
│   ├── ScreenShot8.png
│   └── ScreenShot9.png
├── Agent.py
├── Environment.py
├── requirements.txt
├── run.bat
└── SmartIrrigation.py
```

---

## Datasets

1. IrrigationScheduling

It includes data like id, temperature, pressure, altitude, soilmiosture, note, status, class, date, and time. The model learns from this data to predict the right field status.

2. TestData

It includes data like id, temperature, pressure, altitude, soilmiosture, note, status, date, and time.

---

## Steps to Run the Project

1. Install the required libraries:

   ```bash
   pip install -r requirements.txt
  ```

2. Run the application to get below screen:

   On Windows(Double click on ‘run.bat’ file):

   ```bash
   run.bat
   ```

   Or Manually(Run in terminal):

   ```bash
   python SmartIrrigation.py
   ```

![Screenshot 1](ScreenShot/ScreenShot1.png)

3. Upload Dataset:

In above screen click on ‘Upload Irrigation Dataset’ button to upload dataset and get below output.

![Screenshot 2](ScreenShot/ScreenShot2.png)

4. Select and Open Dataset:

In above screen click on ‘Open’ button to load dataset and get below output.

![Screenshot 3](ScreenShot/ScreenShot3.png)

5. View Dataset Graph and Preprocess the Dataset:

In above screen dataset loaded and in graph can see types of field condition where x-axis represents Condition and y-axis represents number of instances that condition hold in dataset and now close above graph and then click on “Pre-process Dataset” button to clean and normalized dataset and get below output.

![Screenshot 4](ScreenShot/ScreenShot4.png)

6. Split Dataset into Train and Test:

In above screen can see normalized dataset values and then click on ‘Dataset Train & Test Split’ button to split dataset into train and test and then will get below output.

![Screenshot 5](ScreenShot/ScreenShot5.png)

7. Train RL Algorithm:

In above screen can see train and test size and now click on ‘Train Reinforcement Learning Algorithm’ button to train RL and get below output.

![Screenshot 6](ScreenShot/ScreenShot6.png)

8. Rewards vs Penalties Graph:

In above screen can see number of rewards and penalties earned by RL by predicting on test data and can see penalties are very few compared to rewards so RL can predict field condition accurately and now click on Rewards & penalty Graph’ to get below graph.

![Screenshot 7](ScreenShot/ScreenShot7.png)

9. Predict Field Condition:

In above graph x-axis represents earned type and y-axis represents values and can see Rewards are more compare to Penalties and now close above graph and then click on ‘Predict Irrigation Status’ button to upload test data and get prediction.

![Screenshot 8](ScreenShot/ScreenShot8.png)

10. Upload Test Data:

In above screen uploading test data and then click on ‘Open’ button to load test data and get below prediction.

![Screenshot 9](ScreenShot/ScreenShot9.png)

11. View Prediction Output:

In above screen in square bracket can see test data and after square bracket can see predicted field condition as Wet, Dry, Very Wet or Very Dry and based on above prediction IOT will give water to crop.
