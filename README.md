# Recommendation_v9

Overview
This script parses and analyzes application usage data from 2 SQLite databases. It processes data from the ZAMDAPPEVENT table in the recommendation_v9.sqlite database and maps AdamIDs to application names using the storeUser.db database. The output is saved as a CSV file, providing detailed information about application usage events.
Prerequisites
•	Python 3.x
•	Required Python packages: pandas

Instructions for Running Recommendation_v9 Script
Installation
1.	Clone the repository:
   git clone https://github.com/yourusername/Recommendation_v9.git
   Or download the repository as a zip file and extract it to a local directory.
   Then cd to Recommendation_v9
2.	Install the required Python packages:
    pip install -r requirements.txt

Running the Script
1.	Ensure you have the recommendation_v9.sqlite and storeUser.db database files available.
2.	Open a command prompt or terminal.
3.	Navigate to the directory where the Recommendation_v9.py script is located.
4.	Run the script with the appropriate paths:
     python Recommendation_v9.py path/to/recommendation_v9.sqlite path/to/storeUser.db
   
Replace path/to/recommendation_v9.sqlite and path/to/storeUser.db with the actual paths to your database files. 
	For example:
   python Recommendation_v9.py D:\Cases\Case1234\recommendation_v9.sqlite D:\Cases\Case1234\storeUser.db

5.	Enter the case number when prompted:

      Please enter the case number: Case1234

6.	The script will process the data and generate the output file:
     Starting script with db_path: D:\Cases\Case1234\Case1234-recommendation_v9.sqlite and storeuser_db_path: D:\Cases\Case1234\storeUser.db
   Fetching app names from storeUser.db...
   Extracted app details: { ... }
   Fetched 100 rows from the database.
   Mapping AdamID 123456789 to app name Example App and bundle ID com.example.app
   ...
   DataFrame created, writing to D:\Cases\Case1234\Case1234-recommendation_v9-StoreUser.db-parsed.csv...
   Data has been written to D:\Cases\Case1234-recommendation_v9-StoreUser.db-parsed.csv
   Script completed.
   Output file: D:\Cases\Case1234\Case1234-recommendation_v9-StoreUser.db-parsed.csv
   
Notes
•	If the purchase_history_apps table is not present in the storeUser.db database, the script will still parse the recommendation_v9.sqlite database and include a note in the details along with the AdamIDs.

   License
This project is licensed under the MIT License. See the LICENSE file for details.
