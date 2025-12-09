# Empower
ProtectPath – Real-Time Journey Safety Tracker

ProtectPath is a real-time location tracking system built using Firebase Realtime Database.
It allows a user to share their live journey link (viewer page) that updates automatically without refreshing, while the tracker page continuously pushes the user’s location to Firebase.

This system is designed for personal safety, emergency tracking, and secure journey monitoring.

🚀 Features

Live Location Tracking powered by Firebase

Two-page System:

tracker.html → Sends real-time GPS updates

viewer.html → Shows live movement on map

Start/End Journey Controls

WhatsApp Link Sharing (visible only after Start Journey)

Location auto-updates without refreshing

Journey link becomes inactive after End Journey

📁 Project Structure
ProtectPath/
│
├── tracker.html      # Sends location to Firebase
├── viewer.html       # Displays live location updates
├── README.md         # Project documentation
└── assets/           # (Optional) CSS/JS files

🔧 Technologies Used

HTML, CSS, JavaScript

Firebase Realtime Database

Google Maps JavaScript API

WhatsApp API (Deep Link)

Geolocation API

⚙️ How It Works

1️⃣ tracker.html

Requests GPS permission

Sends live coordinates (lat, lng, timestamp) to Firebase

Starts only when Start Journey is clicked

Shows “Send WhatsApp Link” button after journey starts

Stops updating when End Journey is clicked

2️⃣ viewer.html

Listens to the same Firebase path in real time

Automatically updates marker position

No need to refresh the page

Only works while journey is active

🗂️ Firebase Database Structure
{
  "journey": {
      "active": true,
      "lat": 11.3410,
      "lng": 77.7172,
      "timestamp": 1712492139
  }
}

▶️ How to Run
1. Clone the Repository
git clone https://github.com/your-username/ProtectPath.git

2. Add your Firebase config

Inside both tracker.html and viewer.html, update:

const firebaseConfig = {
   apiKey: "...",
   authDomain: "...",
   databaseURL: "...",
   projectId: "...",
   storageBucket: "...",
   messagingSenderId: "...",
   appId: "..."
};

3. Open tracker
Open tracker.html in your phone → Click Start Journey

4. Share Live Link

WhatsApp button appears

Send the viewer link to your contacts

5. Open viewer
viewer.html → Shows real-time moving location

📌 Future Improvements

Multi-user tracking

Journey history storage

Encryption for sensitive data

SOS audio/video upload

Mobile app version (Flutter / React Native)
