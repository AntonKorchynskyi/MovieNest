# MovieNest

**MovieNest** is an Android app for discovering and saving movies. Users search by title, browse details, and build a personal favorites list backed by Firebase.

## Key Features

- **User authentication**: Register and log in with email and password via Firebase Auth
- **Movie search**: Query the OMDB API by title and browse paginated results
- **Movie details**: View title, year, genres, IMDb rating, plot, and poster image
- **Favorites**: Save movies to a personal collection stored in Cloud Firestore
- **Favorites management**: Edit the description or delete any saved movie
- **Duplicate prevention**: Blocks adding a movie that is already in your favorites
- **Logout**: Securely sign out and return to the login screen

## Tech Stack

- **Language**: Java
- **Platform**: Android (minSdk 33, targetSdk 35)
- **Authentication**: Firebase Authentication
- **Database**: Cloud Firestore
- **Networking**: OkHttp3
- **Image loading**: Glide
- **API**: OMDB (Open Movie Database)
- **Architecture**: MVVM — ViewModel + LiveData

## Project Structure

```
com.example.movienest/
├── view/          # Activities and RecyclerView adapters
├── viewmodel/     # MovieViewModel, MovieDetailsViewModel
├── models/        # Movie data class
└── utils/         # ApiClient (OkHttp wrapper)
```

## Setup

1. Clone the repository
2. Add your `google-services.json` from the Firebase console to `app/`
3. Set your OMDB API key in `utils/ApiClient.java`
4. Open the project in Android Studio and run on a device or emulator
