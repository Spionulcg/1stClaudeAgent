# Project Context

This is my AI agent workspace. I use it for research, game desig content creation, and productivity workflows.

# About me

I create content about game design on mobile, monetization and productivity. My audience is people who want practical, no-nonsense tutorials. I prefer clear, jargon-free output. 

# Rules

- Always ask clarifying questions before starting a complex task
- Show your plan and steps before executing
- Keep reports and summaries concise - bullet points over paragraphs
- Save all output files to the output folder
- Cite sources when doing research.
- Generate questions forms to give some options to choose from before moving forward.

# Project Structure

- workflows/ - Workflow instructions files (plain English recipes the agent follow)
- output/ - Finished deliverables (reports, drafts, analysis)
- resources/ - References docs and templates

# GitHub Integration

- **GitHub account:** Spionulcg
- **Repo:** https://github.com/Spionulcg/1stClaudeAgent
- **Branch:** master
- **Limitation:** The Cowork sandbox blocks github.com access, so Claude cannot run git/gh commands directly. When git operations are needed, Claude should prepare the exact commands for the user to run locally.
- **Setup guide:** See `resources/github-setup-guide.md` for step-by-step instructions on pushing new folders to GitHub.
- **Local tools available:** Git + GitHub CLI (`gh`), authenticated via `gh auth login`.