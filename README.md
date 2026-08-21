# LinkedIn Ads Manager — AI Agent for Claude

Manage LinkedIn advertising campaigns through natural language with Claude.

**LinkedIn Ads Manager** is a Claude Cowork plugin that connects your LinkedIn advertising account to an AI-powered workflow for campaign management, performance analysis, targeting, budgets, campaign audits, and LinkedIn organization publishing.

Instead of navigating LinkedIn Campaign Manager for every task, you can ask Claude what you want to accomplish and let the plugin handle the appropriate LinkedIn API operations.

> **Talk to your LinkedIn Ads account like an AI assistant.**

---

## What Is the LinkedIn Ads Claude Plugin?

The **LinkedIn Ads Manager Plugin for Claude** turns Claude into an AI agent for LinkedIn advertising.

It helps marketers, agencies, growth teams, and advertisers work with LinkedIn Ads using conversational instructions.

You can ask Claude to:

- Analyze LinkedIn campaign performance
- Find high-spending campaigns
- Audit advertising accounts
- Create campaigns
- Clone existing campaigns
- Pause or resume campaigns
- Update campaign budgets
- Manage campaign targeting
- Review advertising results
- Investigate campaign performance
- Identify areas that need attention
- Find LinkedIn organization information
- Publish content to a LinkedIn organization page

### Instead of this

```text
Open Campaign Manager
→ Find account
→ Find campaign
→ Open campaign settings
→ Check budget
→ Review performance
→ Export data
→ Analyze results
````

### You can simply ask Claude

```text
Audit my LinkedIn ad account and tell me
which campaigns need attention.
```

Claude can use the connected LinkedIn Ads tools to retrieve the relevant information and help you decide what to do next.

---

# Why Use Claude for LinkedIn Ads?

LinkedIn advertising involves multiple layers of campaign management, targeting, budgets, reporting, and optimization.

The LinkedIn Ads Manager plugin gives Claude access to structured LinkedIn advertising capabilities so you can work conversationally instead of manually navigating the advertising interface.

### Natural-language LinkedIn Ads management

Ask questions such as:

```text
How are my LinkedIn campaigns performing this week?
```

```text
Show me the campaigns with the highest spend.
```

```text
Which campaigns are underperforming?
```

```text
Clone this campaign and change the targeting.
```

```text
Pause the campaigns that are underperforming.
```

```text
Increase the budget for this campaign.
```

```text
Run a complete audit of my LinkedIn ad account.
```

The plugin is designed to make LinkedIn advertising workflows more accessible through an AI agent.

---

# Core Capabilities

## 📊 LinkedIn Ads Performance Analysis

Use Claude to investigate advertising performance and understand where your budget is going.

Typical workflows include:

* Campaign performance analysis
* Spend analysis
* Performance comparisons
* Campaign audits
* Account-level analysis
* Identifying high-spend campaigns
* Identifying underperforming campaigns
* Reviewing campaign results

Example:

```text
Show me my LinkedIn campaigns from the last 30 days
and rank them by spend.
```

---

## 🎯 Campaign Management

Manage the LinkedIn campaign lifecycle through Claude.

Supported workflows include:

* Create campaigns
* Clone campaigns
* Pause campaigns
* Resume campaigns
* Update campaign budgets
* Manage campaign targeting
* Review campaign configuration
* Audit campaigns

Example:

```text
Clone my best-performing LinkedIn campaign
and update the targeting for enterprise companies.
```

---

## 💰 Budget Management

Use Claude to inspect and manage campaign budgets.

Example requests:

```text
Show me the campaigns with the highest daily budgets.
```

```text
Which campaigns are spending the most?
```

```text
Update the budget for this campaign to $100 per day.
```

Budget-changing actions should be treated carefully because they can directly affect advertising spend.

---

## 👥 LinkedIn Campaign Targeting

Analyze and manage campaign targeting through natural language.

Example:

```text
Show me the targeting used by this campaign.
```

```text
Clone this campaign but target marketing managers
instead of the current audience.
```

```text
Review the targeting on my active campaigns.
```

This makes it easier to inspect and iterate on LinkedIn advertising audiences without manually navigating multiple campaign settings.

---

## 🔍 LinkedIn Campaign Audits

One of the primary use cases for the plugin is AI-assisted campaign auditing.

Ask Claude to review your account and surface campaigns that deserve attention.

For example:

```text
Run a full audit of my LinkedIn ad account.
```

Claude can help identify:

* High-spend campaigns
* Weak-performing campaigns
* Budget allocation issues
* Campaigns requiring attention
* Performance differences between campaigns
* Opportunities for further investigation

The plugin is designed to support the analysis workflow rather than blindly making optimization decisions.

---

# LinkedIn Organization Content

The plugin can also support LinkedIn organization publishing when the appropriate Community Management API access is configured.

Example:

```text
Find our LinkedIn organization ID.
```

```text
Post this announcement to our company page.
```

```text
Publish this product update to our LinkedIn organization.
```

This functionality is optional and requires the appropriate LinkedIn API product and permissions.

---

# Available Plugin Components

## Skill

### `linkedin-ads-manager`

The primary LinkedIn advertising skill.

It covers workflows including:

* Campaign creation
* Campaign cloning
* Campaign pausing
* Campaign resuming
* Budget management
* Targeting management
* Performance analysis
* Campaign audits
* LinkedIn organization publishing

---

## Command

### `/linkedin-setup`

Use the setup command to configure your LinkedIn API credentials.

```text
/linkedin-setup
```

Claude will guide you through the required configuration for the functionality you want to use.

---

# Example LinkedIn Ads Workflows

## Campaign Performance

```text
How are my LinkedIn campaigns performing this week?
```

```text
Show me the five campaigns with the highest spend.
```

```text
Which campaigns are performing below expectations?
```

---

## Campaign Auditing

```text
Run a full audit of our LinkedIn advertising account.
```

```text
Find campaigns that deserve attention based on spend
and performance.
```

```text
Give me an executive summary of our LinkedIn Ads performance.
```

---

## Campaign Management

```text
Show me all active campaigns.
```

```text
Clone this campaign.
```

```text
Pause this campaign.
```

```text
Resume this campaign.
```

```text
Update the campaign budget.
```

---

## Targeting

```text
Show me the targeting configuration for this campaign.
```

```text
Clone this campaign with different targeting.
```

```text
Review the targeting across my active campaigns.
```

---

## LinkedIn Organization

```text
Find the LinkedIn organization ID for our company.
```

```text
Post this announcement to our LinkedIn company page.
```

---

# Getting Started

## 1. Create a Local Credential Folder

Create a folder on your Mac for the LinkedIn credentials:

```bash
mkdir -p ~/linkedin-ads
```

This folder is used to persist your LinkedIn credentials between Claude Cowork sessions.

---

## 2. Attach the Folder to Your Cowork Project

In Claude Cowork, attach the folder you created:

```text
~/linkedin-ads
```

The folder is mounted into your Cowork project so the credentials can persist between sessions.

---

## 3. Install the Plugin

The plugin can be installed through Claude Cowork using the GitHub repository.

Open Claude Cowork and:

1. Open **Settings**
2. Select **Plugins**
3. Select **Add Marketplace**
4. Select **Add from repository**
5. Enter:

```text
https://github.com/eneelkant/linkedin-ads-manager-claude-plugin
```

6. Select **Sync**
7. Find **LinkedIn Ads Manager**
8. Select **Install**

Once installed, the LinkedIn Ads Manager plugin will be available in Claude Cowork.

---

# Connect Your LinkedIn Account

After installing the plugin, run:

```text
/linkedin-setup
```

Claude will guide you through the configuration process.

Depending on which capabilities you want to use, you may need the following.

## LinkedIn Marketing Developer Platform

For LinkedIn advertising functionality, your LinkedIn Developer application may require access to:

```text
rw_ads
r_ads_reporting
```

Your LinkedIn Ad Account must also be available to the application.

You will also need:

```text
LinkedIn Ad Account ID
```

---

## LinkedIn Community Management API

Organization publishing is optional.

If you want to publish content to a LinkedIn organization page, the application may require:

```text
w_organization_social
```

LinkedIn API products, permissions, and application access are controlled by LinkedIn and may vary depending on your account and application.

Create and manage your LinkedIn Developer applications through the [LinkedIn Developer Portal](https://www.linkedin.com/developers/apps).

---

# Credential Storage

The plugin uses a local `.env` file to store the credentials required by the configured LinkedIn workflows.

A typical setup looks like:

```text
~/linkedin-ads/
└── .env
```

Example:

```text
LINKEDIN_CAMPAIGNS_TOKEN=your_token_here
LINKEDIN_ACCOUNT_ID=your_account_id
LINKEDIN_POSTS_TOKEN=your_posts_token
```

The posts token is optional and is only required for supported LinkedIn organization publishing workflows.

---

# Protect Your Credentials

Your `.env` file contains sensitive credentials.

**Never commit it to GitHub.**

Do not publish:

* OAuth access tokens
* API credentials
* LinkedIn campaign tokens
* LinkedIn account IDs combined with private credentials
* `.env` files
* Other authentication secrets

If credentials are accidentally exposed, revoke them through the LinkedIn Developer Portal and generate new credentials.

To remove your local credential file:

```bash
rm ~/linkedin-ads/.env
```

---

# Requirements

You need:

* Claude Cowork
* A LinkedIn Developer account
* A LinkedIn Developer application
* Appropriate LinkedIn API products and permissions
* A LinkedIn Ad Account
* A local folder attached to your Cowork project
* Python 3.8+
* Python `requests`

Install the Python dependency if required:

```bash
pip install requests
```

---

# How the Plugin Works

The plugin connects Claude's conversational interface with LinkedIn's APIs.

```text
┌──────────────────────┐
│        You           │
│ Natural language     │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│       Claude         │
│     AI Agent         │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ LinkedIn Ads Manager  │
│       Plugin          │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│    LinkedIn APIs     │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ LinkedIn Ad Account  │
└──────────────────────┘
```

Claude interprets your request and uses the plugin's available capabilities to interact with your LinkedIn advertising environment.

---

# AI Agent for LinkedIn Ads

The plugin is designed around a simple idea:

> **Your advertising platform should be something you can talk to.**

Instead of learning every navigation path inside LinkedIn Campaign Manager, you can describe the outcome you want.

For example:

```text
I want to understand where we're wasting LinkedIn
ad spend this month.
```

Claude can investigate campaign performance and help identify areas that require attention.

You can then continue the conversation:

```text
Show me the campaigns responsible for most of that spend.
```

Then:

```text
Compare their performance.
```

And finally:

```text
Clone the strongest campaign and change the targeting.
```

This conversational workflow makes Claude useful as an **AI assistant and agent for LinkedIn advertising operations**.

---

# Use Cases

## PPC & Paid Social Managers

Analyze LinkedIn campaigns without manually navigating through multiple reporting screens.

## B2B Marketers

Use Claude to investigate LinkedIn advertising performance and campaign structure.

## Growth Teams

Combine campaign analysis with broader marketing workflows and decision-making.

## Marketing Agencies

Use conversational workflows to review and manage LinkedIn advertising accounts.

## Performance Marketers

Quickly investigate spend, campaigns, budgets, targeting, and performance.

## Marketing Automation Specialists

Use the plugin as an AI-powered interface for LinkedIn advertising workflows.

---

# Security Considerations

LinkedIn API access is controlled by the permissions granted to your Developer application.

Only configure the API products and permissions required for your use case.

The plugin does not bypass LinkedIn permissions or account-level access controls.

### Important

Actions that modify campaigns, budgets, or other advertising resources can have financial consequences.

Review important changes before executing them, especially:

* Campaign launches
* Budget increases
* Campaign status changes
* Targeting changes
* Campaign cloning

You remain responsible for the advertising actions performed through your LinkedIn account.

---

# Troubleshooting

## Plugin cannot access my LinkedIn account

Run:

```text
/linkedin-setup
```

and verify that your credentials and account ID are configured correctly.

Also verify that your LinkedIn Developer application has the required API products and permissions.

---

## Campaign data is unavailable

Check:

* LinkedIn Ad Account ID
* OAuth token
* Application permissions
* Ad Account access
* LinkedIn API product access

LinkedIn controls access to its APIs and may require approval for certain products or permissions.

---

## Organization publishing does not work

Verify that:

```text
w_organization_social
```

is available to your LinkedIn Developer application and that the authenticated account has the necessary organization permissions.

---

# Repository

GitHub:

[https://github.com/eneelkant/linkedin-ads-manager-claude-plugin](https://github.com/eneelkant/linkedin-ads-manager-claude-plugin)

---

# Project Status

This project is actively developed.

LinkedIn API capabilities, permissions, endpoints, and access requirements can change over time. Some functionality may require LinkedIn approval or specific account access.

---

# Contributing

Contributions, bug reports, feature requests, and improvements are welcome.

If you find an issue with the plugin, please open an issue in the GitHub repository.

When reporting API-related problems, include:

* The affected workflow
* The LinkedIn API capability involved
* The error message
* Relevant configuration details without exposing credentials

**Never include OAuth tokens or private credentials in an issue.**

---

# License

See the repository's license file for licensing information.

---

# SEO Keywords

LinkedIn Ads Claude plugin · LinkedIn Ads AI agent · Claude LinkedIn Ads · Claude Cowork LinkedIn Ads · LinkedIn advertising AI · LinkedIn Ads automation · LinkedIn campaign management · LinkedIn Ads manager · LinkedIn Ads reporting · LinkedIn Ads optimization · LinkedIn marketing automation · LinkedIn campaign automation · AI agent for LinkedIn Ads · LinkedIn advertising assistant · Claude AI marketing assistant · LinkedIn PPC automation · B2B advertising AI · LinkedIn Campaign Manager AI
