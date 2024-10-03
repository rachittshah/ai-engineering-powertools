# Compound AI Systems Tools
This is a dev tools garage for building Compound AI Systems. Expect breaking releases. 

## Ideas: [#1](https://github.com/NirantK/dspy-tools/issues/1)

AI Audit Tool
Overview
The AI Audit Tool is designed to perform rapid, deep, and insightful AI audits for clients. Leveraging existing Standard Operating Procedures (SOPs), meeting transcripts, and other collected files, the tool generates comprehensive reports, visualizes workflows using Mermaid diagrams, and offers automation suggestions utilizing Large Language Models (LLMs). The primary goal is to streamline the AI auditing process, minimize human effort, and potentially offer the service at a low or no cost by automating significant portions of the workflow.

Objectives
Automate AI Auditing: Utilize AI models like OpenAI's GPT-4 and Anthropic's Claude to automate the AI audit process.
Workflow Visualization: Convert SOPs and transcripts into structured Mermaid diagrams representing current and optimized workflows.
Automation Suggestions: Provide actionable recommendations for process optimization and automation using LLMs.
Cost Reduction: Decrease the effort and cost required for AI audits, aiming to offer the service for free or at minimal cost.
Scalability: Develop a tool that can be scaled and reused for multiple clients with minimal adjustments.
Key Features
Data Ingestion:

Import and process various data sources including SOPs, meeting transcripts (e.g., SRT files from Fireflies), and notes.
Support for multiple file formats and seamless integration with data collection tools.
Mermaid Diagram Generation:

Use AI models to parse textual information and generate visual workflow diagrams.
Represent both existing processes and proposed AI-enhanced processes.
Automation Recommendations:

Analyze workflows to identify areas where AI and automation can be implemented.
Provide suggestions within diagrams and reports for using LLMs and other AI technologies.
Report Generation:

Compile findings into a comprehensive, client-ready AI audit report.
Include visual diagrams, identified opportunities, and actionable next steps.
Integration with Existing Tools:

Utilize Fireflies API for meeting transcript export.
Leverage DSPy for prompt building and workflow automation.
Collaboration and Version Control:

Host the project on GitHub under the repository ai-engineering-powertools.
Encourage collaborative development and contributions.
Technical Requirements
Programming Language: Python 3.x
AI Models:
OpenAI GPT-4 (referred to as 'o1' in conversations)
Anthropic's Claude (noted for better Mermaid diagram generation)
Libraries and Frameworks:
Mermaid.js for diagram creation
DSPy for prompt management
APIs:
Fireflies API for data export
OpenAI and Anthropic API access keys
Data Storage:
Support for storing and retrieving client data securely
Environment Setup:
Repository cloning and environment setup instructions
Dependency management via requirements.txt
Milestones and Timeline
Week 1-2:

Set up the development environment.
Clone the repository and install necessary dependencies.
Integrate Fireflies API for transcript export.
Week 3-4:

Develop data ingestion and preprocessing scripts.
Implement AI models for initial data analysis.
Week 5-6:

Create functionality for generating Mermaid diagrams from SOPs and transcripts.
Validate diagram accuracy with sample data.
Week 7-8:

Integrate automation suggestion capabilities using LLMs.
Refine the process for providing actionable recommendations.
Week 9-10:

Develop report generation module to compile findings.
Ensure the report is client-ready with professional formatting.
Week 11-12:

Conduct testing with real client data (as permitted).
Optimize for speed and scalability.
Week 13 onwards:

Gather feedback from stakeholders (e.g., Sudip).
Enhance the tool based on feedback and prepare for deployment.
Dependencies and Assumptions
Access to AI Models: Valid API keys and sufficient usage quotas for OpenAI and Anthropic models.
Data Availability: Clients provide necessary SOPs, transcripts, and other relevant documents.
Compliance: Adherence to data privacy laws and regulations when handling client data.
Team Collaboration: Contributors have experience with AI models, data processing, and software development.
Risks and Mitigation
Data Privacy Concerns: Ensure all client data is handled securely with appropriate anonymization where necessary.
Model Limitations: AI models may produce inaccurate or nonsensical outputs; include human oversight for validation.
API Rate Limits: Monitor usage to prevent exceeding API limits; consider batching requests or using multiple keys.
Project Scope Creep: Stick to defined objectives to prevent delays; prioritize features based on client impact.
Success Metrics
Efficiency: Reduction in time taken to perform AI audits compared to manual processes.
Cost Reduction: Lower operational costs enabling potential free service offerings.
Client Satisfaction: Positive feedback from clients on the usefulness and quality of the AI audit reports.
Scalability: Ability to handle multiple clients concurrently without degradation in performance.
Future Enhancements
Automated Client Onboarding: Streamline the process for collecting client data and initiating audits.
Enhanced Visualizations: Incorporate more advanced diagramming tools or interactive dashboards.
Additional AI Capabilities: Expand to include other AI transformation areas beyond content creation and support.
Open Source Contributions: Encourage community involvement to improve and expand the tool's capabilities.
README

AI Audit Tool
An AI-powered solution to perform rapid, deep, and insightful AI audits by processing SOPs, meeting transcripts, and other relevant documents to generate comprehensive reports and workflow diagrams with automation suggestions.

Overview
The AI Audit Tool automates the AI auditing process by:

Ingesting Data: Importing SOPs, meeting transcripts, and notes.
Visualizing Workflows: Converting textual information into Mermaid diagrams.
Generating Recommendations: Providing automation suggestions using Large Language Models (LLMs).
Creating Reports: Compiling findings into client-ready AI audit reports.
Features
Data Ingestion and Processing
Supports various file formats (e.g., .docx, .pdf, .srt).
Integrates with Fireflies API for meeting transcript exports.
Mermaid Diagram Generation
Transforms SOPs and transcripts into visual workflow diagrams.
Utilizes AI models for accurate and efficient parsing.
Automation Suggestions
Identifies areas for AI and automation implementation.
Provides actionable recommendations within diagrams.
Report Generation
Compiles data, diagrams, and suggestions into a cohesive report.
Outputs in formats suitable for client presentations.
Getting Started
Prerequisites
Python 3.8 or higher
API Keys:
OpenAI GPT-4 API key
Anthropic Claude API key
Fireflies API key (if using transcript export)
Git
Installation
Clone the Repository

bash
Copy code
git clone https://github.com/NirantK/ai-engineering-powertools.git
Navigate to the Project Directory

bash
Copy code
cd ai-engineering-powertools
Create a Virtual Environment (Optional but Recommended)

bash
Copy code
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
Install Dependencies

bash
Copy code
pip install -r requirements.txt
Configuration
Set API Keys

Create a .env file in the root directory and add your API keys:

env
Copy code
OPENAI_API_KEY=your_openai_api_key
CLAUDE_API_KEY=your_anthropic_api_key
FIREFLIES_API_KEY=your_fireflies_api_key
Ensure SOPs and Transcripts are Available

Place all SOP documents and transcript files in the data/ directory.

Usage
Prepare Input Data

Ensure all relevant files are in the data/ directory.
Supported formats include .docx, .pdf, .txt, .srt.
Run the Main Script

bash
Copy code
python main.py
The script will process the input data, generate diagrams, and compile the report.
Progress and logs will be displayed in the console.
Access Output Files

Diagrams: Located in outputs/diagrams/
Audit Report: Located in outputs/reports/ai_audit_report.pdf
Project Structure
data/: Input directory for SOPs and transcripts.
outputs/: Contains generated diagrams and reports.
diagrams/: Mermaid diagrams in .md and image formats.
reports/: Final AI audit reports.
src/: Source code files.
data_processing.py: Functions for data ingestion and preprocessing.
diagram_generator.py: Contains logic for generating Mermaid diagrams.
automation_recommender.py: Module for providing automation suggestions.
report_compiler.py: Assembles the final report.
main.py: Orchestrates the execution flow.
requirements.txt: Lists all Python dependencies.
.env: Environment file for API keys (not included in the repository for security).
Contributing
We welcome contributions! Here's how you can help:

Fork the Repository

Click the "Fork" button on the top right of the repository page.

Clone Your Fork

bash
Copy code
git clone https://github.com/your_username/ai-engineering-powertools.git
Create a Branch

bash
Copy code
git checkout -b feature/your_feature_name
Make Changes and Commit

bash
Copy code
git add .
git commit -m "Add your message here"
Push to Your Fork

bash
Copy code
git push origin feature/your_feature_name
Submit a Pull Request

Go to the original repository and submit a pull request.

License
This project is licensed under the Apache License 2.0. See the LICENSE file for details.

Contact
Project Lead: Nirant (@NirantK)
Contributor: Rachitt Shah (@RachittShah)
For any questions or support, please open an issue or reach out directly via GitHub.

Future Work
UI Development

Transition from a command-line interface to a user-friendly web or desktop application.

Enhanced AI Models

Explore integrating additional AI models for improved accuracy and capabilities.

Client Portal

Develop a portal where clients can upload data and receive reports directly.

Acknowledgments
OpenAI and Anthropic

For providing powerful AI models that make this tool possible.

Fireflies

For their API and services in meeting transcription.

