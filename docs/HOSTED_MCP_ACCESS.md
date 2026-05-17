# Hosted MCP access

The Education Agent Skills Library is free and open source. The hosted MCP server is a convenience endpoint for remote clients that cannot install the skills locally.

If you can use the skills locally, please do that first. Local use costs nothing to host, keeps the project sustainable, and avoids routing your work through the public MCP server.

## What is changing?

The public hosted MCP endpoint has created real infrastructure costs because anonymous remote clients can open long-lived connections. Those connections are useful for some MCP workflows, but they are not free to run at public scale.

The plan is to keep the library free while moving hosted MCP access toward a more sustainable model:

- Local plugin use remains free.
- Manual copy-paste use remains free.
- The GitHub repository remains open.
- Hosted MCP may become access-controlled, rate-limited, or offered by request.

## Free alternatives to hosted MCP

### Claude

Use the Claude plugin route where available:

```text
https://github.com/GarethManning/education-agent-skills
```

Or install with Claude Code:

```bash
claude plugin install https://github.com/GarethManning/education-agent-skills
```

### OpenAI Codex

Use the local Codex plugin or copy individual skills locally. See [CODEX.md](CODEX.md).

### Any AI tool

Open any `SKILL.md` file under `skills/`, copy the instructions, and paste them into Claude, ChatGPT, Codex, Gemini, or another assistant with your teaching context.

### Local MCP

Clone the repository and run the MCP server locally if your client supports local MCP configuration. See [mcp-server/README.md](../mcp-server/README.md).

## Hosted MCP access requests

Hosted MCP is mainly for people who cannot use local plugins or local skill files, or who are building a workflow that specifically depends on remote MCP discovery.

Request hosted MCP access here:

```text
https://docs.google.com/forms/d/e/1FAIpQLSdW1EdcmtjSPPq68Hx-bdth5hO2KNyjhAwEV9Ld0EwWL1Gr8Q/viewform
```

The form is intentionally short and respectful. It collects only what is needed to decide whether hosted access is the right path.

After someone submits the form, access is not provisioned automatically yet. The current process is:

1. Review the request.
2. If hosted access is appropriate, send the requester a token or connector details by email.
3. Include short setup instructions for their client, including whether they need to reconnect, disable/re-enable a connector, or paste a token into an auth screen.

Recommended fields:

### Required

1. **Email address** — needed to send an access link or token.
2. **Which tool are you using?** — Claude.ai, Claude Desktop, Claude Code, Codex, custom MCP client, other.
3. **Do you specifically need the hosted MCP endpoint?** — yes/no/not sure.
4. **Brief use case** — one or two sentences about what you are trying to do.
5. **Fair-use acknowledgement** — checkbox: “I understand hosted MCP has real infrastructure costs and I will use local/free options where they work for my workflow.”

### Optional

1. Name.
2. Organisation or role.
3. GitHub username.
4. Whether you are happy to be contacted about your use case.

### Do not ask

- Phone number.
- Exact income or budget.
- Student names or student data.
- School address.
- Detailed lesson materials.
- A long justification for why they “deserve” access.

## Suggested form copy

Title:

> Education Agent Skills — Hosted MCP Access Request

Description:

> The Education Agent Skills Library remains free and open source. For most people, the best free route is to install the skills locally from GitHub or use them manually from the `SKILL.md` files.
>
> This form is only for people who specifically need the hosted MCP endpoint. Hosted MCP creates infrastructure costs, so I’m using this form to understand who depends on it and how to keep access sustainable.
>
> After you submit, I’ll review the request and email the next step. This form does not automatically issue a token yet. If hosted access is enabled for you, the email will include the token or connector details and short setup instructions for your client.
>
> Please do not include student data or confidential school information.

Required questions:

1. **Email address**
   - Short answer
   - Required

2. **Which tool are you using?**
   - Multiple choice
   - Required
   - Claude.ai
   - Claude Desktop
   - Claude Code
   - OpenAI Codex
   - ChatGPT or another OpenAI tool
   - Custom MCP client
   - Other / not sure

3. **Do you specifically need the hosted MCP endpoint?**
   - Multiple choice
   - Required
   - Yes — my workflow depends on remote MCP
   - Not sure — I need help choosing the right setup
   - No — I can probably use the local/free options

4. **What are you trying to use the skills for?**
   - Paragraph
   - Required
   - Helper text: “One or two sentences is enough. Please do not include student data.”

5. **Fair-use acknowledgement**
   - Checkbox
   - Required
   - “I understand hosted MCP has real infrastructure costs and I will use local/free options where they work for my workflow.”

Optional questions:

6. **Name**
7. **Organisation or role**
8. **GitHub username**
9. **Are you happy for me to contact you about your use case?**

## Tone note

Avoid making people prove hardship. If someone cannot pay or needs help, let them explain that in the optional “anything else” field. The public message can say: “If hosted access is essential and the alternatives do not work for you, use the form and I’ll try to help.”
