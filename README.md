

# 🎬 Demographically-Enhanced Movie & Book Recommendation System

A Big Data and Machine Learning project that delivers **personalized recommendations** for movies and books by leveraging **user demographics** along with collaborative and content-based filtering techniques.  

Built entirely on **AWS Cloud Services**, this system provides a scalable, real-time solution that enhances user engagement by offering cross-media recommendations (movies → books).

---

## 📖 Overview
With the explosion of content in the digital age, users face **information overload**. Traditional recommendation systems often fail to incorporate **demographics** and rarely bridge across domains (e.g., movies and books).  

This project solves that by:  
- Suggesting **movies based on user demographics** (age, gender, occupation, location).  
- Recommending **books based on the genres of suggested movies**.  
- Creating a **holistic entertainment experience** that improves discoverability across media.

---

## ✨ Features
- Hybrid recommendation using **Collaborative Filtering** + **Content-Based Filtering**.  
- Demographic-aware personalization (age, gender, location, occupation).  
- End-to-end data pipeline using **AWS Glue (PySpark, DataBrew)**.  
- Scalable ML model training and deployment via **Amazon SageMaker**.  
- Real-time recommendations served through **Lambda + API Gateway**.  
- User-friendly web app powered by **AWS Amplify + Cognito**.  
- Interactive **dashboards & visualizations** using **Amazon QuickSight**.

---

## 🛠️ Tech Stack
- **Languages & Libraries**: Python, PySpark, SQL  
- **Big Data & ETL**: AWS Glue, AWS DataBrew, AWS Redshift  
- **Machine Learning**: Amazon SageMaker (K-Nearest Neighbor, custom ML)  
- **Backend & APIs**: AWS Lambda, AWS API Gateway  
- **Frontend**: AWS Amplify, React, Cognito for Authentication  
- **Database**: Amazon DynamoDB  
- **Visualization**: Amazon QuickSight  

---

## 📂 Project Structure


demographic-recsys/
├── data/                 # Raw & cleaned datasets (MovieLens, Goodreads)
├── etl/                  # PySpark ETL scripts for AWS Glue
├── models/               # Trained ML models
├── src/
│   ├── recommender.py    # Core recommendation logic
│   ├── api\_lambda.py     # AWS Lambda handler
│   ├── utils.py          # Helper functions
├── frontend/             # Amplify web app code
├── dashboards/           # QuickSight dashboards
├── assets/               # Diagrams & images
├── README.md             # Project documentation

````

---

## 🚀 Getting Started

### 1. Clone the REPO
bash
git clone https://github.com/<your-username>/demographic-recsys.git
cd demographic-recsys


### 2. Set up environment

* Install dependencies:

  ```bash
  pip install -r requirements.txt
  ```
* Configure your AWS CLI with appropriate IAM credentials.
* Ensure S3, Glue, Redshift, SageMaker, DynamoDB, and Amplify services are active.

### 3. Run ETL Pipeline

* Upload raw datasets (MovieLens + Goodreads) to an S3 bucket.
* Trigger **AWS Glue crawler + ETL script** to clean and transform data.
* Load transformed data into **Redshift**.

### 4. Train the Model

```bash
# Example: Train KNN model in SageMaker
python src/recommender.py --train --algorithm knn
```

### 5. Deploy Model

* Deploy ML model via **SageMaker Endpoint**.
* Connect API Gateway + Lambda to expose recommendations as REST API.

### 6. Run the Web App

```bash
cd frontend
npm install
npm start
```

---

## 📊 Datasets

* **Movie Dataset**: [MovieLens 1M Ratings](https://www.tensorflow.org/datasets/catalog/movie_lens#movie_lens1m-ratings)
* **Book Dataset**: [Goodreads Best Books of the 21st Century](https://www.kaggle.com/datasets/justinnguyen0x0x/best-books-of-the-21st-century-dataset)

---

## 🏗️ System Architecture

![System Architecture](assets/system_architecture.png)

---

## 🔄 ETL Workflow

![ETL Workflow](assets/etl_workflow.png)

---

## 🌐 Web Integration Workflow

![Web Integration](assets/web_integration.png)

---

## 📈 Visualizations

Dashboards created with **Amazon QuickSight** include:

* Ratings by **timestamp**
* Ratings distribution by **occupation**
* Multi-factor analysis: **occupation × genre × gender**
* Geo-distribution by **zip code**
* Interactive **dashboard** for cross-media recommendations

![QuickSight Dashboard](assets/dashboard.png)

---

## 🎯 Future Work

* Integrate with **voice assistants** (e.g., Alexa).
* Use **context-aware recommendations** (mood, time-of-day).
* Expand beyond movies/books into **music or podcasts**.
* Add fairness-aware ML to avoid bias in demographic-based recs.

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo
2. Create a branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -m "Add new feature"`)
4. Push (`git push origin feature/new-feature`)
5. Submit a Pull Request

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 🙏 Acknowledgements

* MovieLens (GroupLens Research)
* Goodreads (Kaggle dataset)
* AWS Educate & SJSU DATA 228 course
* Project Team: Priya Varahan, Priyanka Akula, Pooja Manjunatha, Shreya Chikatmarla, Nandini Sreekumaran Nair

```

