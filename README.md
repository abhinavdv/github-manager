Built end-to-end using Cursor. 0 lines of code actually written

# GitHub Manager

A web application to intelligently break down project requirements into GitHub issues.

## Features

- **Voice Input**: Record and transcribe your project requirements directly through your microphone
- **Interactive Step-by-Step Process**: Guide users through a structured workflow
- **Intelligent Text Analysis**: Analyze project requirements using Azure AI and OpenAI LLM
- **AI-Powered Goal Generation**: Leverage Azure OpenAI to intelligently create project goals
- **Goal Breakdown**: Break big goals into smaller, actionable tasks using AI
- **GitHub Integration**: Create repositories and issues automatically
- **Tree Visualization**: View your project structure in an intuitive hierarchical tree format
- **Graph Visualization**: Alternative visualization showing relationships between tasks
- **Real-time Feedback**: Loading indicators and progress updates during processing
- **Responsive UI**: Works on desktop and mobile devices
- **Dark Mode Support**: Easy on the eyes during late-night planning sessions
- **Local Storage**: Save your progress and continue later
- **Editable Goals**: Modify AI-generated tasks to fit your exact requirements
- **Step Navigation**: Easily move between different stages of your project planning

## User Journeys

### 1. Meeting Note Taker & PBI Creator

**Scenario**: Product team meeting to discuss new feature requirements

1. During the meeting, the team discusses requirements for a new feature
2. The scrum master opens GitHub Manager and uses voice recording to capture the conversation
3. After the meeting, the transcribed text is automatically analyzed to identify high-level tasks
4. The application breaks these down into specific, actionable Product Backlog Items (PBIs)
5. The scrum master reviews and adjusts the PBIs as needed
6. With a single click, a new GitHub repository is created with all PBIs as issues
7. The team can immediately start development with a well-organized backlog

### 2. Solo Developer Project Kickoff

**Scenario**: Independent developer starting a new side project

1. Developer has a new app idea but struggles to organize where to begin
2. They input their app concept through text or voice into GitHub Manager
3. The application analyzes the requirements and generates structured high-level goals
4. Each goal is automatically broken down into smaller, achievable tasks
5. The developer reviews the generated hierarchy in the tree visualization
6. They adjust any tasks that don't match their vision
7. GitHub Manager creates a new repository with all the tasks as issues
8. The developer can now start coding with a clear roadmap

### 3. Technical Documentation Creation

**Scenario**: Technical writer creating documentation for a complex system

1. The technical writer interviews engineers about a system that needs documentation
2. They record the conversation through GitHub Manager's voice input
3. The system transcribes and analyzes the technical details
4. GitHub Manager generates a hierarchical structure of documentation topics
5. The writer reviews the tree view to ensure the documentation structure is logical
6. They modify headings and descriptions to match documentation standards
7. A repository is created with issues representing each documentation section
8. The writing team can now collaborate efficiently with a clear documentation plan

## Architecture

- **Backend**: Python with Flask
- **Frontend**: HTML, CSS, JavaScript
- **APIs**: GitHub API, Azure AI Text Analytics API, Azure OpenAI API

## Setup Instructions

### Prerequisites

- Python 3.7 or higher
- GitHub account with personal access token
- Azure account with Text Analytics resource
- Azure OpenAI Service or equivalent

### Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/github-manager.git
   cd github-manager
   ```

2. Install backend dependencies:
   ```
   cd backend
   pip install -r requirements.txt
   ```

3. Configure environment variables:
   ```
   cp .env.example .env
   ```
   Then edit `.env` to add your GitHub token and Azure credentials.

4. Run the application:
   ```
   python app.py
   ```

5. Access the application at http://localhost:5000

## Usage Flow

1. **Enter Project Instructions**: Provide a detailed description of your project.
2. **Review Big Goals**: Analyze and adjust the main project goals (generated by Azure OpenAI).
3. **Review Small Goals**: Break down each big goal into smaller, actionable tasks (generated by Azure OpenAI).
4. **Create Repository**: Set up a new GitHub repository for your project.
5. **Create Issues**: Generate GitHub issues for each of the small goals.

## Development

### Project Structure

```
github-manager/
├── backend/
│   ├── services/
│   │   ├── azure_service.py
│   │   ├── github_service.py
│   │   └── __init__.py
│   ├── static/
│   │   ├── css/
│   │   │   └── styles.css
│   │   └── js/
│   │       └── app.js
│   ├── templates/
│   │   └── index.html
│   ├── app.py
│   ├── requirements.txt
│   └── .env.example
└── README.md
```

## License

MIT

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
