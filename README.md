## 📱 Flutter App

### Features:
- Sliders to control three motors.
- Save pose (motor positions) to the database.
- View saved poses.
- Send commands to run or reset poses.

### Requirements:
- Flutter SDK
- Internet permission in AndroidManifest.xml
- http package added to pubspec.yaml

### Important File:
- main.dart contains the UI and logic to save poses.

---

## 🛢️ Database

### Table: poses
CREATE TABLE poses (
  id INT AUTO_INCREMENT PRIMARY KEY,
  motor1 INT,
  motor2 INT,
  motor3 INT,
  status INT DEFAULT 0
);

---
## 🌐 PHP Backend Files

- save_pose.php: Saves new motor values into the database.
- get_run_pose.php: Retrieves the latest pose with status = 1.
- update_status.php: Resets the pose status to 0 after execution.

### PHP Configuration:
Make sure to set your database credentials properly:$host = "localhost";
$user = "root";
$pass = "";
$db = "robot_arm";

---
## 🗂️ Project Structure
robot_arm_project/
├── flutter_app/
│   └── main.dart
├── php_files/
│   ├── save_pose.php
│   ├── get_run_pose.php
│   └── update_status.php
└── database/
    └── robot_arm.sql
    
---
## 📤 Deployment

1. Upload the PHP files to a server (e.g., XAMPP/Apache).
2. Create the database using robot_arm.sql.
3. Run the Flutter app on an emulator or real device.
4. Ensure device and server are on the same network or use a hosted API endpoint.
---

## 🛠️ Developed for: Educational and Robotics control projects.


![Image](https://github.com/user-attachments/assets/cfc07fb4-754d-4aab-8b72-fab86134eb2f)
