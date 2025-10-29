<h1>Analyzing Trader Behavior During Fear and Greed Cycles</h1>

<p><strong>Overview</strong><br>
This project analyzes how trader behavior changes during different market sentiment cycles — specifically during Fear and Greed phases. The analysis combines a trader activity dataset (trade size, leverage, profit) with a market sentiment dataset (Fear &amp; Greed Index).</p>

<hr>

<h2>Problem Statement</h2>
<p>Does market sentiment (Fear vs Greed) influence trader behavior in terms of:</p>
<ul>
  <li>Trade size</li>
  <li>Leverage used</li>
  <li>Profitability</li>
</ul>

<hr>

<h2>Approach</h2>
<h3>Data Processing (Phases 1–3)</h3>
<ul>
  <li>Cleaned raw datasets and removed duplicates / nulls</li>
  <li>Converted timestamps to <code>datetime</code> and extracted dates</li>
  <li>Renamed columns for clarity (e.g., <code>Size Tokens → leverage</code>, <code>Size USD → size</code>)</li>
  <li>Merged trader and sentiment datasets on the common date key</li>
</ul>

<h3>Analysis (Phase 4)</h3>
<ul>
  <li>Grouped merged data by sentiment classification (Fear / Greed)</li>
  <li>Calculated average profit, average leverage, and average trade size per sentiment</li>
  <li>Generated the following visualizations: average profit, average leverage, average trade size vs sentiment</li>
</ul>

<hr>

<h2>Key Insights</h2>

<table>
  <thead>
    <tr>
      <th>Market Sentiment</th>
      <th>Average Profit</th>
      <th>Average Leverage</th>
      <th>Average Trade Size</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Greed</td>
      <td>Higher</td>
      <td>Higher</td>
      <td>Larger</td>
    </tr>
    <tr>
      <td>Fear</td>
      <td>Lower</td>
      <td>Lower</td>
      <td>Smaller</td>
    </tr>
  </tbody>
</table>

<p><strong>Conclusion:</strong> Traders tend to take higher risks during Greed (higher leverage and larger trade sizes) and behave conservatively during Fear.</p>

<hr>

<h2>Technologies Used</h2>
<ul>
  <li>Python</li>
  <li>Pandas</li>
  <li>Matplotlib, Seaborn</li>
  <li>Google Colab</li>
</ul>

<hr>

<h2>Project Folder Structure</h2>
<pre>
Analyzing_Trader_Behavior_Fear_Greed/
├── csv_files/
│     ├── trader_data.csv
│     └── fear_greed.csv
├── output/
│     └── charts/
│           ├── avg_profit_vs_sentiment.png
│           ├── avg_leverage_vs_sentiment.png
│           └── avg_trade_size_vs_sentiment.png
├── Market_Sentiment_Impact_on_Trading.ipynb
├── Fear_Greed_Trading_Report.pdf
└── README.md
</pre>

<hr>

<h2>How to Run the Project</h2>
<ol>
  <li>Open Google Colab.</li>
  <li>Upload the notebook file: <code>Market_Sentiment_Impact_on_Trading.ipynb</code>.</li>
  <li>Upload both dataset CSV files located in the <code>csv_files/</code> folder.</li>
  <li>Run all cells in sequence. Visualizations will be saved to <code>output/charts/</code>.</li>
</ol>

<hr>

<h2>Author</h2>
<p><strong>Prajwal Mesare</strong><br>Data Science Intern</p>
