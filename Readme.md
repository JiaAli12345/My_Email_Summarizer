
# MySmartMail: AI Email Summarizer & Task Assistant

This Python application uses the Ollama LLaMA 3 model (via the Ollama-python library) to automatically summarize emails and generate actionable task lists from your Gmail account. MySmartMail connects to Gmail, fetches emails, summarizes their contents, and identifies key action items to boost your productivity.

## Features

- **Gmail Integration**: Securely fetches emails from your Gmail inbox.
- **AI Summarization**: Uses LLaMA 3 to summarize email content.
- **Task Extraction**: Automatically generates to-do lists from important emails.
- **Daily Digest**: Provides a daily summary of all important emails.

## Prerequisites

- Python 3.8+
- Gmail account
- Gmail API credentials in `credentials.json`
- Required Python libraries: `ollama`, `google-auth`, `google-auth-oauthlib`, `google-api-python-client`, `bs4`

## Installation

1. Clone this repository or download the source code.
2. Install dependencies:
   ```bash
   pip install ollama google-auth google-auth-oauthlib google-api-python-client bs4
   ```
3. Set up Gmail API credentials:
   - Follow [these instructions](https://developers.google.com/gmail/api/quickstart/python#set_up_your_environment) to enable the Gmail API and download your `credentials.json`.

## Usage

1. Run the script:
   ```bash
   python MySmartMail.py
   ```
2. Authorize Gmail access in your browser on first run.
3. The script fetches new emails, summarizes them, and saves a daily summary and task list to `daily_summary.txt`.

## Example Output

```
To-do list from email summaries:

* Register for the webinar on May 21
* View billing statement (Westlake Financial)
* Apply by February 6th at apply.oru.edu

Summary of highlights:

The past 24 hours included a webinar invitation, a university application opportunity, and several marketing emails. No urgent actions required.
```

## Troubleshooting

- Ensure `token.json` is generated and up-to-date.
- Check the console for Gmail API or model errors.

## Contributing

Fork the repo and submit pull requests. Open issues for bugs or feature requests.

## Roadmap

- Add support for Office365 and Yahoo Mail
- Build a graphical user interface (GUI)
- Improve AI prompt customization
- Integrate Telegram bot notifications

## License

Licensed under the Apache License 2.0. See [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).