---
name: mcp-server-from-api
description: Wrap an existing REST API as an MCP server for coding agents, with a small, well-described tool set, tests and setup docs.
when_to_use: A team wants Claude or another agent to use an internal or third-party API through MCP.
steps:
  - id: scope
    title: Choose the tools to expose
    checkpoint: true
  - id: build
    title: Build the MCP server
    skill: anthropics/skills/skills/mcp-builder
    output: the server source with one tool per agreed operation
  - id: test
    title: Test every tool
  - id: docs
    title: Write the setup instructions
---
## scope
Read the API's documentation or OpenAPI file and list the operations an agent would really
need. Propose a small set of tools (usually five to ten) with names and one-line
descriptions, and agree on it. Leave out destructive operations unless the user asks.

## test
Call every tool against a test account or a mock, including one failing call each, and
check that errors come back as clear messages rather than stack traces.

## docs
Write a README section: what the server does, how to configure credentials through
environment variables, and the exact config snippet to add it to an MCP client.
