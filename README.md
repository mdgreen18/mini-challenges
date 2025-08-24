🐼📊 Pandas + Matplotlib Mini Challenge Pack
## 🔹 Challenge 1: Log Summary with Pandas

👉 Goal: Practice data loading, filtering, and grouping.
Task:

1. Create a small CSV called logs.csv with columns:
    - timestamp, level, message
    - Example rows:

    ```pgsql 
    2025-08-17 10:00:00, INFO, Service started
    2025-08-17 10:05:00, ERROR, Database connection failed
    2025-08-17 10:06:00, WARNING, Memory usage high
    2025-08-17 10:07:00, ERROR, Timeout reached
    ```
2. Load into Pandas.
3. Count how many times each level occurs (INFO, ERROR, WARNING).
4. Save the summary as log_summary.csv.

---

## 🔹 Challenge 2: Error Frequency Plot

👉 Goal: Apply Pandas value counts + Matplotlib bar chart.
Task:

1. Re-use logs.csv from Challenge 1.
2. Plot a bar chart of error levels (INFO, ERROR, WARNING).
3. Add proper labels & title:
    - Title: "Log Level Frequency"
    - X-axis: "Log Level"
    - Y-axis: "Count"

(Hint: df["level"].value_counts().plot(kind="bar"))

---

## 🔹 Challenge 3: Daily Error Trends

👉 Goal: Combine Pandas grouping with a line plot.
Task:
1. Expand your logs.csv to have multiple days of data (e.g. 2–3 days with a few ERROR logs each).
2. Convert the timestamp column to datetime:
    ```python
    df["timestamp"] = pd.to_datetime(df["timestamp"])
    ```
3. Group by date (not full timestamp) and count how many errors occur per day.
(Hint: df[df["level"]=="ERROR"].groupby(df["timestamp"].dt.date).size())
4. Plot a line graph of errors per day.
