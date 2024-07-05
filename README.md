# Hit the Google Trends API with DuckDB

Definitely don't do this for anything in production.

## How do I find the Google Trends Endpoint I need?

Go to trends.google.com and search for the term you're interested in. Then, open the network tab in your browser's developer tools and look for a request to a URL that looks like `https://trends.google.com/trends/api/widgetdata/multiline/csv?req=...`. This is the URL you need to hit.

## I'm getting a 401 error with your example code

The request has a token inlined into it that expires after a while. You'll need to get your own token by visiting the URL in your browser.

## I'm getting CORS errors using this with Evidence

You can't hit the Google Trends API from the browser because of CORS. You can disable CORS in your browser using an extension. You can also just use DuckDB from the CLI.

## This still doesn't work

This is a toy project. I haven't tested it for more than 5 minutes. Also Google might change their API at any time. Good luck!