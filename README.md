# **Spotify-to-YouTube Playlist Manager**

This project bridges Spotify and YouTube, enabling users to extract Spotify playlists and manage them with features like video matching or downloading using the YouTube API and `yt_dlp`.

---

## **Features**
- **Spotify Playlist Integration**: Extract and process playlists from Spotify.
- **YouTube Matching**: Find YouTube videos corresponding to Spotify tracks.
- **Download Tracks**: Leverage `yt_dlp` to download matched YouTube videos.
- **GUI Interface**: A simple PyQt5-based interface for user interaction.

---

## **Setup Instructions**

### **Prerequisites**
Ensure you have the following installed:
- Python 3.7+
- Spotify Developer Account with API credentials.
- YouTube API key.
- Required Python libraries.

### **Install Dependencies**
Run the following command to install dependencies:
```bash
pip install spotipy google-api-python-client yt-dlp PyQt5
```

---

## **How to Run**

1. **Set Up Spotify and YouTube API Credentials**:
   - **Spotify**: Create an app at the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/applications) and obtain:
     - `SPOTIPY_CLIENT_ID`
     - `SPOTIPY_CLIENT_SECRET`
     - `SPOTIPY_REDIRECT_URI`
   - **YouTube**: Obtain an API key from the [Google Cloud Console](https://console.cloud.google.com/).

2. **Configure Credentials**:
   - Edit the `main.py` file to include your API credentials:
     ```python
     SPOTIPY_CLIENT_ID = 'your-client-id'
     SPOTIPY_CLIENT_SECRET = 'your-client-secret'
     SPOTIPY_REDIRECT_URI = 'http://localhost:8888/callback'
     YOUTUBE_API_KEY = 'your-youtube-api-key'
     ```

3. **Run the Application**:
   - Start the program:
     ```bash
     python main.py
     ```
   - Interact with the GUI to input Spotify playlist links and manage the corresponding YouTube videos.

---

## **Key Components**

- **Spotify Integration**:
  - Authenticates with Spotify to access playlist data.
  - Extracts track metadata from playlists.

- **YouTube Matching**:
  - Searches for tracks on YouTube using the YouTube API.
  - Matches and displays video links for playlist tracks.

- **Downloading**:
  - Uses `yt_dlp` to download YouTube videos for offline use.

- **GUI**:
  - A PyQt5-based interface for ease of use.

---

## **Future Enhancements**
- Add support for multiple playlist formats.
- Improve matching accuracy between Spotify and YouTube tracks.
- Allow batch downloads and error handling for unavailable content.

---

## **Acknowledgments**
- **Spotify API**: For playlist and track data.
- **YouTube API**: For video searching and metadata.
- **yt-dlp**: For reliable YouTube video downloads.

---

