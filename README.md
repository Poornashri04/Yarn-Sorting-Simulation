**Yarn Color Classifier with Servo-Based Sorting (AI + Arduino Simulation)**
This project is a smart yarn color sorting system that uses Artificial Intelligence (AI) to detect the color of yarn from images and then physically simulates the sorting process using a servo motor controlled by an Arduino.

The system uses a Convolutional Neural Network (CNN) trained to classify yarn colors — specifically red, green, and blue. A web interface allows users to upload yarn images. Once an image is uploaded, the AI model predicts the color and the result is:
Stored in a MySQL database
Displayed on a web dashboard
Sent to an Arduino via serial communication, which moves a servo motor to sort the yarn into the correct bin based on color
This simulates a real-world automated sorting system found in textile industries.

**Key Features**
Upload yarn image via browser
Predict yarn color using a CNN model trained on custom dataset
Live statistics chart showing how many yarns of each color have been detected
History page with image, label, and timestamp
Sends the result to Arduino (or Proteus simulation)
Moves servo motor to a specific angle (0°, 90°, 180°) based on the predicted color

**Technologies Used**
Layer	Technology
Frontend	HTML, CSS, JavaScript (Chart.js)
Backend	Python (FastAPI), TensorFlow/Keras
Database	MySQL
Hardware	Arduino UNO + Servo Motor
Simulation	Proteus 8 Professional (optional)

**How the Servo Logic Works**
Red yarn → Servo moves to 0° (e.g., drops into Red bin)
Green yarn → Servo moves to 90°
Blue yarn → Servo moves to 180°

Each time a yarn is uploaded and classified, the backend sends "red", "green", or "blue" via serial to Arduino. Arduino then rotates the servo motor accordingly.

**Project Structure**
project/
├── main.py              
├── train_model.py         
├── cnn_model/
│   └── yarn_color_classifier.h5
├── uploads/               
├── dataset/               
├── templates/
│   ├── index.html
│   └── history.html
├── static/
│   ├── style.css
│   └── script.js

**Industrial Application**
This project simulates how textile industries can automate yarn classification and sorting to:
Save labor time
Reduce sorting errors
Improve production speed and quality
It can later be extended to detect defects, contamination, or yarn type.

**Developer Info**
Poorna Shri
B.Sc. Computer Science
Sri Krishna Arts and Science College

