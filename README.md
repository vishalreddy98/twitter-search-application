# Twitter Search Application using Database Management Systems
### Task
The objective of this project is to build an optimized search application using Twitter data enabled with a variety of search criteria that mimic the actual Twitter application.

### Dataset
The data at hand was a JSON file that contains approximately ~100k tweets and ~60k retweets in the form of JSON and nested JSON objects. It is important to note that there were also several retweets that were linked to the same original tweet. In terms of unique tweet (and retweet) ID’s, the total was 112036. The total number of users in this dataset corresponded to 88068. This indicates that a single user has made multiple tweets/retweets.

### Methodology
User information was stored locally in a relational database - PostgreSQL was used for this project. MongoDB Atlas was used as a non-relational data store for Tweets & Retweets information. MongoDB Atlas is a fully managed cloud database that can be easily accessed using its Python distribution - PyMongo. The user interface for the Search Application was designed using FastAPI and uvicorn. In order to make the process of data retrieval faster and more efficient, Least Recently Used (LRU) Caching was implemented.

A bird’s eye view of the project flow is shown below, describing how data is moved across various units.

<img width="468" alt="image" src="[https://github.com/vishalreddy98/twitter-search-application/assets/83286490/a33d916d-6d14-456c-b49c-59d553c153a8]">

### Important Information
Please follow the instructions below to set up and run the application. Please use Python 3.9 to run this code, preferably 3.9.13.

### Initial (One-Time) Setup
1. In a terminal, type the following: "pip install -r requirements.txt"
2. Download PostgreSQL. Open the application and make sure the server is running.
3. Go to utils > twitter-users.ipynb and run the file. Give your system's username when prompted. Please make sure that the file 'corona-out-3' is added to the utils folder prior to running the file.
4. Go to utils > tweets_to_mongoDB.ipynb and run the file. This is suggested to check the connection to the MongoDB cluster.

### Running the API
1. In the terminal, type: "cd src". This command allows you to change the working directory to the 'src' folder.
2. Type this command in the terminal to start the API server: "python -m uvicorn main:app --reload" or "python main.py"
3. Go to http://127.0.0.1:8000/docs to make a search.
