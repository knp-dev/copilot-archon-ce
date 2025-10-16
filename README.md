# Copilot Archon Context Engineering

A development framework that streamlines software projects through structured prompts and intelligent task management.
This template project is an adaptation of claude workflows found in [Archon](https://github.com/coleam00/Archon) repo. It can be used as base of any development project.

## Overview

The Copilot Archon Context Engineering framework enhances development productivity through intelligent task management and research capabilities that integrate with the Archon MCP server. The system is designed to be used directly with GitHub Copilot Chat through structured prompts and instructions.

## Using Workflows with GitHub Copilot Chat

The system works through GitHub Copilot Chat with structured prompts and workflows. Prompts are located in the `.github/prompts/` folder and can be referenced in chat:

### Key Prompts

1. **Create Plan Prompt** - Transform requirements into implementation plans
   - Use in chat: `/create-plan`
   - Provide your requirements document when prompted

2. **Execute Plan Prompt** - Execute development plans with task tracking
   - Use in chat: `/execute-plan`
   - Provide your plan document when prompted

3. **Primer Prompt** - Set up project context
   - Use in chat: `/primer`
   - Useful for new projects or when switching contexts

### Usage Examples

Use the prompts in GitHub Copilot Chat:

```
User: Use /create-plan to create a plan for user authentication

[Copilot executes the prompt and creates a comprehensive plan]

User: Use /execute-plan to implement the plan

[Copilot executes the plan with full task management]
```

## Project Structure

```
copilot-archon-ce/
├── .github/                      # GitHub configuration
│   ├── chatmodes/                # Custom Copilot chat modes
│   ├── prompts/                  # Structured workflow prompts
│   │   ├── create-plan.prompt.md # Requirements-to-plan workflow
│   │   ├── execute-plan.prompt.md# Plan execution workflow
│   │   └── primer.prompt.md      # Project context workflow
│   └── copilot-instructions.md   # Core Copilot instructions
├── .vscode/
│   └── mcp.json                  # MCP server configuration
├── .gitignore                    # Git ignore configuration
├── INITIAL.md                    # Project initialization file
├── LICENSE                       # Project license
└── README.md                     # This file
```

## Archon Integration

The prompt workflows automatically handle Archon MCP server integration through the configured setup in `.vscode/mcp.json` for:

- **Task Management**: Creating and tracking development tasks
- **Knowledge Management**: Research capabilities for informed implementation  
- **Project Organization**: Structured approach to managing projects

You don't need to manually call Archon functions - the prompt workflows handle this for you.

## Getting Started

1. **Configure MCP**: Ensure Archon MCP server is properly configured in `.vscode/mcp.json`
2. **Initialize your project**: Create an `INITIAL.md` file with basic project information
3. **Create a plan**: Use `/create-plan.prompt.md` with your requirements
4. **Execute the plan**: Use `/execute-plan.prompt.md` to implement with full task tracking

## Example Workflow

```
1. User provides requirements for a new feature
2. User runs: /create-plan
3. System creates comprehensive implementation plan
4. User reviews and approves the plan
5. User runs: /execute-plan
6. System implements the feature with:
   - Automatic task creation and tracking
   - Research-driven implementation
   - Built-in testing and validation
   - Progress reporting
```

## Best Practices

- Always start with `/create-plan.prompt.md` for new features
- Provide clear, specific requirements in your initial request
- Review the generated plan before execution with `/execute-plan.prompt.md`
- Let the prompts handle task management automatically
- Use the research capabilities built into the prompts

## Configuration

The system uses several key configuration files:

- **`.vscode/mcp.json`**: MCP server configuration for Archon integration
- **`.github/copilot-instructions.md`**: Core instructions for GitHub Copilot behavior
- **`.github/prompts/`**: Structured workflow prompts for development processes
- **`.github/chatmodes/`**: Custom chat modes for specialized scenarios

---

*For detailed workflow prompts, see the files in `.github/prompts/`.*
*For Archon integration details, see `.github/copilot-instructions.md`.*