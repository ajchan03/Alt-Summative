# How does comments regarding Trump differ in sentiment across different political subreddits?

## Description
This project analyzes political discussions on Reddit through examining comments from various political subreddits, giving insights about polarization, sentiment intensity, and user engagement in online political discussions.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Data Sources](#data-sources)


---

## Installation

Follow these steps to set up the project:

### Step 1: Clone the Repository
```bash
git clone git@github.com:lse-ds105/ds105a-2024-alternative-summative-ajchan03.git
```
This will download the repository's contents to a local folder.

### Step 2: Set Up a Virtual Environment
1. Navigate to the project directory:
   ```bash
   cd /path/to/ds105a-2024-alternative-summative-ajchan03
   ```

2. Create a virtual environment:
   ```bash
   python -m venv .venv
   ```

3. Activate the virtual environment:
   - On macOS/Linux:
     ```bash
     source .venv/bin/activate
     ```
   - On Windows:
     ```bash
     .venv\Scripts\activate
     ```
   A **(.venv)** should appear in your terminal prompt.

4. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

5. Ensure the correct Python kernel is selected when running Jupyter notebooks.

---

### Step 3: Set Up Reddit API Authentication
Since this project uses Reddit’s API, you need your own credentials to collect data.

1. Go to [Reddit API Apps](https://www.reddit.com/prefs/apps) and create an app.
2. Set the app type to **"script"**.
3. Copy your **Client ID**, **Client Secret**, **Username**, and **Password**.
4. Store these credentials securely in a `.env` file:

```bash
REDDIT_CLIENT_ID=your_client_id
REDDIT_CLIENT_SECRET=your_client_secret
REDDIT_USERNAME=your_username
REDDIT_PASSWORD=your_password
```

5. Save this `.env` file in the root directory.

---

## Usage

### Running the Data Scraper (NB01)
To collect Reddit data, run the first notebook:

```bash
jupyter notebook NB01-Data Collection.ipynb
```

This will:
✅ Authenticate to the Reddit API  
✅ Scrape political comments from selected subreddits  
✅ Store the raw data in JSON format  

### Processing Data (NB02)
To clean and structure the collected data, run:

```bash
jupyter notebook NB02-Data Cleaning and Storage.ipynb
```

This will:
✅ Remove duplicates and filter unwanted comments  
✅ Store cleaned data in an SQLite database  

### Generating Visualizations (NB03)
To analyze and visualize Reddit discussions, run:

```bash
jupyter notebook NB03- Data Visualisation and Analysis.ipynb
```

This will:
✅ Generate sentiment distribution charts  


---

## Data Sources

This project utilizes data from:
1. [Reddit API](https://www.reddit.com/dev/api/) - for fetching posts and comments.  
2. [VADER Sentiment Analysis](https://github.com/cjhutto/vaderSentiment) - for sentiment scoring of comments.  

---
