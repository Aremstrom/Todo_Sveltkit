# 📝 SvelteKit Firebase ToDo List

This ToDo List project is built using SvelteKit framework for the frontend and Firebase for authentication and database management. With features like user authentication, adding tasks, marking them as completed, and deleting them, this application provides a seamless experience for managing your daily tasks.

## Features

- **🔐 User Authentication:** Users can sign up and log in securely using Firebase Authentication.
- **✅ Task Management:** Add new tasks, mark them as completed, or delete them as needed.
- **🔄 Real-time Updates:** Tasks are synchronized in real-time across all logged-in devices thanks to Firebase Realtime Database.
- **📱 Responsive Design:** The application is designed to work seamlessly across various screen sizes, making it accessible from desktops, tablets, and mobile devices.

## Usage

To use this project locally, follow these steps:

1. Clone this repository to your local machine.
   ```bash
   git clone https://github.com/Aremstrom/Todo_Sveltkit.git
   ```

2. Install dependencies using npm or yarn.
   ```bash
   cd todo-list
   npm install # or yarn
   ```

3. **Obtaining Firebase Configuration**

   To set up Firebase Authentication and Database services for this project, you need to create a Firebase project and obtain your Firebase configuration.

   ### Steps to Obtain Firebase Configuration:

   1. **Create a Firebase Project:**
      - Go to the [Firebase Console](https://console.firebase.google.com/).
      - Click on "Add project" and follow the on-screen instructions to create a new Firebase project.
   
   2. **Enable Authentication:**
      - In the Firebase Console, navigate to the "Authentication" section.
      - Enable the authentication methods you want to use (e.g., Email/Password, Google Sign-In, etc.).
   
   3. **Enable Firestore Database:**
      - In the Firebase Console, navigate to the "Firestore Database" section.
      - Click on "Create database" and choose the appropriate location and mode for your database.
   
   4. **Obtain Firebase Configuration:**
      - In the Firebase Console, go to the project settings.
      - Scroll down to the "Your apps" section and click on the "Web" icon (</>).
      - Register your app by providing a nickname (e.g., "ToDoListApp").
      - Copy the Firebase configuration object provided (it should look like a JavaScript object).

   ### Setting up Environment Variables:

   Once you have obtained your Firebase configuration, you need to set up environment variables in your SvelteKit project to securely store this information.

   1. **Create a `.env` File:**
      - In the root directory of your project, create a new file named `.env`.

   2. **Add Firebase Configuration as Environment Variables:**
      - Open the `.env` file in a text editor.
      - Add the following environment variables, replacing the placeholders with your Firebase configuration values:
        ```plaintext
        VITE_FIREBASE_API_KEY=your_api_key
        VITE_FIREBASE_AUTH_DOMAIN=your_auth_domain
        VITE_FIREBASE_PROJECT_ID=your_project_id
        VITE_FIREBASE_STORAGE_BUCKET=your_storage_bucket
        VITE_FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id
        VITE_FIREBASE_APP_ID=your_app_id
        ```

   ### Example Firebase Configuration:

   Here's an example of how your Firebase configuration might look:

   ```javascript
   const firebaseConfig = {
     apiKey: "YOUR_API_KEY",
     authDomain: "YOUR_AUTH_DOMAIN",
     projectId: "YOUR_PROJECT_ID",
     storageBucket: "YOUR_STORAGE_BUCKET",
     messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
     appId: "YOUR_APP_ID"
   };
   ```

   Replace `"YOUR_API_KEY"`, `"YOUR_AUTH_DOMAIN"`, etc., with the actual values obtained from your Firebase project.

4. Start the development server.
   ```bash
   npm run dev # or yarn dev
   ```

5. Open your browser and navigate to `http://localhost:5173` to view the application.

## Credits

This project was inspired by the tutorial series on [Smoljames](https://www.youtube.com/watch?v=TIbL0VOE900)🙌🫡 and was built with SvelteKit and Firebase.
