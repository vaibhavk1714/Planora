# Planora ✈️

AI-powered travel itinerary planner built with Next.js, Gemini AI, Firebase Authentication, and Google Maps.

## Features

* Generate personalized travel itineraries using Gemini AI
* Interactive maps powered by Google Maps
* Firebase Authentication for user sign-in
* Modern UI built with Next.js and React
* Responsive design for desktop and mobile

---

## Tech Stack

* Next.js 15
* React 19
* TypeScript
* Firebase Authentication
* Google Gemini API
* Google Maps JavaScript API
* Tailwind CSS

---

## Prerequisites

Before running the project, create the following services:

### 1. Gemini API Key

1. Visit Google AI Studio.
2. Sign in with your Google account.
3. Create a new API key.
4. Save the key for later use.

### 2. Firebase Project

1. Create a Firebase project.
2. Enable Authentication.
3. Configure the desired sign-in provider (Google, Email/Password, etc.).
4. Create a Web App.
5. Copy the Firebase configuration values.

### 3. Google Maps API Key

1. Create or select a Google Cloud project.
2. Enable:

   * Maps JavaScript API
   * Places API
3. Create an API key.
4. Restrict the key appropriately for security.

---

## Environment Variables

Create a `.env.local` file in the project root:

```env
# Gemini
GEMINI_API_KEY=your_gemini_api_key
GOOGLE_API_KEY=your_gemini_api_key

# Firebase
NEXT_PUBLIC_FIREBASE_API_KEY=your_firebase_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id

# Google Maps
NEXT_PUBLIC_GOOGLE_MAPS_API_KEY=your_google_maps_api_key
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/vaibhavk1714/Planora.git
cd Planora
```

Install dependencies:

```bash
npm install
```

---

## Running the Application

Start the development server:

```bash
npm run dev
```

Open:

```text
http://localhost:3000
```

---

## Production Build

Build the application:

```bash
npm run build
```

Run the production server:

```bash
npm start
```

---

## Project Structure

```text
app/
├── api/             # API routes
├── login/           # Authentication pages
├── search/          # Trip search and planning
├── dashboard/       # User dashboard
└── trips/           # Saved trip details

components/
├── map/             # Google Maps components
└── ui/              # Reusable UI components

lib/
├── ai.ts            # Gemini integration
├── firebase.ts      # Firebase configuration
└── trips.ts         # Trip data management

types/               # Custom TypeScript types

```

---

## Common Issues

### Missing Gemini API Key

Error:

```text
Missing GOOGLE_API_KEY or GEMINI_API_KEY
```

Solution:

Verify that `.env.local` contains a valid Gemini API key.

### Firebase Authentication Error

Error:

```text
Firebase: Error (auth/configuration-not-found)
```

Solution:

* Ensure Firebase Authentication is enabled.
* Enable the required sign-in provider.
* Verify Firebase environment variables.

### Google Maps Not Loading

Verify:

```env
NEXT_PUBLIC_GOOGLE_MAPS_API_KEY=your_key
```

and ensure the Maps JavaScript API is enabled in Google Cloud.

---

## Security Notes

* Never commit `.env.local`.
* Restrict API keys where possible.
* Use separate keys for development and production environments.

---

## License

MIT 
