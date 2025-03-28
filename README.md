News & User Profile App

📌 Overview

This is a modern News & User Profile App that provides an immersive news reading experience along with user authentication and profile management. The app is built using the latest Android technologies and follows MVVM architecture for maintainability and scalability.

✨ Features

1. Splash Screen with Video

Displays a video splash screen (.mp4 file).

Navigation logic:

✅ If the user is logged in, navigate to HomeFragment.

✅ If not logged in, navigate to the Login Screen.

2. Google Sign-In Authentication

Implements Google Sign-In using Firebase Authentication.

Fetches and stores user profile details:

✅ Name

✅ Email

✅ Profile Picture

Navigates to the Home Screen after login.

3. Bottom Navigation with 3 Fragments

✅ HomeFragment

Displays news articles in full-screen mode (like Inshorts, one news per screen).

Allows swipe up/down to navigate to the next/previous news item.

Fetches latest news articles using:

Retrofit + Paging 3 (for efficient data loading).

Shows profile image (top-right corner) (from Google or locally updated).

✅ SearchFragment

Displays multiple news articles in a grid/list format.

Implements search functionality for news.

✅ ProfileFragment

Displays Google profile details (Name, Email, Profile Picture).

Shows current location (Latitude & Longitude) using Fused Location Provider API.

Allows profile picture update from Camera & Gallery.

4. Profile Picture Update (Camera & Gallery)

Users can update profile pictures from:

✅ Camera (Capture and set profile picture).

✅ Gallery (Pick and update profile picture).

Properly handles permissions:

⛔ Deny All Permissions → Shows an alert dialog explaining why the permission is needed.

🚫 Allow Limited Access → Allows selection but disables camera capture.

✅ Allow Once → Works normally for that session.

Updates profile picture in:

HomeFragment (top-right avatar).

ProfileFragment (profile section).

Stores the selected image locally using Room Database / SharedPreferences.

5. Advanced Functionalities

✅ Swipe to Refresh (Pull to refresh the news list).

✅ Swipe Gestures in RecyclerView:

Left swipe to delete a news item.

Right swipe to open news details.

✅ Offline Caching (Cache API data in Room Database for offline access).

✅ Dark Mode Support (Automatically switches themes based on system settings).

✅ Shimmer Effect (Loading animation while fetching news).

6. Background Tasks & WorkManager

Uses WorkManager to refresh news every 30 minutes in the background.

7. Navigation & Animations

✅ Fragment Transitions for smooth navigation.

✅ Shared Element Transition (News list → News details).

✅ Swipe-based Navigation in HomeFragment (like Inshorts for full-screen browsing experience).

🚀 Tech Stack

MVVM Architecture

Hilt (Dependency Injection)

Retrofit + OkHttp (API Calls)

Room Database (Offline caching)

WorkManager (Background tasks)

ViewBinding (Efficient UI handling)

Glide (Image loading)

Fused Location Provider API (Location access)

Firebase Authentication (Google Sign-In)

ViewPager (Navigation)

🛠️ Project Setup Instructions

Clone the repository:

git clone https://github.com/yourusername/news-app.git
cd news-app

Open the project in Android Studio.

Sync Gradle files (File > Sync Project with Gradle Files).

Obtain an API key from NewsAPI and update local.properties:

NEWS_API_KEY=your_api_key_here

Run the app on an emulator or a real device.

🔑 API Key Setup

Register at NewsAPI to get an API Key.

Add the API Key in local.properties:

NEWS_API_KEY=your_api_key_here

Update gradle.properties:

NEWS_API_KEY=${NEWS_API_KEY}

📦 Dependencies Used

All dependencies are managed in libs.versions.toml.

📂 Submission Requirements

✅ Push the code to GitHub and share the repository link.

✅ Include this README.md with:

Project setup instructions

API key setup

Dependencies used

✅ Export the APK file and share it for testing.

✅ Record a short demo video showcasing the app's features and functionality.

🎉 Happy Coding! 🚀
