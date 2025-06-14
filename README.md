# Social-Media-Analytics-with-Spark

Social Media Analytics Platform is a scalable data analysis solution built using Apache Spark for big data processing and Streamlit for interactive visualizations. The project focuses on extracting insights from Twitter (X) data — including trending topics, user engagement metrics, geospatial activity, and network relationships — to understand social media dynamics at scale.

## Features

- **Trending Topics and Hashtags**: Identifies frequently discussed hashtags and keywords.
- **User Engagement Analytics**: Measures likes, retweets, mentions, and replies to determine engagement.
- **Geospatial Analysis**: Maps tweet distributions to understand regional activity.
- **Network Graphs**: Builds user interaction networks to identify key influencers and communities.

## Tech Stack

- Apache Spark (Batch + Streaming)
- Python (Pandas, NLTK, Matplotlib)
- Streamlit (for visualization)
- Twitter API (for data collection)

- Python Socket Server (to simulate real-time streaming)

![workflow](https://github.com/user-attachments/assets/77eb81d0-e046-4b92-86cb-20a2e0aa3191)

## How to Run

### Requirements

1. Install required Python packages:

   ```bash
   pip install -r requirements.txt
2. **Apache Spark**: Ensure that you have **Apache Spark** installed. You can follow the [official Spark installation guide](https://spark.apache.org/docs/latest/) to install it or use a pre-configured environment like **Databricks**.

### Step 1: Start the Python Socket Server

The **Python Socket Server** simulates real-time streaming by reading the `tweets.csv` file line-by-line and sending the data to Spark Streaming via a socket. To start the server:

1. Navigate to the directory where your `socket_server.py` is located.
2. Run the following command:

   ```bash
   python socket_server.py
   ```

### Step 2: Run the Spark Streaming Job

Once the socket server is running, you can run the Spark job to process the real-time data, using the command

   ```bash
   spark-submit spark_streaming.py
   ```

### Step 3: Launch the Streamlit Dashboard
After the data is processed, you can visualize the results with Streamlit:

   ```bash
   streamlit run dashboard.py
   ```
