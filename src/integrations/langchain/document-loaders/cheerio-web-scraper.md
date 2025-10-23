# Cheerio Web Scraper

Cheerio is lightweight and doesn't require a full browser environment like some other scraping tools. Keep in mind that when scraping websites, **you should always review and comply with the website's terms of service and policies to ensure ethical and legal use of the data**.

This module provides a sophisticated web scraper that can:

* Load content from single or multiple web pages
* Crawl relative links from websites
* Extract content using CSS selectors
* Handle XML sitemaps
* Process web content with text splitters

## Inputs

* **URL**: The webpage URL to scrape
* **Text Splitter** (optional): A text splitter to process the extracted content
* **Get Relative Links Method** (optional): Choose between:
  * Web Crawl: Crawl relative links from HTML URL
  * Scrape XML Sitemap: Scrape relative links from XML sitemap URL
* **Get Relative Links Limit** (optional): Limit for number of relative links to process (default: 10, 0 for all links)
* **Selector (CSS)** (optional): CSS selector to target specific content
* **Additional Metadata** (optional): JSON object with additional metadata to add to documents
* **Omit Metadata Keys** (optional): Comma-separated list of metadata keys to omit

## Outputs

* **Document**: Array of document objects containing metadata and pageContent
* **Text**: Concatenated string from pageContent of documents

## Features

* CSS selector-based content extraction
* Web crawling capabilities
* XML sitemap processing
* Configurable link limits
* Error handling for invalid URLs and PDFs
* Metadata customization
* Debug logging support

## Notes

* PDF files are not supported and will be skipped
* Invalid URLs will throw an error
* Setting link limit to 0 will retrieve all available links (may take longer)
* Debug mode provides detailed logging of the scraping process

## Scrape One URL

1. _(Optional)_ Connect [**Text Splitter**](../text-splitters/).
2. Input desired URL to be scraped.

## Crawl & Scrape Multiple URLs

Visit [**Web Crawl**](../../../use-cases/web-scrape-qna.md#id-1.-crawl-multiple-pages) guide to allow scaping of multiple pages.

## Output

Loads URL content as Document

## Resources

* [LangChain JS Cheerio](https://js.langchain.com/docs/integrations/document\_loaders/web\_loaders/web\_cheerio)
* [Cheerio](https://cheerio.js.org/)
