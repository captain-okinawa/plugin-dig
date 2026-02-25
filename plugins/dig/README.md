# dig

Clarify ambiguities in plans with structured questions using the AskUser tool.

## Overview

This plugin helps analyze the current plan or discussion, identify unclear points, and ask structured questions to clarify requirements before implementation. It is ported from the [Claude Code dig plugin](https://github.com/fumiya-kume/claude-code/tree/master/dig) to work with Cursor.

## Installation

### From Local Repository

If you have this plugin in your local project:

1. Open Cursor Settings
2. Navigate to Plugins
3. Add this plugin directory: `plugins/dig`

### From Marketplace (Future)

Once published to the Cursor Marketplace:

```
cursor://plugin/install?name=dig
```

## Usage

Simply invoke the command:

```
/dig
```

The plugin will:
1. Read your current plan files (CLAUDE.md, prd.md, README.md, etc.)
2. Identify ambiguities across multiple categories (Architecture, Data, API, UI/UX, Testing, DevOps, Scope)
3. Generate 2-4 structured questions with concrete options including pros/cons
4. Process your answers and output decisions and next steps
5. Revisit the plan and continue until all unclear points are resolved

## Features

- **Automatic Context Loading**: Reads project files to understand current state
- **Structured Questions**: Generates multiple-choice questions with 2-4 options each
- **Pros/Cons Analysis**: Each option includes brief pros and cons
- **Iterative Clarification**: Continues asking until all ambiguities are resolved
- **Decision Summary**: Outputs clear decisions table and next steps after each round

## How it Works

### Phase 1: Clarify Unclear Points
The plugin analyzes your current plan and identifies ambiguous or underspecified areas.

### Phase 2: Generate Questions
Creates 2-4 structured questions using the AskUser tool:
- Each question has 2-4 concrete options
- Each option includes pros/cons
- Aligned with existing project patterns (if CLAUDE.md exists)

### Phase 3: Post-Answer Processing
After receiving your answers, outputs:

**Decisions Table**:
| Item | Choice | Reason | Notes |
|------|--------|--------|-------|
| Data storage | Database | Scalability needs | Consider migration strategy |

**Next Steps**:
1. First task with details
2. Second task with details

### Iteration
After Phase 3, the plugin revisits the plan file and continues to Phase 2 if any unclear points remain.

## Allowed Tools

This command uses the following Cursor tools:
- `Write` - Create new files
- `Edit` - Modify existing files
- `Read` - Read file contents
- `Grep` - Search file contents
- `Glob` - Find files by pattern
- `TodoRead` - Read todo list
- `TodoWrite` - Update todo list
- `AskUser` - Ask structured questions (core functionality)

## Plugin Structure

```
dig/
├─ .cursor-plugin/
│  └─ plugin.json        # Plugin manifest
├─ commands/
│  └─ dig.md             # Command definition
└─ README.md             # This file
```

## Credits

This plugin is a port of the [dig plugin](https://github.com/fumiya-kume/claude-code/tree/master/dig) from Claude Code by [Kuu](https://github.com/fumiya-kume).

Ported to Cursor by: captain-okinawa

## License

GPL-3.0 (same as original)

## Contributing

Issues and pull requests are welcome!

## Links

- Original Claude Code plugin: https://github.com/fumiya-kume/claude-code/tree/master/dig
- Cursor Documentation: https://cursor.com/docs
- Cursor Plugin Building Guide: https://cursor.com/docs/plugins/building
