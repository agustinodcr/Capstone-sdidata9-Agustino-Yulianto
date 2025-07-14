# 🎧 Spotify Data Analysis with IBM Granite

## 🧠 Project Overview

This project explores and analyzes a large-scale public dataset from Spotify containing over 114,000 songs. Using AI capabilities from IBM Granite and LangChain in Google Colab, the project extracts meaningful insights such as the most danceable genres, most popular tracks, and audio feature trends across various music categories. The goal is to demonstrate how AI models can support data exploration and insight generation from real-world datasets.

## 📂 Raw Dataset

- Source: [Spotify Dataset](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset)
- Format: CSV
- Size: ~114,000 rows × 21 columns
- Sample Columns: `track_name`, `artists`, `popularity`, `danceability`, `energy`, `valence`, `track_genre`, etc.

## 💡 Insight & Findings

1. **Genre with Highest Valence:**
Based on AI results, the **acoustic** genre has the highest average valence of around **0.143**, indicating that this genre tends to convey a more positive emotional tone than other genres.

2. **Top 3 Most Popular Songs:**
The most popular songs in the dataset are:
- **Unholy (feat. Kim Petras)** – Sam Smith; Kim Petras (recorded twice as the highest popularity)
- **Quevedo: Bzrp Music Sessions, Vol. 52** – Bizarrap; Quevedo
*Note:* There are duplicates due to ties (equal popularity values), so only two unique songs are included in the Top 3.

3. **Explicit vs. Non-Explicit Popularity:**
**Explicit (adult content) songs** have a **higher average popularity** than non-explicit songs in this dataset.

4. **Popularity Distribution:**
The histogram generated from 1,000 song samples shows a distribution of popularity values that tends to cluster around 50–70, with several outliers at the top and bottom.


## 🤖 AI Support (IBM Granite via LangChain)

We used IBM Granite models through LangChain’s `create_pandas_dataframe_agent` to analyze the dataset using natural language prompts such as:

- `"Which genre has the highest average valence?"`
- `"Top 3 most popular songs with track name and artist only"`
- `"Are explicit songs more popular than non-explicit songs?"`
- `"Plot histogram of track popularity from sample of 1000 songs"`

These prompts were executed through `agent.invoke()` and allowed non-technical users to explore data effectively.

## 🧪 Tools & Stack

- IBM Granite LLM via LangChain
- Google Colab (Python, Pandas, Matplotlib)
- Seaborn for visualization
- GitHub for project version control

## 📊 Visualization Example

![popularity_histogram](https://drive.google.com/file/d/1yiMkDt9V2RAYev9DP_syDcq1vJS1eB4c/view?usp=drive_link)

> Histogram showing popularity distribution of tracks.

## ✅ Conclusion & Recommendations

- The **'acoustic'** genre has the highest average valence, suggesting it tends to express more positive or emotionally warm tones.
- **Explicit songs** are generally more popular than non-explicit ones based on average popularity in the dataset.
- The most popular songs in the dataset include **"Unholy (feat. Kim Petras)"** and **"Quevedo: Bzrp Music Sessions, Vol. 52"**, both with high popularity scores.
- Using AI tools like **IBM Granite** and **LangChain**, we can quickly explore datasets with natural language prompts, saving time and enabling deeper music analytics.
- For music platforms, integrating AI into their data analysis pipeline could help in **automated trend detection**, **user preference modeling**, and **personalized playlist generation**.
