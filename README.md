# Youform agent plugin and skill

Use Youform with an AI assistant to find form templates, create or edit forms, surveys and quizzes, publish authorized changes, and analyze responses.

## Install the agent skill

```sh
npx skills add mkmaker/youform-agent-plugin --skill youform
```

Choose the agent you use when prompted. The skill is installed in the current project by default. Review [the skill instructions](skills/youform/SKILL.md) before installing.

The skill contains instructions only. It does not install an MCP client, connect your account, or supply credentials.

## Connect Youform

Public template search needs no account. Working with private forms and responses requires a Youform MCP connection through your assistant's OAuth flow:

- Server: `https://app.youform.com/mcp`
- Transport: Streamable HTTP
- [Connection setup](https://help.youform.com/connect-an-ai-assistant-to-youform-1tjid)
- [Tools and permissions](https://help.youform.com/youform-mcp-tools-and-permissions-e9hl0)
- [Developer documentation](https://youform.com/developers/)

A normal Youform API token does not authenticate the MCP endpoint. Do not put credentials in this repository or paste OAuth tokens into chat.

Select the intended workspace and form. Keep changes in draft unless publishing is authorized, and access only the responses needed for the task.

## Existing directory configuration

`plugin.json`, `mcp.json`, and `server.json` describe the hosted Youform MCP connection for existing directory listings. Installing this skill does not change those connections.
