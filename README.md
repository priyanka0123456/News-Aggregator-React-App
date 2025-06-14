
### Features:
1.**Article Search and Filtering**: Users can search for articles by entering keywords. Filtering options are available by date, category, and source.<br>
2.**Personalized News**: Feed Users can customize their news feed by selecting preferred sources, categories, and authors.<br>
3.**Mobile-Responsive Design**: The website is optimized for both desktop and mobile devices.<br>
4.**Data Sources**: The application uses the following data sources:<br>
-NewsAPI: Provides access to a wide range of news articles from various sources.<br>
-The Guardian API: Fetches articles from The Guardian.<br>
-New York Times API: Retrieves articles from The New York Times.

### Technologies Used:-<br>
1.**React.js**: A JavaScript library for building user interfaces.<br>
2.**Redux Toolkit**: For state management.<br>
3.**Axios**: For making HTTP requests to fetch data from APIs.<br>
4.**React Bootstrap**: For UI components and styling.<br>
5.**Docker**: For containerizing the application.<br>
### Folder Structure: <br>
``` news-aggregator/
  ├── public/ 
  │ └── index.html 
  ├── src/ 
  │ ├── components/
  │ │ ├── Error/
  │ │ │ └── Error.js
  │ │ ├── Loading/
  │ │ │ ├── index.js
  │ │ │ └── Loading.js
  │ │ ├── NavBar/
  │ │ │ ├── Loading.js
  │ │ │ └── Loading.css
  │ │ ├── News/
  │ │ │ ├── index.js
  │ │ │ ├── News.js
  │ │ │ └── News.css
  │ │ ├── NewsCard/
  │ │ │ ├── NewsCard.js
  │ │ │ ├── NewsCard.css
  │ │ │ └── Details/
  │ │ │ ├── Details.js
  │ │ │ └── Details.css
  │ │ ├── NoDataFound/
  │ │ │ ├── NoDataFound.js
  │ │ │ └── NoDataFound.css
  │ │ ├── NoRouteFound/
  │ │ │ └── NoRouteFound.js
  │ │ └── ScrollToTop/
  │ │ └── ScrollToTop.js
  ├── App.js
  ├── index.js
  └── package.json
 ``` 


### Implementation Details:-<br>
1.**Search and Filtering**<br>
*SearchBar Component*: Allows users to search articles by entering keywords. This triggers a search request to the selected data sources.<br>
*FilterOptions Component*: Users can filter articles based on categories, date ranges, and sources. This component interacts with Redux to update the filter criteria.<br>
2.**Personalized News Feed**<br>
*PersonalizedFeed Component*: Displays a custom news feed based on user preferences such as preferred categories, sources, and authors. User preferences are stored in Redux and used to fetch and display relevant articles.<br>
3.**Mobile-Responsive Design**<br>
*Responsive Layout*: The UI components are designed using React Bootstrap, ensuring the layout adjusts for different screen sizes. Media queries are used for custom styling on mobile devices.<br>
4.**API Integration**
api.js contains four different data sources newsAPI, guardianAPI, nytAPI, and gnewsAPI: These service file handle API requests to the respective data sources. It contains functions to fetch data, and convert all the data into normalize data which are used in Redux actions and components.

5.**Redux Toolkit**: Used to manage the state of the application, including articles fetched, user preferences, and filter criteria. Redux slices (articlesSlice.js) are created to handle specific aspects of the state.
<br>
### Project Setup and Dockerization:-<br>
1.**Clone the Repository**:git clone https://github.com/priyanka0123456/News-Aggregator-React-App.git <br><br>
2.**Install Docker**:Ensure Docker is installed on your machine. You can download it from Docker's official website.<br> <br>
3.**Build the Docker Image**:<br>
``` docker build -t news-aggregator ``` . <br><br>
4.**Run the Docker Container**:<br>
docker run -p 80:80 news-aggregator<br><br>
Alternatively, if you are using Docker Compose, run:<br>
```docker-compose up --build```<br><br>
5.**Access the Application**:<br>
Open your web browser and go to http://localhost to see the application running.<br>
Stopping the Container:<br><br>
If you started the container with Docker Compose, stop it using:<br>
```docker-compose down```<br><br>
If you started the container directly, find the container ID with:<br>
```docker ps```<br><br>
Then stop it with:<br>
```docker stop <container_id>```<br>

