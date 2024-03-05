# Movie Rating App
This is a simple movie rating app built using React. It allows users to search for movies, view movie details, and add movies to a watched list with user ratings.

## Features
- Search for movies by title
- View movie details including title, release year, poster, runtime, IMDb rating, plot, actors, and director
- Add movies to a watched list
- Rate movies on a scale of 1 to 10
- View average user ratings for watched movies
- Remove movies from the watched list
- 
## Technologies Used
- React
- JavaScript (ES6)
- HTML
- CSS
- OMDB API (for movie data)
- 
## How to Use
1. Clone the repository to your local machine.
2. Run npm install to install dependencies.
3. Run npm start to start the development server.
4. Open your web browser and navigate to http://localhost:3000/ to view the app.
   
## How it Works
#### The app consists of several components:

**Main:** The main component that wraps the app and provides the children prop to its child components.
**MovieList:** A component that displays a list of movies. It takes in a movies prop, which is an array of movie objects, and an onSelectMovie callback function.
**Movie:** A component that displays a single movie. It takes in a movie prop, which is a movie object, and an onSelectMovie callback function.
**MovieDetails:** A component that displays movie details and allows the user to rate the movie and add it to the watched list. It takes in several props, including the selectedId of the movie, a watched array of watched movies, and callback functions for closing the details modal and adding a movie to the watched list.
**WatchedSummary:** A component that displays a summary of the watched movies, including the number of movies, average IMDb rating, average user rating, and average runtime.
**WatchedMovieList:** A component that displays a list of watched movies. It takes in a watched array of watched movies and a onDeleteWatched callback function for removing movies from the watched list.
**WatchedMovie:** A component that displays a single watched movie. It takes in a movie prop, which is a watched movie object, and an onDeleteWatched callback function for removing the movie from the watched list.
The app uses the OMDB API to fetch movie data based on the user's search input. When a user clicks on a movie, the onSelectMovie callback function is called with the movie's imdbID as the argument. This function sets the selected movie's ID in the parent component's state, which triggers the rendering of the MovieDetails component.

When a user rates a movie and adds it to the watched list, the onAddWatched callback function is called with the new watched movie object as the argument. This function adds the new watched movie to the parent component's watched state array, which triggers the rendering of the WatchedSummary and WatchedMovieList components.

When a user clicks the delete button on a watched movie, the onDeleteWatched callback function is called with the movie's imdbID as the argument. This function removes the watched movie from the parent component's watched state array, which triggers the re-rendering of the WatchedMovieList and WatchedSummary components.

## Contributing
Contributions are welcome! Please submit a pull request with your changes.

## License
This project is licensed under the MIT License.
