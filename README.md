ArtVision - Interactive Art Gallery with Firebase

 📋 Project Overview
ArtVision is a fully functional, responsive web application that serves as an interactive art gallery with Firebase backend integration. This single-page application allows users to browse artworks, while authenticated users can add new artworks through an admin panel.

 🚀 Features

Core Features
- Responsive Gallery Display: Grid-based layout showcasing artworks with hover effects
- Firebase Backend: Real-time data storage using Firestore database
- User Authentication: Secure login/signup system with Firebase Auth
- Dynamic Filtering: Filter artworks by category (Paintings, Sculptures, Digital Art, Photography)
- Search Functionality: Real-time search across artwork titles, artists, and mediums
- Admin Panel: Authenticated users can add new artworks
- Mobile-Friendly: Fully responsive design with mobile menu

Technical Features
- Single HTML File: All code (HTML, CSS, JavaScript) in one file for easy deployment
- Firebase Integration: Uses Firestore for data storage and Firebase Auth for authentication
- Modern UI/UX: Clean design with CSS custom properties and smooth transitions
- Error Handling: Comprehensive error messages and loading states
- Form Validation: Client-side validation for all forms

🛠️ Technologies Used
- Frontend: HTML5, CSS3, Vanilla JavaScript
- Backend: Firebase (Firestore, Authentication)
- Icons: Font Awesome 6.4.0
- Images: Unsplash (for sample images)
- Fonts: Google Fonts (Segoe UI system font stack)

 📁 File Structure
```
ArtVision/
├── index.html                    # Main HTML file (all code in one file)
├── (No external CSS/JS files - all included in HTML)
```

 🔧 Setup Instructions

1. Firebase Setup
1. Create a Firebase project at [Firebase Console](https://console.firebase.google.com/)
2. Enable Firestore Database (start in test mode for development)
3. Enable Authentication with Email/Password provider
4. Get your Firebase configuration from Project Settings

2. Configuration
Replace the Firebase configuration in the script section with your own:

```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_PROJECT_ID.appspot.com",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID"
};
```

3. Initial Data Setup (Optional)
Uncomment the `addSampleArtworks()` function call in the script to populate your Firestore database with sample artworks.

🎨 Design System

Color Palette
- `--primary`: #2c3e50 (Dark Blue)
- `--secondary`: #3498db (Bright Blue)
- `--accent`: #e74c3c (Red)
- `--light`: #ecf0f1 (Light Gray)
- `--dark`: #1a252f (Almost Black)
- `--success`: #2ecc71 (Green)

Typography
- Primary font: Segoe UI system font stack
- Responsive typography with appropriate scaling

 📱 Responsive Breakpoints
- Desktop: 1200px max-width container
- Tablet: 768px and below
- Mobile: Responsive grid and mobile menu

 🔐 Security Considerations
- Firestore Rules: Configure appropriate security rules in Firebase Console
- Admin Access: Currently checks for specific email (`admin@artvision.com`)
- Password Requirements: Minimum 6 characters for user registration

 🧪 Key Functions

Data Management
- `loadArtworks()`: Fetches artworks from Firestore
- `addArtwork()`: Adds new artwork to Firestore
- `filterArtworks()`: Filters by category
- `searchArtworks()`: Implements search functionality

Authentication
- `auth.onAuthStateChanged()`: Monitors authentication state
- `signInWithEmailAndPassword()`: User login
- `createUserWithEmailAndPassword()`: User registration

UI Functions
- `renderGallery()`: Dynamically renders artworks
- `showSuccess()`: Displays success/error messages
- `switchAuthTab()`: Toggles between login/signup tabs

 🚀 Deployment

Local Deployment
1. Simply open `index.html` in any modern web browser
2. Configure Firebase as described above

Web Hosting Options
- Firebase Hosting: Perfect for this project
- Netlify: Easy static site hosting
- GitHub Pages: Free hosting for open source projects

Firebase Hosting Steps
```bash
 Install Firebase CLI
npm install -g firebase-tools

 Login to Firebase
firebase login

 Initialize project
firebase init

 Deploy
firebase deploy
```

📈 Future Enhancements
- [Artwork Editing: Allow editing/deleting existing artworks
- User Profiles: User-specific galleries and favorites
- Shopping Cart: E-commerce functionality for purchasing artworks
- Image Upload: Direct image upload instead of URL input
- Pagination: Load more artworks on scroll
- Social Sharing: Share artworks on social media
- Comments/Ratings: User interaction with artwor
