# Sample Snowpark Demo Notebooks

Please Download the sample Jupyter Notebooks to test basic Snowflake functionality. Snowpark currently requires Python 3.8 enviroment. You can easily run these notebooks via VSCODE.

**Requirements:**
1. Python 3.8 Environment 
2. Notebook GUI (Jupyter, VSCODE or others)
3. Install Snowpark-Python Library - `pip install snowflake-snowpark-python`

[Additional Docs for Installing/Configuration of Python & Snowpark Environment](https://docs.snowflake.com/en/developer-guide/snowpark/python/setup)

4. Install Python NLTK library if testing Sentiment Analysis - `pip install nltk`
    

### 1- Basic Data Engineering Dataframe operations 
Read, Join, Summarize & Write large datasets via Dataframes in Snowflake.

[Snowpark_Data_Engineering_Public.ipynb](https://github.com/NickAkincilar/Sample_Snowpark_Demos/blob/main/Snowpark_Data_Engineering_Public.ipynb).


### 2- Running Native Python Code/Libraries within Snowflake via UDFs
[Snowpark_Sentiment_Analysis_Public.ipynb](https://github.com/NickAkincilar/Sample_Snowpark_Demos/blob/main/Snowpark_Sentiment_Analysis_Public.ipynb).

Shows how to ingest data directly from Parquet files & perform Sentiment Analysis on 16,000 Amazon Product reviews via Python NLTK library running on Snowflake compute.
