#  Customer Churn Prediction using Machine Learning

This project predicts whether a telecom customer is likely to **churn** (i.e., stop using the service) based on demographic and service usage data.
It uses **Machine Learning** models built in Python, packaged and run inside **Docker** for portability and reproducibility.

---

##  Project Structure

```
Customer churn prediction/
│
├── Customer_Churn_Prediction_using_ML.ipynb   # Main Jupyter notebook
├── WA_Fn-UseC_-Telco-Customer-Churn.csv       # Dataset
├── customer_churn_model.pkl                   # Trained ML model
├── encoders.pkl                               # Encoders for categorical features
├── requirements.txt                           # Python dependencies
├── Dockerfile                                 # Docker setup for environment
└── README.md                                  # Project documentation
```

---

##  Features

* End-to-end **ML pipeline**: data preprocessing → feature encoding → model training → prediction
* Uses **Logistic Regression / Random Forest / XGBoost** (depending on notebook logic)
* Visualizes key trends in customer churn
* Fully **Dockerized** for consistent execution across systems
* Easy to extend into a **Flask/FastAPI web app** for deployment

---

##  Setup Instructions (Locally)

### Prerequisites

* [Docker Desktop](https://www.docker.com/products/docker-desktop/) installed and running.

### Steps

1. **Clone the repository**

   ```bash
   git clone https://github.com/<your-username>/customer-churn-docker.git
   cd customer-churn-docker
   ```

2. **Build the Docker image**

   ```bash
   docker build -t customer-churn-app .
   ```

3. **Run the container**

   ```bash
   docker run -p 8888:8888 -v "${PWD}:/app" customer-churn-app
   ```

4. Copy the **Jupyter Notebook link** shown in the terminal and open it in your browser.

---

## 🧩 Inside the Notebook

The notebook performs:

1. **Data Exploration (EDA)** – Visualizing distributions, correlations, churn patterns
2. **Feature Engineering** – Encoding categorical data, handling missing values
3. **Model Building** – Training ML algorithms and evaluating accuracy
4. **Model Saving** – Exporting trained model and encoders using `pickle`
5. **Prediction** – Using the saved `.pkl` model to predict churn on new data

---

## 🐳 Running Notes Inside Docker

If your dataset or notebook changes on your host machine, they will automatically sync into the container because of the `-v "${PWD}:/app"` volume mapping.

Stop the container anytime with **Ctrl + C**.

---

## 🤝 Contributing

Feel free to fork this repo, improve model accuracy, or containerize a web-based UI using Flask or Streamlit.

---

## 🧑‍💻 Author

**Basavaraj Nadagouda**
📧 [[your-email@example.com](mailto:your-email@example.com)]
🐙 [GitHub](https://github.com/<your-username>)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
