# Twitter Scraper CLI

A Python package to scrape Twitter trends and tweets using Selenium. It provides a command-line interface (CLI) for easy use and doesnot require any twitter api.

## Features

- Scrape trending topics from Twitter.
- Scrape tweets for specific trends.
- Specify the fields you want to scrape (e.g., tweet text, images, likes).

## Installation

To install the package, run:

```bash
pip install twitter-cli-scraper
```

## Usage

The Twitter Scraper CLI can be used via the command line after installation. Below are some examples of usage:

### 1. Scraping Twitter Trends

To scrape the latest trends from Twitter, use the following command:

```
twitter-scraper --username your_twitter_username --password your_twitter_password --action scrape_trends

```

This command will log in to Twitter using your credentials, scrape the trending topics, and save the data in an Excel file called `trends.xlsx`.

### 2. Scraping Tweets for a Specific Trend

If you want to scrape tweets related to a specific trend, you can do the following:

```
twitter-scraper --username your_twitter_username --password your_twitter_password --action scrape_tweets --trend "trend_name" --fields tweets images likes

```

For example, to scrape tweets for the trend **"WorldCup2024"** and extract both the tweet text and images, you would run:

```
twitter-scraper --username your_twitter_username --password your_twitter_password --action scrape_tweets --trend "WorldCup2024" --fields tweets images

```

This will scrape tweets containing the term "WorldCup2024" and save the results in an Excel file called `tweets.xlsx`.

### 3. Available Fields to Scrape

When scraping tweets, you can specify which fields you want to extract by using the `--fields` option. You can choose from the following fields:

* `tweets`: Scrapes the tweet text.
* `images`: Scrapes any image URLs in the tweet.
* `likes`: Scrapes the number of likes.

If no fields are specified, the tool will default to scraping tweet text (`tweets`).

### 4. Example Commands

#### Scrape Only Trends:

```
twitter-scraper --username your_username --password your_password --action scrape_trends

```

Scrape Tweets for a Trend:

```
twitter-scraper --username your_username --password your_password --action scrape_tweets --trend "Olympics" --fields tweets likes

```

This command will scrape tweets related to the "Olympics" trend and include tweet text and like counts in the output.

## Command Line Arguments

* `--username`: Your Twitter username.
* `--password`: Your Twitter password.
* `--action`: The action to perform (`scrape_trends` or `scrape_tweets`).
* `--trend`: The name of the trend to search for (required for `scrape_tweets` action).
* `--fields`: A list of fields to scrape (e.g., `tweets`, `images`, `likes`). Defaults to `tweets`.

## Output

* **Trends** : Saved as `trends.xlsx` containing trending topics and related keywords.
* **Tweets** : Saved as `tweets.xlsx` containing the scraped data based on the specified fields (e.g., tweet text, images, likes).

## Error Handling

If any error occurs during the scraping process, the scraper will attempt to handle it gracefully and log the error for further inspection.

## Contributing

Contributions are welcome! If you find any bugs or want to request a new feature, feel free to open an issue on the [Github repository](https://github.com/bsse23087/twitter-cli-scraper).

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/bsse23087/twitter-cli-scraper/blob/main/LICENSE) file for details.

**Disclaimer** : This tool is for educational purposes only. Please ensure you comply with Twitter's [Terms of Service](https://twitter.com/en/tos) when using this scraper.

### Breakdown:

- **Usage Commands**: Added clear examples for both scraping trends and tweets.
- **Fields Explanation**: Provided options for which fields users can scrape.
- **Example Section**: Showcased sample command-line usage.

This should cover all aspects of usage, including installation, examples, and command-line arguments. Let me know if you need anything else!
