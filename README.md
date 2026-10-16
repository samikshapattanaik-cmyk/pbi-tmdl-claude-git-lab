# 📊 Power BI Code-First Analytics Lab: TMDL, Git, and Claude AI

An experimental workspace and demonstration project exploring a modern, code-first workflow for Power BI. This repository replaces traditional monolithic, binary `.pbix` files with human-readable **TMDL (Tabular Model Definition Language)**, local **Git version control**, and automated AI-assisted measure development via **Claude Desktop (Model Context Protocol / MCP)**.

---

Human-Readable Models (PBIP & TMDL): Tables, relationships, and DAX measures live as plain text files (.tmdl) in VS Code instead of a locked binary container.

AI Co-Pilot Integration: Claude Desktop connects directly to the local project via MCP, allowing you to prompt natural-language requests for DAX code, formatting, and display folder organization.

Local Version Control: Track exact, line-by-line model and measure updates (git diff) before committing or pushing to GitHub.

Live Desktop Sync: Save changes in VS Code or via Claude, click Refresh in Power BI Desktop, and watch your semantic model update instantly.

--------------------------------

Prerequisites & Tooling
-----------------------------------
To run and experiment with this workflow, ensure you have the following installed:

Power BI Desktop (with Developer Preview enabled for saving as .pbip)

Visual Studio Code (with the TMDL extension recommended)

Git (for local and remote version control)

Claude Desktop configured with the Model Context Protocol (powerbi-modeling-mcp)

Quickstart Guide
----------------------------------
1. Clone the Repository
Bash
git clone [https://github.com/samikshapattanaik-cmyk/pbi-tmdl-claude-git-lab.git](https://github.com/samikshapattanaik-cmyk/pbi-tmdl-claude-git-lab.git)
cd pbi-tmdl-claude-git-lab
2. Open in Power BI Desktop
Double-click web_analytics.pbip to open the workspace natively in Power BI Desktop.

3. Edit via VS Code or Claude AI
Open the project folder in VS Code.

Edit .tmdl files directly under web_analytics.SemanticModel/definition/tables/, or prompt Claude Desktop to write measures and organize them into display folders.

Save your files in VS Code.

4. Sync & View in Power BI
Go back to Power BI Desktop and click Refresh on the notification banner to load the updated TMDL definitions in real time.

5. Track and Commit Changes
Open your terminal in VS Code to stage and commit your model updates:

Bash
git status
git add .
git commit -m "feat(tmdl): update semantic model definitions via Claude MCP"
git push origin main

💡 Why Code-First Power BI?
---------------------
Clean Code Reviews: Review exact DAX formula changes line-by-line in Pull Requests rather than dealing with binary diff failures.

AI Leverage: Seamlessly integrate AI agents to handle repetitive boilerplate, DAX formatting, and folder structuring.

Robust Backup & History: Never lose track of who edited a measure or when a breaking change was introduced.

🤝 Contributing & Feedback
----------------
Feel free to fork this repository, open issues, or submit pull requests if you have ideas for optimizing TMDL structures or MCP agent workflows!

pbi-tmdl-claude-git-lab/
├── web_analytics.Report/            # Report visuals, layout, and page definitions (JSON)
│   └── definition/                  
├── web_analytics.SemanticModel/     # Power BI Semantic Model definitions
│   └── definition/
│       ├── tables/                  # Table schemas & DAX measures (.tmdl)
│       └── model.tmdl               # Model relationships and culture settings
├── .gitignore                       # Ignores local user settings and cache files (.pbi/)
└── README.md                        # Project documentation

<img width="1280" height="720" alt="GItpowerBi-ezgif com-video-to-gif-converter" src="https://github.com/user-attachments/assets/788a1d64-0d3c-43e2-aa40-be4ad8eecd50" />

