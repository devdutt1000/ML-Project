# 🎓 Student Performance Predictor

An end-to-end machine learning project that predicts student math scores based on various demographic and academic factors. Built with Flask and scikit-learn, featuring a modern, responsive web interface.

## 📋 Overview

This project demonstrates a complete machine learning workflow from data analysis to model deployment. The application uses multiple regression algorithms to predict student performance in mathematics based on factors such as gender, ethnicity, parental education level, lunch type, test preparation course, and scores in reading and writing.

## ✨ Features

- **🤖 ML-Powered Predictions**: Uses trained machine learning models for accurate score predictions
- **📊 Data-Driven Insights**: Based on comprehensive student performance datasets
- **⚡ Fast Results**: Real-time predictions with optimized model loading
- **🎯 High Accuracy**: Multiple regression techniques for reliable predictions
- **💻 Modern UI**: Beautiful, responsive frontend with gradient designs and animations
- **📱 Mobile Responsive**: Works seamlessly on all device sizes
- **🎨 Professional Design**: Clean interface with smooth transitions and intuitive forms

## 🛠️ Tech Stack

### Backend
- **Python 3.9+**
- **Flask** - Web framework
- **scikit-learn** - Machine learning library
- **pandas** - Data manipulation
- **numpy** - Numerical computing
- **dill** - Model serialization

### Frontend
- **HTML5/CSS3**
- **Modern CSS** (Flexbox, Grid, Animations)
- **Google Fonts** (Inter)
- **Responsive Design**

### ML Algorithms
- Linear Regression
- StandardScaler for feature scaling
- Pipeline for streamlined preprocessing
- ColumnTransformer for handling mixed data types

## 📦 Installation

1. **Clone the repository**
   ```bash
   cd ML-Project
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Usage

1. **Start the Flask application**
   ```bash
   python application.py
   ```

2. **Open your browser**
   Navigate to `http://localhost:5000`

3. **Make predictions**
   - Fill in the student information form
   - Enter reading and writing scores
   - Click "Predict Math Score"
   - View the predicted math score instantly

## 📁 Project Structure

```
ML-Project/
├── application.py          # Flask application entry point
├── requirements.txt        # Python dependencies
├── setup.py               # Package setup configuration
├── README.md              # Project documentation
├── artifacts/             # Data and model artifacts
│   ├── data.csv          # Original dataset
│   ├── train.csv         # Training data
│   └── test.csv          # Testing data
├── notebook/              # Jupyter notebooks
│   ├── 1. EDA STUDENT PERFORMANCE.ipynb
│   └── 2. MODEL TRAINING.ipynb
├── src/                   # Source code
│   ├── __init__.py
│   ├── exception.py       # Custom exception handling
│   ├── logger.py          # Logging configuration
│   ├── utils.py           # Utility functions
│   ├── components/        # ML pipeline components
│   └── pipeline/          # Prediction pipeline
└── templates/             # HTML templates
    ├── index.html         # Landing page
    └── home.html          # Prediction form page
```

## 🎯 Model Features

The model takes the following inputs:

| Feature | Type | Options |
|---------|------|---------|
| Gender | Categorical | Male, Female |
| Race/Ethnicity | Categorical | Group A, B, C, D, E |
| Parental Education | Categorical | High school, Some high school, Some college, Associate's degree, Bachelor's degree, Master's degree |
| Lunch Type | Categorical | Standard, Free/Reduced |
| Test Prep Course | Categorical | None, Completed |
| Reading Score | Numerical | 0-100 |
| Writing Score | Numerical | 0-100 |

**Output**: Predicted Math Score (0-100)

## 🎨 UI Features

- **Landing Page**: Modern gradient design with feature cards and animated elements
- **Prediction Form**: Clean, intuitive form with custom-styled inputs and dropdowns
- **Result Display**: Beautiful result card showing the predicted score
- **Animations**: Smooth fade-in effects, hover transitions, and floating elements
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices

## 📊 Model Performance

The model has been trained and evaluated on student performance data with the following characteristics:
- Multiple regression algorithms tested
- Feature engineering and scaling applied
- Cross-validation for robust performance
- Optimized hyperparameters

## 🔧 Development

### Running in Debug Mode
```bash
export FLASK_ENV=development  # On Windows: set FLASK_ENV=development
python application.py
```

### Training the Model
Refer to the Jupyter notebooks in the `notebook/` directory:
1. `1. EDA STUDENT PERFORMANCE.ipynb` - Exploratory Data Analysis
2. `2. MODEL TRAINING.ipynb` - Model training and evaluation

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

Built with ❤️ as an end-to-end machine learning demonstration project.

## 🙏 Acknowledgments

- Dataset sourced from student performance studies
- Inspired by real-world educational data analysis needs
- Built with modern web design principles

---

**Note**: This is an educational project demonstrating ML deployment. The predictions should be used for educational purposes only.