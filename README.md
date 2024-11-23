# Slack Thread Exporter

## Description

A Python script to export Slack threads to Markdown files, including user mentions, attachments, and reactions.

## Features

- Resolve Slack user IDs to usernames.
- Handle attachments and blocks in messages.
- Download and embed file attachments.
- Export reactions associated with messages.
- Opsgenie-specific message formatting.
- Comprehensive logging.

## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/walbeh/slack-thread-exporter.git
    cd slack-thread-exporter
    ```

2. **Create a virtual environment and activate it:**

    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3. **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

## Configuration

1. **Slack Bot Token:**

    Obtain a Slack Bot Token with the required scopes. Set it as an environment variable:

    ```bash
    export SLACK_TOKEN='xoxb-your-slack-bot-token'
    ```

    Alternatively, you can pass it as a command-line argument when running the script.

## Required Slack Bot Token Scopes

Ensure your Slack app has the following [OAuth scopes](https://api.slack.com/authentication/oauth-v2#scopes):

- `channels:read`: To access channel information.
- `channels:history`: To read message history in channels.
- `groups:read`: To access private channels information.
- `groups:history`: To read message history in private channels.
- `users:read`: To resolve user IDs to usernames.
- `files:read`: To download file attachments.
- `reactions:read`: To access reactions on messages.

## Usage

Run the script with the Slack thread URL:

```bash
python sl-ex.py <xoxb-xxxxx> <SLACK_LINK>
