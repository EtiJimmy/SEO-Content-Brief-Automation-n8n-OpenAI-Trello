# SEO-Content-Brief-Automation-n8n-OpenAI-Trello

This workflow automatically transforms a keyword from a Google Sheet into a full SEO content brief and sends it to Trello — no copying, pasting, or manual brief creation.

## What It Does

This workflow automates the creation of SEO content briefs, reducing the time spent on manual research and formatting.

# It:

- Listens for new keywords in a shared Google Sheet.

- Formats the data for predictable downstream processing.

- Uses OpenAI to generate:

  - Related keywords

  - Target audience

 - Topic and heading ideas

 - Suggested subtopics

 - Creates a Trello card with the entire brief in the description, ready for writers to use.

## Workflow Overview
<img width="1232" height="484" alt="Screenshot 2025-08-12 at 13 38 17" src="https://github.com/user-attachments/assets/5246f7ab-42bd-42ab-87e6-c83e11ea4842" />


- Google Sheets Trigger: Watches for new rows (keywords).

- Set Node: Cleans/formats the keyword data.

- HTTP → OpenAI Node: Sends the keyword to GPT, which:

- Suggests additional related keywords

- Creates a structured content brief with headings and topics

- Trello Node: Posts the generated brief into a “To Write” list in Trello.

## Why This Is Useful

- Instant Briefs – No waiting for manual keyword research.

- Better Handoffs – Writers get everything they need in one place.

- Trackable Process – All briefs are logged in Trello for review.

## Possible Enhancements

While this version uses OpenAI to brainstorm and expand keywords, you could make it more data-driven by connecting an SEO API (e.g., Ahrefs, SEMrush, Google Keyword Planner) to pull:
Search volume, Competition level, Click potential. That would result in even more accurate, intent-driven briefs.

## Example Use Case/ Trello Output
<img width="1082" height="691" alt="Screenshot 2025-08-12 at 14 25 46" src="https://github.com/user-attachments/assets/d068f9b7-6bb2-4fe3-a664-1f174ae0ab67" />


Scenario:
Your marketing team shares a Google Sheet for keyword ideas. Once someone adds "Online Alcohol Delivery in Lagos", the workflow:

Picks up the keyword

Sends it to OpenAI for related terms and a content plan

Posts a Trello card like:

**SEO Content Brief: Online Alcohol Delivery in Lagos**

**Target Audience:**

Urban professionals in Lagos who are tech-savvy and prefer convenience in their shopping experience.

Party planners or individuals hosting events who need quick and reliable alcohol delivery services.

People looking for a wide selection of alcoholic beverages with the convenience of ordering online.

**Main Topics to Cover:**

Introduction to online alcohol delivery services in Lagos

Benefits of using online alcohol delivery services

How online alcohol delivery works in Lagos

Popular alcohol delivery services in Lagos

Different types of alcoholic beverages available for delivery

**Suggested Headings:**

Exploring the Convenience of Online Alcohol Delivery in Lagos

Top Reasons to Choose Online Alcohol Delivery Services

Expert Tips for a Seamless Online Alcohol Ordering Experience

**Keywords to Use:**

Online alcohol delivery Lagos

Alcohol delivery services in Lagos

Order alcohol online Lagos

Alcohol delivery near me

Best online liquor store Lagos

Convenient alcohol delivery Lagos

**Note**
Ensure the content is informative, engaging, and optimized for the target audience's search intent. Incorporate local references and highlight the unique aspects of online alcohol delivery services in Lagos to attract and engage the audience effectively.


**Requirements**
- n8n

- Google Sheets API access

- Trello API access

- OpenAI API key (or alternative SEO API)
