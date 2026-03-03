# Learn VG Abstractions

A 2D vector graphics drawing tool that records user interactions to identify opportunities for new drawing abstractions and productivity improvements.

## Purpose

This is a research/learning tool designed to capture and analyze how users create vector graphics. By logging detailed action sequences, we can discover patterns in drawing workflows and design better tools, shortcuts, and features that match how people actually work.

## Features

### Drawing Tools
- **Line Tool** - Click and drag to create straight lines
  - Hold Shift to constrain to horizontal/vertical axes
- **Bezier Tool** - Multi-step cubic Bezier curve creation
  - Click-drag for first control point
  - Click to set end anchor
  - Drag to set second control point
- **Select Tool** - Click to select shapes, drag to move them
  - Marquee selection by dragging on empty space
  - Shift+click for multi-selection

### Editing Features
- Drag anchor points and control handles to reshape
- Copy/paste shapes (Cmd/Ctrl+C, Cmd/Ctrl+V)
- Undo actions (Cmd/Ctrl+Z)
- Delete selected shapes (Backspace)

### Action Logging
Every user interaction is recorded with:
- Action type and parameters
- Shape data (coordinates, IDs)
- Unique action IDs for traceability
- Timestamps for temporal analysis

Export the complete action log as JSON for analysis.

## Getting Started

```bash
# Install dependencies
npm install

# Run development server
npm run dev
```

Open the provided URL in your browser and start drawing!

## How It Works

The application uses:
- **SVG.js** - For rendering and manipulating vector graphics
- **Interact.js** - For drag-and-drop interactions
- **Vite** - For development and building

All drawing actions are logged to an in-memory array and can be exported as JSON using the "Export Log" button.

## Action Analysis

The `system-prompt.txt` file contains detailed instructions for analyzing exported action logs. An AI agent can process these logs to:

1. Identify repetitive action patterns
2. Discover multi-step workflows that could be simplified
3. Detect common shape combinations
4. Measure workflow efficiency using temporal data
5. Suggest new abstractions (tools, shortcuts, features)

## Use Cases

- **UX Research** - Understand how users create vector graphics
- **Tool Design** - Data-driven approach to designing drawing tools
- **Workflow Optimization** - Identify inefficiencies in creative workflows
- **UI/UX Education** - Study interaction patterns and tool usability

## License

MIT
