# 🎬 CineSeek: Personalized Movie Suggestion Engine

| Section                                  | Overview                                                                                                            |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| 🎥 **Demo**                              | Explore CineSeek in action with a live demo hosted on a cloud-based PaaS platform                                   |
| 📦 **Dependencies**                      | List of packages and step-by-step setup instructions for running CineSeek locally                                   |
| 🧠 **Model Training**                    | Guide on how CineSeek’s recommendation model was trained on movie data and how you can adapt it for your own use   |
| 🌐 **Deployment**                        | Detailed guide on deploying the project on cloud servers or running it on your local system                        |
| 🛠️ **Error Resolution**                  | Troubleshooting section to help resolve common issues during project setup                                          |

---

## 1. 🎥 CineSeek Demo

Discover how CineSeek works through a demo and local setup instructions. Follow the steps below to get started:

1. **Live Demo**: Try CineSeek hosted on a free cloud platform.
2. **Local Setup**: Run the project locally on your machine.
3. **Screenshots**: Check out how CineSeek looks and feels.

### Sample Screenshots:

- **Home Screen**  
  ![Home Screen](static/images/ss1.png)

- **Navigation Panel**  
  ![Navigation Panel](static/images/ss2.png)

- **Search with Suggestions**  
  ![Search Functionality](static/images/ss3.png)

- **Personalized Movie Recommendations**  
  ![Recommendations](static/images/ss4.png)

---

## 2. 📦 Requirements & Setup

Follow these steps to set up CineSeek on your system:

1. Create a virtual environment using Python (>=3.8, tested on 3.9.16).
2. Install all necessary dependencies from the `requirements.txt` file using the following command:

```shell
pip install -r requirements.txt
```
---

## 3. 🧠 Model Training & Customization

### Training Overview

For detailed instructions on training and using the movie recommendation model, refer to the provided Jupyter notebook. This guide walks you through the training process and inference steps.

### Django Web Integration

The project structure and setup for Django integration is explained in detail in the project guide.

---

## 4. 🌐 Deployment Guide

### Deploying on Cloud Platforms

A comprehensive guide is available for deploying CineSeek on cloud platforms like Heroku, AWS, or other PaaS services.

### Running Locally

Once you’ve installed the necessary dependencies, activate your virtual environment and start the local server:

```shell
/path/to/env/bin/activate
python manage.py runserver
```
Access the app at `http://localhost:8000` in your browser.

By default, the project uses a sample model. To switch to a different recommendation model:

1. Train and download the model of your choice.
2. Replace the following lines in `recommender/views.py`:

```python
Line 5 : movies_data = pd.read_parquet("static/<dataset_name>.parquet")
Line 73: model = pa.parquet.read_table('static/<model_name>.parquet').to_pandas()
```
Make sure the new dataset and model are placed in the `static` directory.

---

## Additional Information

CineSeek is a system with a user-friendly web interface built using web technology.

### Features
- **Search Suggestions**: Users can search for movies by typing partial or full movie names.
- **Personalized Recommendations**: Get movie suggestions based on user input data.
- **Visual Appeal**: The project uses custom styles and multimedia for a better user experience.

### Dependencies
- **CSS Files**: `cursor.css`, `page.css`, `navbar.css`
- **Assets**: `static/logo.png`, `static/production_ID_4779866.mp4`
- **Libraries**: jQuery, Bootstrap, Font Awesome, Tabler Icons

---

> **Note:** This is the first version of CineSeek. An upcoming update will include expanded datasets, better recommendations, and new features like collaborative filtering and content-based buckets. Stay tuned!

