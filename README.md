# 📋 MeetBrief AI – Intelligent Meeting Preparation Assistant

## Overview

MeetBrief AI is an AI-powered meeting preparation assistant that helps users prepare for professional meetings through automated research, intelligent analysis, and structured report generation.

Users can enter a company or person's name, select a meeting date, and provide the meeting context. The application researches relevant information using Tavily, processes the findings through a Gemini model accessed via the Bifrost AI gateway, and generates a downloadable PDF meeting brief.

## Problem Statement

Preparing for important meetings often involves time-consuming research, gathering relevant information, identifying potential opportunities and risks, and planning meaningful discussion points.

MeetBrief AI simplifies this process by combining automated web research, AI-powered analysis, and PDF report generation into a single application.

## Key Features

- **Automated Research:** Retrieves relevant company or person information, recent developments, opportunities, and risks using Tavily.
- **Context-Based Analysis:** Uses the user's meeting context to generate relevant and focused insights.
- **AI-Powered Meeting Brief:** Generates structured meeting preparation reports using a Gemini model through the Bifrost AI gateway.
- **Discussion Questions:** Suggests important questions to help users conduct productive meetings.
- **Meeting Strategy:** Provides suggested approaches and key takeaways.
- **PDF Report Generation:** Converts the generated meeting brief into a downloadable PDF.
- **Research Source Links:** Displays links to available research sources for further verification.
- **Session-Based Caching:** Reuses previously generated research and analysis for identical meeting details, reducing unnecessary API requests.
- **Error Handling:** Handles API failures, connection issues, timeouts, and usage limits.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core application development |
| Streamlit | Interactive web application interface |
| Tavily API | Automated web research |
| Bifrost AI Gateway | OpenAI-compatible AI API integration |
| Gemini Model | AI-powered meeting brief generation |
| OpenAI Python SDK | Communication with the Bifrost gateway |
| ReportLab | PDF report generation |
| Requests | HTTP communication and error handling |
| Python-dotenv | Environment variable management |

## How It Works

1. **User Input:** Enter the company or person's name, meeting date, and meeting context.
2. **Research:** Tavily searches for relevant information and returns research results.
3. **AI Analysis:** The collected research is passed to a Gemini model through Bifrost.
4. **Brief Generation:** The AI generates a structured report containing:
   - Company or Person Overview
   - Recent Developments
   - Important Opportunities
   - Potential Risks and Challenges
   - Important Discussion Questions
   - Suggested Meeting Strategy
   - Key Takeaways
5. **PDF Generation:** The meeting brief is converted into a PDF report.
6. **Results:** Users can view the briefing, access research links, and download the PDF.

## Project Structure

```text
MeetBrief-AI/
│
├── app.py
├── ai_analysis.py
├── research.py
├── pdf_generator.py
├── requirements.txt
├── .gitignore
└── README.md
```

## Installation and Setup

### Prerequisites

- Python 3.10 or later
- pip package manager
- Tavily API key
- Bifrost AI gateway access and a configured Gemini model

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd MeetBrief-AI
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file in the root directory and configure the following variables:

```env
TAVILY_API_KEY=your_tavily_api_key
BIFROST_API_KEY=your_bifrost_virtual_key
BIFROST_MODEL_NAME=your_configured_gemini_model
BIFROST_BASE_URL=http://localhost:8080
```

**Note:**
- Obtain the Tavily API key from the Tavily platform.
- Configure Bifrost and obtain a valid virtual key.
- Set `BIFROST_MODEL_NAME` to the exact Gemini provider/model identifier enabled for your Bifrost virtual key.
- Ensure the Bifrost gateway is running and accessible at the configured base URL.
- Update `BIFROST_BASE_URL` if your gateway runs at a different address.

Never commit or share your `.env` file or API credentials.

### 5. Run the Application

```bash
streamlit run app.py
```

The application will launch in your default web browser.

## Future Enhancements

- Calendar integration for automated meeting preparation.
- Meeting history and saved report management.
- Support for multiple meeting participants.
- Customizable meeting briefing templates.
- Enhanced research filtering and source verification.
- Automated reminders before scheduled meetings.

## Project Objective

MeetBrief AI aims to make meeting preparation faster and more effective by combining web research, generative AI, and automated report generation.

---

**MeetBrief AI – Research Smarter. Prepare Better. Meet Confidently.**