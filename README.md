# 🎧 The DNA of a Hit: Strategic Audio Analysis for Playlist Curation
### A Statistical Deep Dive into Top-Streamed Tracks

![Data Analysis](https://img.shields.io/badge/Analysis-Descriptive%20Statistics-blue)
![Business Intelligence](https://img.shields.io/badge/Domain-Media%20%26%20Entertainment-green)
![Google Sheets](https://img.shields.io/badge/Tools-Google%20Sheets-success)
![Excel](https://img.shields.io/badge/Tools-Microsoft%20Excel-orange)

---

## 📖 Background & Business Case
In the hyper-competitive streaming era, music curators and labels can no longer rely solely on "gut feeling" to predict success. With thousands of tracks released daily, identifying the specific audio DNA that drives listener engagement is a critical business advantage.

I conducted this analysis to move beyond subjective "vibe" checks. By analyzing the physical attributes of popular music—such as Energy, Acousticness, and Pitch—I’ve defined a "Hit Profile" that helps curators optimize track selection for maximum ROI and listener retention.

---

### 📂 Data Reference
* **Source:** [Spotify Tracks Dataset via Hugging Face](https://huggingface.co/datasets/maharshipandya/spotify-tracks-dataset)
* **Sample Size:** 3,000 tracks selected for granular statistical modeling.
* **Fields:** `Energy`, `Valence` (Mood), `Acousticness`, `Loudness`, `Key`, and `Duration`.

---

## ⚙️ Methodology & Analytical Process
I followed a structured 3-phase statistical lifecycle to find patterns within a dataset of popular Spotify tracks:

### 📊 Phase 1: Identifying Market Norms (Central Tendency)

* **The Objective:** *What are the "typical" musical characteristics of a hit song, and is there a favorite key?*

* **Analysis Logic:** I used **Histograms** for continuous variables ( Energy, Valence, and Acousticness) and **Column Charts** for discrete categories like Key. 
* **The Findings:**
    * **Energy Intensity:** Hits cluster heavily around a mean of **0.79**, proving that high-intensity tracks dominate the market.
    * **The "Hit" Key:** By identifying the **Mode**, I found that **Key 1 (C♯/D♭)** is the most frequent choice for top-performing tracks.
    * **Acousticness Bias:** The market shows a massive preference for produced sounds over acoustic ones (Mean score near 0.0).

**Central Tendency Analysis:**
| Feature | Mean | Median | Mode |
| :--- | :--- | :--- | :--- |
| **Valence** | 0.46 | 0.45 | N/A (Continuous) |
| **Energy** | 0.79 | 0.82 | N/A (Continuous) |
| **Acousticness** | 0.15 | 0.04 | N/A (Continuous) |
| **Key** | 5.25 | 5.00 | **1 (C♯/D♭)** |


* **Formulas Used:**
> * **Mean:** `AVERAGE()` - To find the average "center" of the music features.
> * **Median:** `MEDIAN()` - To find the middle value and check if the average is being pulled by outliers.
> * **Mode:** `MODE()` - Used for **Key** to find the most frequent pitch used in hits.

### Visualizations:
<p align="center">
  <img src="Distribution of Valence.png" width="45%" /> 
  <img src="Distribution of Energy.png" width="45%" />
  <img src="Distribution of Acousticness.png" width="45%" />
  <img src="Distribution of Key.png" width="45%" />
</p>

---

## 📉 Phase 2: Consistency & Variety (Variation & Skewness)
* **The Objective:** *How reliable are these trends? Do hits always have to be "happy"?*

* **Analysis Logic:** I used **Standard Deviation** to measure the risk/variety and **Skewness** to detect if the market leans heavily toward one style.
* **The Findings:**
    * **Reliable Energy:** A low spread (0.18) means high energy is a consistent requirement.
    * **Emotional Flexibility:** Valence (mood) is perfectly balanced (0.025 skew). This proves "sad" songs can be just as popular as "happy" ones, as long as the production is intense.

**Variability & Skewness:**
| Feature | Standard Deviation | Skewness | Market Sentiment |
| :--- | :--- | :--- | :--- |
| **Valence** | 0.2272 | 0.0250 | **Balanced:** No preference for happy vs. sad. |
| **Energy** | 0.1825 | -0.6298 | **Biased:** Strong preference for high energy. |
| **Acousticness**| 0.2400 | 1.4000 | **Rare:** Acoustic hits are very uncommon. |

* **Formulas Used:**
> * **Standard Deviation:** `STDEV()` - To measure the "spread." A low number means the tracks are very similar to each other.
> * **Skewness:** `SKEW()` - To see if the data is lopsided. (e.g., 0 = perfectly balanced, >1 = heavily leaning to one side).

---

## 🔗 Phase 3: Feature Synergies (Correlation)
* **The Objective:** *Does volume affect energy? Does track length impact success?*

* **Analysis Logic:** I used Scatter Plots and Pearson’s Correlation ($r$) to identify how audio features move together.
* **The Findings:**
    * **Loudness is Energy ($r = 0.70$):** High-energy hits almost always require a louder mastering profile.
    * **The "Length Myth" ($r = 0.01$):** There is **no relationship** between song length and energy. Hits can be any duration as long as the intensity is right.

* **Formulas Used:**
> * **Correlation:** `CORREL()` - To determine if two features move together (1.0), move opposite (-1.0), or are unrelated (0).

### Correlation Plots
<p align="center">
  <img src="Loudness vs Energy.png" width="45%" />
  <img src="Acousticness vs Energy.png" width="45%" />
  <img src="Duration vs Energy.png" width="45%" />
</p>

---

## 🛠️ Tools & Skills:
* **Environment:** Google Sheets
* **Statistical Methods:** Central Tendency, Variability, Skewness, Pearson Correlation ($r$).
* **Data Storytelling:** Converting abstract numbers into clear advice for curators.

---

## 💡 Strategic Recommendations:
1. **Optimize for "Perceived Intensity":** Prioritize tracks with an **Energy score > 0.70**. Since Energy and Loudness are highly correlated, ensuring a track is mastered competitively is critical for hit potential.
2. **Prioritize Produced Content:** The high positive skew in Acousticness shows that most hits are non-acoustic. Focus curation on produced/electronic textures for mainstream success.
3. **Broaden Emotional Range:** Mood (Valence) is balanced in popular music. Focus on **energy consistency** rather than sticking to just "happy" or "sad" songs.

---

## 🎓 Project Credits:
This analysis was developed as part of the **Applied Statistics for Data Analytics** course by **DeepLearning.AI** on Coursera. It demonstrates proficiency in applying statistical models to solve business-oriented problems in the media and entertainment domain.

---
## 👤 About the Author:
**Ayushi Gajendra** 

*Data Analyst | Ex-Startup Co-founder*
* **7+ Years** of experience in business operations and strategic growth.
* I specialize in turning raw data into **clear business decisions**.
* My goal is to help companies stop "guessing" and start growing using data.
