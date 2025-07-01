# Data Cleaning using Python

# Friend Recommendation System using Mutual Connections 🤝

This project is a simple yet effective implementation of a **"People You May Know"** recommendation system. It uses mutual friend connections to suggest new friends to a user, similar to social networking platforms like Facebook or LinkedIn.

## 📂 Project Structure

- **Jupyter Notebook**: Core logic implemented in Python
- **`data.json`**: Contains users and their friend connections
- **Python Logic**: Reads data, builds a network graph, and recommends friends based on mutual connections

## 🚀 Features

- Load user data from a JSON file
- Construct friend relationships
- Recommend users based on the number of mutual friends
- Sorted suggestions based on highest mutual count

## 🧠 How it Works

1. Each user has a list of direct friends.
2. For a given user, the system finds all friends of friends.
3. Excludes direct friends and the user themself.
4. Counts how many mutual friends exist between the user and suggested people.
5. Returns a sorted list of suggested users.

## 📂 Files

- `data.json` – Contains sample user-friend data.
- `people_you_may_know.ipynb` – Main logic in Python using JSON and dictionaries.

## 🧪 Sample Output

people you may know 1: [5, 6]

# Social Network Data Cleaning Script 🧹

This project focuses on cleaning user data typically used in social networking applications. The data consists of users and their friend lists. The script removes inconsistencies to ensure cleaner input for downstream processes like recommendation engines or graph analytics.

## 📂 Features

- Removes users with empty or whitespace-only names
- Eliminates duplicate entries in each user's list of friends
- Ensures the dataset is in a valid format for further analysis

## 🧠 How it Works

- Loads JSON data containing a list of users
- Filters out users whose names are blank
- Converts each user's list of friends to a set to remove duplicates, then back to a list

## 🔍 Sample Code Logic

```python
data['users'] = [user for user in data['users'] if user['name'].strip()]
for user in data['users']:
    user['friends'] = list(set(user['friends']))
