# MLS-Player-Similarity-Network
Player Similarity Network of players in the MLS league


Introduction
The Player Similarity Network is a web application built using Dash, BeautifulSoup, pandas, scikit-learn, and plotly. The app scrapes data from FBref, processes it to calculate player statistics, and visualizes a network graph showing similarities between players based on their performance metrics.
Features
•	Scrapes player statistics from multiple FBref pages.
•	Processes and cleans the data.
•	Groups players by their positions.
•	Calculates per 90 minutes statistics.
•	Generates a similarity matrix using cosine similarity.
•	Creates and visualizes a network graph of player similarities.
Installation
To run the app, ensure you have Python installed and install the necessary packages:
bash
------------------------------------------------------------------------------------------------------------------
pip install requests pandas beautifulsoup4 scikit-learn numpy networkx plotly dash 
------------------------------------------------------------------------------------------------------------------
Usage
1.	Clone the repository:
-------------------------------------------------------------------------------------------------------------------
git clone https://github.com/yourusername/player-similarity-network.git
cd player-similarity-network
-------------------------------------------------------------------------------------------------------------------
Run the app
-------------------------------------------------------------------------------------------------------------------
python app.py
-------------------------------------------------------------------------------------------------------------------
3.	Open a web browser and go to http://127.0.0.1:8050 to view the app.
Functions
scrape_fbref_data(url)
Scrapes data from the given FBref URL and returns a DataFrame.
rename_duplicate_columns(df, suffix)
Renames duplicate columns in the DataFrame by appending a suffix.
create_full_stats_db()
Creates a full statistics database by scraping and merging data from multiple FBref pages.
position_grouping(x)
Groups player positions into broader categories.
per_90fi(dataframe)
Calculates per 90 minutes statistics for the given DataFrame.
key_stats_db(df, position)
Extracts key statistics for players of a specific position.
create_similarity_matrix(df, method='cosine')
Creates a similarity matrix using the specified method (cosine or euclidean).
create_network(player_name, similarity_matrix, threshold=0.99)
Creates a network graph for the specified player based on the similarity matrix.
Dash App
Layout
•	A dropdown for selecting a team.
•	A dropdown for selecting a player from the chosen team.
•	A graph displaying the similarity network for the selected player.
Callbacks
set_player_options(selected_team)
Updates the player dropdown based on the selected team.
update_graph(selected_player)
Updates the network graph based on the selected player.


