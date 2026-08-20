# LinkedIn Ads Manager Plugin for Claude Cowork

Manage LinkedIn ad campaigns through natural conversation in Claude Cowork — create campaigns, audit performance, manage targeting and budgets, analyze results, and publish LinkedIn organization content without leaving your workflow.

## What this plugin does

### Skills

| Skill                  | What it does                                                                                                              |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `linkedin-ads-manager` | Full campaign lifecycle: create, clone, pause, resume, budget, targeting, analytics, campaign audits, and organic posting |

### Commands

| Command           | What it does                                                              |
| ----------------- | ------------------------------------------------------------------------- |
| `/linkedin-setup` | Connect your LinkedIn account by configuring the required API credentials |

## Getting started

### 1. Create a local folder for the plugin

Create a folder on your Mac to store your LinkedIn credentials. This folder holds your tokens in a `.env` file that persists between Cowork sessions.

```bash
mkdir -p ~/linkedin-ads
```

### 2. Add the folder to your Cowork project

In Claude Cowork, attach the folder you just created as a local folder for your project.

This allows your credentials to persist between Cowork sessions because the folder is mounted from your Mac into the Cowork environment.

### 3. Install the plugin

You can install the plugin directly from this GitHub repository through Claude Cowork.

1. Open **Claude Cowork**.
2. Go to **Settings** and select **Plugins**.
3. Select **Add Marketplace**.
4. Select **Add from repository** — this lets you sync a plugin marketplace from a GitHub repository or GitHub URL.
5. Enter the following repository URL:

```text
https://github.com/eneelkant/linkedin-ads-manager-claude-plugin
```

6. Click **Sync**.
7. Find **LinkedIn Ads Manager** in the marketplace.
8. Click **Install**.

Once installed, the plugin is available in Claude Cowork.

### 4. Connect your LinkedIn account

Run the setup command in Cowork:

```text
/linkedin-setup
```

Claude will guide you through configuring the LinkedIn Developer applications and credentials required by the plugin.

Depending on the functionality you want to use, you may need:

* **A LinkedIn Developer App with the Marketing Developer Platform product**

  * `rw_ads`
  * `r_ads_reporting`
  * Your LinkedIn Ad Account must be available to the application
* **Your LinkedIn Ad Account ID**
* **A LinkedIn Developer App with the Community Management API product** *(optional, for posting organization content)*

  * `w_organization_social`

LinkedIn API products and permissions are controlled by LinkedIn and may vary depending on your application and account access.

Get your LinkedIn Developer applications from the [LinkedIn Developer Portal](https://www.linkedin.com/developers/apps).

### 5. Start managing campaigns

Once the plugin is installed and your credentials are configured, use the skill by typing `/` in a Cowork conversation or simply describe what you want to accomplish.

Examples:

* *"How are my LinkedIn campaigns performing this week?"*
* *"Show me the campaigns with the highest spend."*
* *"Clone this campaign and update the targeting."*
* *"Pause the underperforming campaigns."*
* *"Update the budget for this campaign."*
* *"Run a full audit of our LinkedIn ad spend."*
* *"Find the LinkedIn organization ID for our company."*
* *"Post this announcement to our company page."*

## How credential storage works

Your tokens are stored in a `.env` file inside the local folder you attached to your Cowork project.

Because this folder lives on your Mac rather than inside the ephemeral Cowork environment, your credentials can persist between Cowork sessions.

```text
~/linkedin-ads/.env
  ├── LINKEDIN_CAMPAIGNS_TOKEN=your_token_here
  ├── LINKEDIN_ACCOUNT_ID=your_account_id
  └── LINKEDIN_POSTS_TOKEN=your_posts_token  (optional)
```

The `.env` file contains sensitive credentials and should never be committed to GitHub.

The repository includes `.gitignore` rules to help prevent credential files from being committed accidentally.

To revoke access, revoke your LinkedIn tokens through the [LinkedIn Developer Portal](https://www.linkedin.com/developers/apps), or remove the local credentials file:

```bash
rm ~/linkedin-ads/.env
```

## Requirements

* A LinkedIn Developer account with the appropriate API products and permissions
* Claude Cowork
* A local folder attached to your Cowork project for credential persistence
* Python 3.8+
* Python `requests` library

Install the Python dependency if required:

```bash
pip install requests
```

## Repository

GitHub repository:

https://github.com/eneelkant/linkedin-ads-manager-claude-plugin

## Security

Never commit:

* LinkedIn API keys
* OAuth access tokens
* `.env` files
* Other sensitive credentials

If credentials are accidentally exposed, revoke them immediately through the LinkedIn Developer Portal and generate new credentials.
