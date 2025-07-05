📸 Face Recognition Employee Dashboard

This project is a Face Recognition-Based Employee Login & Dashboard System built using AWS cloud services and  JavaScript frontend. It enables employee registration and authentication through facial recognition, then redirects them to a secure dashboard showing their details.

🌐 Live Demo [ https://facial-reck.vercel.app/FaceLogin.html ]

⚙️ Features

🔐 Secure login using face recognition

🧑‍💼 Employee registration with camera capture

📊 Personalized employee dashboard

🕒 Auto session tracking with timeout

☁️ Built with serverless AWS services

🧠 Confidence score and login history

📋 How It Works
🧍 Employee Registration (Register.html)
User fills in name, email, employee ID, and department.

Camera is opened to capture a face image.

On submit, the data is sent to the AWS Lambda function via API Gateway.

Lambda stores the image in S3 and metadata in DynamoDB.

On success, the user is auto-logged in and redirected to the Dashboard.

😎 Employee Login (FaceLogin.html)
Opens the camera and captures a face image.

Sends the captured face to a Login Lambda API.

Lambda fetches the stored image from S3, compares it using Amazon Rekognition.

If matched, returns employee details → redirects to Dashboard.

📊 Dashboard (Dashboard.html)
Displays employee name, ID, department, login time, confidence score, and session status.

Auto logout after 30 mins of inactivity.

Uses sessionStorage to validate active sessions.


