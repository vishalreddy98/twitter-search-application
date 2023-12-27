# Twitter Search Application using Database Management Systems
Repository containing the code for the final project for the [STAT-694] Data Management for Advanced Data Science Applications course at Rutgers University - New Brunswick, during the Spring 2023 semester.

## Important Information
Please use Python 3.9 to run this code, preferably 3.9.13.

## Initial (One-Time) Setup
1. In a terminal, type the following: "pip install -r requirements.txt"
2. Download PostgreSQL. Open the application and make sure the server is running.
3. Go to utils > twitter-users.ipynb and run the file. Give your system's username when prompted. Please make sure that the file 'corona-out-3' is added to the utils folder prior to running the file.
4. Go to utils > tweets_to_mongoDB.ipynb and run the file. This is suggested to check the connection to the MongoDB cluster.

## Running the API
1. In the terminal, type: "cd src". This command allows you to change the working directory to the 'src' folder.
2. Type this command in the terminal to start the API server: "python -m uvicorn main:app --reload" or "python main.py"
3. Go to http://127.0.0.1:8000/docs to make a search.
