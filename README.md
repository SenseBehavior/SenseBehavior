---
title: SenseBehavior
emoji: 🚀
colorFrom: purple
colorTo: indigo
sdk: docker
pinned: false
license: other
---

# 🚀 SenseBehavior - Human Behavior Classification

A comprehensive Flask-based web application that uses LSTM neural networks to classify human behavior patterns from sensor data with advanced analytics and visualization capabilities.

## 🎯 Features

### 🔹 Model Interaction
- **Load pre-trained LSTM model** (.pth file)
- **Predict behavior with confidence scores**
- **Test predictions on samples from training data**
- **Real-time model evaluation**

### 🔹 Data Input & Validation
- **Upload CSV files** with sensor time-series data
- **Validate CSV structure** and format automatically
- **Drag-and-drop interface** for easy file upload
- **Multiple file format support**

### 🔹 Exploratory Data Analysis
- **Interactive data visualizations** with matplotlib
- **Live plotting** of individual or multiple sensor axes
- **Compare different sensor channels** side-by-side
- **Data preview and statistics**

### 🔹 Model Evaluation
- **Confusion matrix visualization**
- **Overall and per-class accuracy metrics**
- **Classification report** (Precision, Recall, F1-score)
- **Model performance analytics**

### 🔹 Visualization Tools
- **Interactive sensor data plots**
- **Confusion matrix heatmaps**
- **Real-time data visualization**
- **Multiple plot types** (line, scatter, histogram)

### 🔹 Output & Export
- **Download prediction results** as CSV
- **Export model evaluation metrics**
- **Save visualizations** and reports
- **Comprehensive data export**

### 🔹 User Interface
- **Dark/light theme toggle**
- **Tabbed interface** for organized navigation
- **Interactive sliders, checkboxes, and file uploaders**
- **Responsive design** for all devices

### 🔹 Configuration Options
- **Adjustable model architecture** (input_size, hidden_size, etc.)
- **Editable label encoder class mappings**
- **Real-time configuration updates**
- **System information display**

## 🧠 Supported Behaviors

The application can classify the following human behaviors:

- **🚶‍♂️ Walking** - Movement patterns while walking
- **🪑 Sitting** - Stationary sitting behavior
- **🚗 Driving** - Vehicle operation patterns
- **🧍‍♂️ Standing** - Upright stationary behavior

## 📊 How It Works

1. **Upload Sensor Data**: Drag and drop a CSV file containing sensor data
2. **Data Analysis**: The system automatically analyzes your data structure and creates visualizations
3. **LSTM Prediction**: Our trained neural network processes the sensor data
4. **Results Display**: View behavior predictions with confidence scores and detailed analytics
5. **Model Evaluation**: Evaluate model performance on training data
6. **Export Results**: Download predictions and evaluation metrics

## 🛠️ Technical Details

- **Framework**: Flask web application with RESTful API
- **ML Model**: LSTM (Long Short-Term Memory) neural network
- **Input**: CSV files with sensor data (accelerometer, gyroscope, etc.)
- **Output**: Behavior classification with confidence scores and detailed metrics
- **Model Architecture**: 332 input features → 128 LSTM units → 4 output classes
- **Visualization**: Matplotlib and Seaborn for interactive plots
- **Evaluation**: Scikit-learn metrics and confusion matrix analysis

## 📁 Data Format

Your CSV file should contain sensor data with the following characteristics:
- **Numeric columns**: Sensor readings (acc_x, acc_y, acc_z, gyro_x, etc.)
- **Time series data**: Sequential sensor measurements
- **332 features**: The model expects 332 input features
- **Optional**: sequence_id and behavior columns for evaluation

## 🚀 Usage

### Web Interface
1. **Access the Application**: Visit the Hugging Face Space URL
2. **Upload Data**: Click "Choose File" or drag-and-drop a CSV file
3. **View Results**: See behavior predictions with confidence scores
4. **Explore Data**: Use the visualization tools to analyze sensor data
5. **Evaluate Model**: Run model evaluation on training data
6. **Export Results**: Download predictions and evaluation metrics

### API Endpoints
- `GET /` - Main application interface
- `POST /upload` - Upload and process CSV files
- `GET /evaluate` - Evaluate model performance
- `POST /test_sample` - Test model on random sample
- `POST /download_results` - Download prediction results
- `GET/POST /config` - Get/update model configuration
- `GET /health` - Health check endpoint

## 🔧 Development

### Local Setup

```bash
# Clone the repository
git clone <repository-url>
cd SenseBehavior

# Install dependencies
pip install -r requirements.txt

# Run the application (with cache)
python app.py

# Run the application (without cache)
python run_no_cache.py
```

### Docker Setup

```bash
# Build the Docker image
docker build -t sensebehavior .

# Run the container
docker run -p 7860:7860 sensebehavior
```

## 📋 Requirements

- Python 3.11+
- Flask 2.3.3
- PyTorch 2.0.1
- Pandas 2.0.3
- Scikit-learn 1.3.0
- NumPy 1.24.3
- Matplotlib 3.7.2
- Seaborn 0.12.2

## 🎓 Academic Project

This project was developed for **CIS6005 — Computational Intelligence Project (2025)**.

## 📝 License

This project is licensed under the MIT License.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Support

If you encounter any issues or have questions, please open an issue in the repository.

---

**Developed with ❤️ for Human Behavior Analysis**
