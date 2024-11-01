# Movie Recommender System

This project is a **Movie Recommender System** built with Streamlit, using cosine similarity to recommend movies based on a selected title. It leverages movie metadata and the OMDb API to fetch movie posters, providing an engaging, interactive experience for users to discover similar movies.

## Features

- **Movie Recommendation**: Based on a selected movie, the system provides recommendations for five similar movies.
- **Poster Display**: Movie posters are fetched using the OMDb API, offering a visual appeal.
- **Interactive Interface**: The application is deployed with Streamlit for a user-friendly, interactive experience.


## Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/movie-recommender-system.git
cd movie-recommender-system
```

### 2. Install required libraries

Install the necessary packages listed in the `requirements.txt` file:

```bash
pip install -r requirements.txt
```

### 3. Obtain OMDb API Key

1. Sign up at [OMDb API](http://www.omdbapi.com/apikey.aspx) to get an API key.
2. Replace `api_key=YOUR_API_KEY` in the `fetch_poster` function with your OMDb API key.

### 4. Run the Streamlit app

```bash
streamlit run app.py
```

## File Structure

- `app.py`: Main file containing the Streamlit app code.
- `movies.pkl`: A pickled file containing movie metadata.
- `similarity.pkl`: A pickled file with the precomputed similarity matrix.
- `requirements.txt`: Lists all required Python libraries for the project.

## Project Details

The application is built around content-based filtering:

- **Movie Metadata**: The system uses metadata about each movie to compute a similarity matrix using cosine similarity.
- **Recommendation Function**: The `recommend` function retrieves the top five similar movies for a selected movie.
- **Poster Fetching**: The `fetch_poster` function uses the OMDb API to fetch poster images for each recommended movie.

## Usage

1. **Select a Movie**: Choose a movie title from the dropdown menu.
2. **Show Recommendation**: Click on "Show Recommendation" to view five similar movie recommendations with posters.
3. **View Recommendations**: Recommended movies with their posters will be displayed in a 5-column layout.

## Example

Selecting "Inception" from the dropdown and clicking "Show Recommendation" will display five movies similar to "Inception," with their posters.

![image](https://github.com/user-attachments/assets/699619e3-33e8-4b78-9c69-62abfc8ebf01)

Selecting "Spider-Man 3" from the dropdown and clicking "Show Recommendation" will display five movies similar to "Inception," with their posters.

![image](https://github.com/user-attachments/assets/dab045b8-fcc2-4120-aab6-89020c685dbe)



## Future Improvements

- **Enhanced Recommendation Algorithm** : Experimenting with other recommendation algorithms for improved recommendations.
- **Expanded Movie Metadata**: Incorporating genres, actors, and directors to improve similarity calculations.
- **User Ratings Integration**: Allowing users to rate movies, potentially enhancing personalized recommendations.

