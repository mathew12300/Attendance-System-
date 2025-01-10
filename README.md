# Attendance-System-

## **Project Description**  

This project is a **Face Recognition Attendance System** built using Python and powered by a pre-trained model from **Google Teachable Machine**. It integrates **machine learning** and **computer vision** to detect and recognize faces in real-time using a webcam. The recognized faces are logged into a **MySQL database** to mark attendance automatically.  

The system provides an intuitive and efficient solution for managing attendance records, eliminating manual processes. With a user-friendly interface, it can be customized to detect specific individuals based on the trained model.  

---

## **Features**  
This face detection project is designed to efficiently recognize faces using a machine learning model trained on Google Teachable Machine. Key features include:  

1. **Face Recognition in Real-Time**:  
   - Detects and recognizes faces in real-time using a webcam feed.  

2. **Pre-Trained Model Integration**:  
   - Leverages a pre-trained TensorFlow model exported from Google Teachable Machine for accurate recognition.  

3. **Attendance Management**:  
   - Automatically records attendance in a MySQL database with a name and status.  

4. **Customizable and Scalable**:  
   - Easily add new classes for face detection by training a new model with Google Teachable Machine.  

5. **User-Friendly Interface**:  
   - Simple integration and visual feedback via webcam feed for detected faces and their confidence scores.  

6. **Efficient Cooldown Mechanism**:  
   - Avoids duplicate recognition within a specified timeframe for reliable attendance marking.  

---

## **Prerequisites**  
Before running this project, ensure you have the following:  

### **Software Requirements**  
1. **Python 3.7 or Higher**  
   - Make sure Python is installed and added to the system PATH.  

2. **Required Python Libraries**:  
   Install the dependencies using pip:  
   ```bash
   pip install opencv-python numpy mysql-connector-python tensorflow
   ```  

3. **MySQL Database**:  
   - Install MySQL Server by clicking the link (https://dev.mysql.com/downloads/installer/).
   -  and create a database named `attendance_system` with a table for storing attendance records.  

4. **Code Editor**:  
   - Use an IDE like PyCharm, VS Code, or any Python-supported editor.  

---

### **Hardware Requirements**  
1. **Webcam**:  
   - A functional webcam to capture images for real-time face recognition.  

2. **System Configuration**:  
   - Minimum 4GB RAM and a dual-core processor for smooth execution.  

---

### **Files Needed**  
1. **Pre-Trained Model Files**:  
   - `keras_model.h5` (trained model file).  
   - `labels.txt` (label file with class names).  

2. **Project Code**:  
   - Ensure the Python script is in the same directory as the model files.  

Here’s the step-by-step procedure for executing the attendance system project, formatted for inclusion in your **README.md** file:  

---

## **Execution Steps**  

### **Step 1: Set Up the Environment**  
1. Ensure Python 3.7 or higher is installed on your system.  
2. Install the required libraries by running the following command:  
   (Download the REQUIREMENT.TXT file and use this command)
   --pip install -r requirements.txt.
   -Run it. 
---

### **Step 2: Set Up the MySQL Database**  
1. Open your MySQL server and create a database named `attendance_system`.  
   ```sql
   CREATE DATABASE attendance_system;
   ```
2. Create a table to store attendance records:  
   ```sql
   USE attendance_system;

   CREATE TABLE attendance (
       id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(255) NOT NULL,
       status VARCHAR(50) NOT NULL
   );
   ```
3. Ensure you update the database connection details in the code (`host`, `user`, `password`) to match your MySQL setup.

---

Here’s an elaborated section for the **Google Teachable Machine** part, formatted for your **README.md** file:

---

### **Step 3: Train the Model Using Google Teachable Machine**  
The face detection system uses a pre-trained model from **Google Teachable Machine**, a user-friendly platform for creating machine learning models without prior coding experience. Follow these steps to train and download the model:  

#### **3.1: Access Google Teachable Machine**  
1. Open [Google Teachable Machine](https://teachablemachine.withgoogle.com/) in your web browser.  
2. Click **Get Started** to launch the platform.  

#### **3.2: Create a New Project**  
1. Under the **New Project** section, choose **Image Project**.  
2. Select the **Standard Image Model** option.  

#### **3.3: Upload Training Data**  
1. Define the number of **classes** (e.g., `Person A`, `Person B`, etc.) based on the faces you want to detect.  
2. For each class:
   - Use the webcam to capture images or upload images directly from your computer or Google Drive.  
   - Aim for 20–30 images per class to improve accuracy.  

#### **3.4: Train the Model**  
1. Click the **Train Model** button.  
2. Wait for the training process to complete.  
   - Once done, you’ll see a preview of the model's accuracy and class predictions.  

#### **3.5: Export the Model**  
1. Click the **Export Model** button.  
2. Under the **TensorFlow** tab, select **Download My Model**.  
3. A `.zip` file containing the following files will be downloaded:  
   - `keras_model.h5` (the trained model file).  
   - `labels.txt` (contains the class names).  

#### **3.6: Add the Model Files to Your Project**  
1. Extract the `.zip` file.  
2. Copy the `keras_model.h5` and `labels.txt` files into the project directory where your Python script resides.  



---

### **Step 4: Run the Script**  
1. Open the project directory in your terminal or Python IDE (e.g., PyCharm).  
2. Execute the script using the following command:  
   ```bash
   python your_script_name.py
   ```  

---

### **Step 5: Use the Webcam for Face Detection**  
1. Ensure your webcam is connected and functional.  
2. The system will capture images from the webcam, detect faces, and recognize them using the pre-trained model.  
3. If a face is recognized with a confidence score above 95%, it will mark the attendance in the MySQL database.  

---

### **Step 6: Exit the System**  
1. Press the **ESC** key to exit the program.  
2. The webcam feed will close, and the MySQL connection will terminate.  

---

### **Important Notes**  
- Ensure the `keras_model.h5` and `labels.txt` files are in the same directory as the script.  
- Confirm that the Python version and TensorFlow version are compatible with the model.  
- If you encounter errors, verify the MySQL connection details and required libraries.  

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests for enhancements or bug fixes.


## License
This project is licensed under the MIT License.


## Acknowledgments
- [Google Teachable Machine](https://teachablemachine.withgoogle.com/) for providing the pre-trained model.(RECOMMENDED).
