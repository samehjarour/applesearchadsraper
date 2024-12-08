# applesearchadsraper
Files for the Apples Ad Search Scraper
# Apple Ads Repository Scraper
This project is a web scraping tool built using Apify SDK and Crawlee. It automates the extraction of advertisement data from the Apple Ads Repository, supporting advanced filtering by developer, country/region, and date range.

Features
Dynamic Filtering: Apply filters for Developer/App, Country/Region, and Date Range.
Infinite Scroll Handling: Automatically scrolls to load more content.
Error Handling: Retries on failed requests and logs missing elements.
Data Export: Extracted data is stored in the Apify dataset.
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/apple-ads-repository-scraper.git
cd apple-ads-repository-scraper
Install dependencies:

bash
Copy code
npm install
Ensure you have Apify CLI installed:

bash
Copy code
npm install -g apify-cli
Usage
Running Locally
Configure the input parameters in input.json:

json
Copy code
{
    "startUrls": [
        { "url": "https://adrepository.apple.com/" }
    ],
    "developerOrApp": "Sample Developer",
    "countriesOrRegions": ["United States", "Germany"],
    "dateRange": "Last 90 Days"
}
Run the scraper:

bash
Copy code
apify run
Deploying to Apify
Push the actor to your Apify account:

bash
Copy code
apify push
Run the actor from the Apify platform with your desired input.

Input Parameters
startUrls (array): List of URLs to start the scraping process.
developerOrApp (string, optional): The developer or app name to filter ads.
countriesOrRegions (array, optional): List of countries or regions to filter ads (e.g., ["United States", "Germany"]).
dateRange (string, optional): Date range to filter ads (e.g., "Last 90 Days").
Example Input
json
Copy code
{
    "startUrls": [
        { "url": "https://adrepository.apple.com/" }
    ],
    "developerOrApp": "Sample Developer",
    "countriesOrRegions": ["United States", "Germany"],
    "dateRange": "Last 90 Days"
}
Output
The extracted data is saved in the Apify dataset in the following format:

json
Copy code
[
    {
        "title": "Ad Title",
        "description": "Ad Description",
        "image": "https://example.com/ad-image.png"
    },
    ...
]
File Structure
main.js: Entry point for initializing the crawler and handling inputs.
routes.js: Contains the scraping logic, including handling filters and data extraction.
package.json: Project dependencies.
input_schema.json: Schema for input parameters validation.
Debugging
Logs: View detailed logs in the console or Apify platform.
Screenshots: Captures screenshots of the loaded page (debug-page.png) to aid troubleshooting.
HTML Dump: Logs the full page HTML structure.
Known Issues
Dropdown Elements Not Found:

Ensure that the provided selectors are up-to-date and reflect changes on the Apple Ads Repository page.
Bot Detection:

Use proper headers and mimic user interactions to avoid bot detection.
Contributing
Fork the repository.
Create a feature branch:
bash
Copy code
git checkout -b feature-name
Commit changes:
bash
Copy code
git commit -m "Add new feature"
Push changes and open a pull request.
License
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
For any issues or feature requests, please open an issue in this repository or contact the author via GitHub.
