# SMS Spam Detection: Django Project

This project implements a machine learning model to classify SMS messages as spam or legitimate (ham). It uses **Django** to create a user-friendly web application for real-time spam detection. The model leverages **CountVectorizer** for text processing and a pre-trained classifier for spam detection.

![SMSSpamdetectionDjango](https://github.com/user-attachments/assets/b0467e94-76c0-4b58-b3ce-db55dc5f6d36)


## Features
- **Real-time SMS Spam Detection**: Enter a message and predict if it’s spam or ham.
- **Pre-trained Model**: Utilizes `CountVectorizer.pkl` and `spam_classifier.pkl` for quick predictions.
- **Django Web Application**: A robust and scalable web application interface.

## Project Structure

```bash
SMS-Spam-Detector-WebApp-master/
├── SMS_Spam_Detector/       # Django project settings & core files
│   ├── settings.py          # Django settings
│   └── urls.py              # URL routing for Django
├── spam_detector/           # Django app for spam detection
│   ├── templates/           # HTML templates for views
│   │   ├── index.html       # Main index page
│   │   ├── home.html        # Home page for spam detection input
│   │   ├── navbar.html      # Navbar component for navigation
│   ├── static/              # Static files (CSS, JS)
│   ├── views.py             # Handles predictions and rendering templates
│   └── forms.py             # Form to input SMS text
├── models/
│   ├── CountVectorizer.pkl  # Pre-trained vectorizer model
│   └── spam_classifier.pkl  # Pre-trained classifier model
├── manage.py                # Django project manager
├── requirements.txt         # Dependencies list
└── README.md                # Documentation file
```

## Installation
**1. Clone the repository**

```bash
git clone https://github.com/KZV027/SMS-Spam-Detector-WebApp.git
cd SMS-Spam-Detector-WebApp 
```

**2. Set up a virtual environment (recommended)**

```bash
python -m venv venv
source venv/bin/activate  # For Windows: venv\Scripts\activate

```

**3. Install dependencies**
```bash
pip install -r requirements.txt

```

**4. Set up Django project**
Run the following commands to apply migrations and start the server:

```bash
python manage.py migrate
python manage.py runserver

```

**5. Access the web app** 

Open your web browser and go to ```bash http://127.0.0.1:8000/ ``` to use the app.

## Usage

1. **Navigate to the Web App**: Go to the app’s homepage.
2. **Enter SMS Text**: Input the SMS message you want to classify.
3. **Prediction**: The app will display if the message is spam or ham and the confidence level.

## Template Details

- **`index.html`**: The main landing page for the application.
- **`home.html`**: The page where users can input SMS messages and get predictions.
- **`navbar.html`**: A reusable navigation bar included in all pages.

## Model Details

- **`CountVectorizer.pkl`**: Used for converting SMS messages into numerical features.
- **`spam_classifier.pkl`**: Pre-trained model that classifies SMS as spam or ham.

## Further Development

- **Text Preprocessing**: Add more preprocessing steps like removing stop words.
- **Model Enhancements**: Experiment with advanced models such as LSTMs.
- **Integration**: Extend to support messaging platforms for real-time spam detection.

## Contributing

Feel free to contribute by creating issues, submitting pull requests, or enhancing the project documentation.

## License

This project is licensed under the MIT License.
