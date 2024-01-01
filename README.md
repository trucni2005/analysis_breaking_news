<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <h1>Analysis Breaking News</h1>
    <section>
        <h2><i class="fas fa-bullseye"></i> Purpose</h2>
        <p>This project performs data collection and analysis from top news websites in Vietnam to provide information about current and popular events.</p>
    </section>
    <section>
        <h2><i class="fas fa-cogs"></i> Functionality</h2>
        <ol>
            <li>
                <strong>Crawl Data:</strong>
                <ul>
                    <li>Crawl data from the sports and cultural news.</li>
                    <li>Crawl data from VietnamPlus.</li>
                    <li>Crawl data from the Vietnam News Agency.</li>
                </ul>
            </li>
            <li>
                <strong>Merge Data:</strong>
                <ul>
                    <li>The <code>merge_data(data)</code> function retrieves data from the raw_data directory of a news source, combines CSV files, and adds a "news source" column.</li>
                    <li>The <code>create_df_merged()</code> function uses <code>merge_data</code> to create a DataFrame containing data from all news sources.</li>
                    <li>Other functions like <code>strip_category</code>, <code>del_duplicate_links</code>, <code>del_null_time_data</code>, <code>clean_duplicate_news_data</code>, <code>convert_time_data</code>, <code>remove_infographic_from_title</code> are used to clean and normalize the data.</li>
                </ul>
            </li>
            <li>
                <strong>Export Cleaned Data:</strong>
                <ul>
                    <li>The <code>export_cleaned_data()</code> function creates and exports a CSV file containing cleaned data from news sources.</li>
                </ul>
            </li>
            <li>
                <strong>Export JSON Based on Start Date and Category:</strong>
                <ul>
                    <li>The <code>export_json(start_date, category_in)</code> function creates and exports a JSON file containing detailed information about posts based on the specified start date and category.</li>
                </ul>
            </li>
            <li>
                <strong>Update Database:</strong>
                <ul>
                    <li>The <code>update_database()</code> function calls the <code>crawl_data()</code> function and then exports the cleaned data.</li>
                </ul>
            </li>
            <li>
                <strong>Crawl News TikTok:</strong>
                <ul>
                    <li>The <code>crawl_news_tiktok(news, reader)</code> function collects data from the TikTok page of identified news sources and exports the data to a CSV file.</li>
                </ul>
            </li>
            <li>
                <strong>Daily Update:</strong>
                <ul>
                    <li>The <code>daily_update()</code> function automatically updates the database daily, including data collection from TikTok.</li>
                </ul>
            </li>
        </ol>
    </section>
    <section>
        <h2><i class="fas fa-cogs"></i> Requirements</h2>
        <ul>
            <li>Python 3.x</li>
            <li>Libraries listed in the <code>requirements.txt</code> file</li>
        </ul>
    </section>
    <section>
        <h2><i class="fas fa-book"></i> How to Use</h2>
        <ol>
            <li>Install requirements by running: <code>pip install -r requirements.txt</code>.</li>
            <li>Run the <code>update_database()</code> script to update the database.</li>
            <li>Perform specific functions as needed.</li>
        </ol>
    </section>
</body>
</html>
