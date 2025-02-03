# Music Recommender System

## Overview

The **Music Recommender System** is a Python-based web application that recommends songs based on a given input song. Built with **Streamlit**, **Spotipy**, and the **YouTube Data API**, this system retrieves song recommendations, displays album cover images, and provides direct YouTube links to listen to the songs. The system uses preprocessed music data and similarity scores to generate relevant song suggestions.

By leveraging the power of Spotify's API (via Spotipy), this system offers a rich and engaging user experience for music lovers seeking new songs to enjoy based on their current preferences.

## Features

- **Song Input**: Enter the name of a song, and the system will recommend five similar songs.
- **Album Covers**: For each recommendation, an album cover image is displayed.
- **YouTube Links**: Direct YouTube links are provided to easily listen to the recommended songs.
- **Preprocessed Data**: The system uses a dataset of over a million songs to make recommendations. It is preprocessed for efficiency and accurate song matching.

## Technologies Used

- **Streamlit**: A web application framework used to build and deploy the music recommender system.
- **Spotipy**: A Python library for the Spotify Web API, used to fetch song data, track features, and generate song recommendations based on similarity scores.
- **YouTube Data API**: Integrated to fetch YouTube links for the recommended songs so users can listen to them.
- **Pickle**: Used for loading preprocessed data (e.g., similarity scores, song metadata) for fast performance.
- **Pandas and Numpy**: Used for handling datasets and mathematical operations involved in song recommendation.
- **Matplotlib**: Used for rendering album covers and other data visualizations.

## Dataset

This project uses the **Spotify Million Song Dataset** which contains detailed metadata on over one million songs. The dataset includes song features such as:

- Track name
- Artist name
- Genre
- Album cover image
- Popularity and release year

The dataset is available for download from [Kaggle: Spotify Million Song Dataset](https://www.kaggle.com/datasets/notshrirang/spotify-million-song-dataset).

### Dataset Features:

- **Track ID**: Unique identifier for each track.
- **Track Name**: Name of the song.
- **Artist Name**: Artist or band performing the track.
- **Album**: Album name the track belongs to.
- **Genres**: Associated music genres.
- **Release Year**: Year the track was released.
- **Audio Features**: Including danceability, energy, valence, and more.
- **Popularity**: Popularity score from Spotify.

## Setup and Installation

To set up the Music Recommender System on your local machine, follow the steps below:

### Prerequisites

- **Python 3.6 or higher**: The project is built with Python and requires a Python 3.6+ environment.
- **Spotify Developer Account**: You will need a Spotify Developer Account to access the Spotify API. You can sign up [here](https://developer.spotify.com/dashboard/applications). Once registered, you will get a `CLIENT_ID` and `CLIENT_SECRET` that are required for authentication in Spotipy.

### Installation Steps

1. **Clone the Repository**:

    To clone the project repository to your local machine, run the following command:

    ```bash
    git clone https://github.com/your-username/music-recommender-system.git
    cd music-recommender-system
    ```

2. **Create a Virtual Environment** (optional but recommended):

    ```bash
    python3 -m venv env
    source env/bin/activate  # On Windows, use `env\Scripts\activate`
    ```

3. **Install Dependencies**:

    Install the necessary Python packages using pip:

    ```bash
    pip install -r requirements.txt
    ```

    `requirements.txt` should include:

    ```
    streamlit
    spotipy
    pickle-mixin
    pandas
    numpy
    matplotlib
    requests
    ```

4. **Configure Spotify API**:

    - Create a `.env` file or set environment variables to store your `CLIENT_ID` and `CLIENT_SECRET` securely.
    - You can get your credentials from [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/applications).

    Example `.env` file:

    ```bash
    CLIENT_ID=your_spotify_client_id
    CLIENT_SECRET=your_spotify_client_secret
    ```

5. **Run the Application**:

    After installing all dependencies and setting up your credentials, you can run the system locally using the following command:

    ```bash
    streamlit run app.py
    ```

    This will start a Streamlit app in your browser.

### Project Structure

- **app.py**: The main script that runs the Streamlit app. It handles user inputs, makes recommendations, and renders the interface.
- **utils.py**: Contains helper functions for Spotify API interaction, data processing, and recommendation logic.
- **model.pkl**: A pickle file containing the preprocessed music data and song similarity matrix (loaded for fast recommendations).
- **assets/**: Folder containing images, stylesheets, or other assets used in the app.
- **requirements.txt**: A list of all Python packages required to run the project.

## Contribution

Feel free to fork this repository and submit issues or pull requests. If you'd like to contribute to improving the system, here are a few ways you can help:

- **Improving Recommendation Logic**: Experiment with different recommendation algorithms such as collaborative filtering, content-based filtering, or hybrid approaches.
- **Enhancing UI**: Improve the user interface or add more features, like displaying song lyrics or artist biographies.
- **Optimizing Performance**: Work on making the recommendation engine faster or more scalable for larger datasets.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **Spotipy**: For providing an easy-to-use interface to the Spotify API.
- **YouTube Data API**: For enabling us to provide YouTube links for song playback.
- **Kaggle**: For providing the dataset used in this project.
