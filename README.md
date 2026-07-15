--
         DYNAMIC TO-DO MATRIX
=================================
A premium productivity dashboard built for seamless task 
management, deep focus, and cloud synchronization.

Live Demo: https://your-vercel-link-here.app
Report Bug / Request Feature: https://github.com/yourusername/dynamic-todo/issues

---------------------------------------------------------
 FEATURES
---------------------------------------------------------
* Seamless Cloud Sync: Log in with Google via Firebase to sync your task matrices instantly across all devices.
* True Offline Mode: Auto-saves your progress to local storage when offline, ensuring you never lose a task.
* Dynamic Theme Engine: Switch between 4 premium color palettes (Default, Sakura Pink, Emerald Green, Midnight Indigo).
* Integrated Focus Room: A built-in, customizable Pomodoro timer combined with a classic YouTube Lofi stream for distraction-free work.
* AI-Powered JSON Import: Paste AI-generated task lists directly into the Command Center to instantly generate UI tiles.
* Notion-Style Editor: Edit tasks and categories on the fly using a clean, markdown-style syntax editor.

---------------------------------------------------------
 TECH STACK
---------------------------------------------------------
This project was built without heavy frameworks to ensure lightning-fast load times and pure frontend performance.

* Frontend: HTML5, CSS3 (Variables, Flexbox/Grid), Vanilla JavaScript
* Backend: Firebase v10 (Google OAuth Authentication, Cloud Firestore Database)
* Deployment: Optimized for Vercel / GitHub Pages

---------------------------------------------------------
 GETTING STARTED
---------------------------------------------------------
To run this project locally on your machine:

1. Clone the repository:
   git clone https://github.com/yourusername/dynamic-todo.git

2. Navigate into the directory:
   cd dynamic-todo

3. Configure Firebase:
   * Create a new project in the Firebase Console.
   * Enable Google Authentication and a Firestore Database.
   * Copy your Firebase config object and paste it into the firebaseConfig section inside index.html.

4. Run the App:
   Open index.html in your browser, or use a tool like VS Code's Live Server extension.

---------------------------------------------------------
 SECURITY NOTES
---------------------------------------------------------
If deploying to production, ensure your Firestore Security Rules are locked down so users can only read and write their own documents:

rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /users/{userId} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
  }
}

---------------------------------------------------------
-- Engineered by Unique
