# ailiste MCP - new builds in Cyprus

[![ToolSDK MCP Registry](https://badges.toolsdk.ai/badge/@toolsdk-remote/ailiste)](https://toolsdk-ai.github.io/toolsdk-mcp-registry/#%40toolsdk-remote%2Failiste)
[![M8ven Score](https://m8ven.ai/badge/mcp/ahmlvs-ailiste-mcp-drspeb?v=60b803359a5f18ee23bd67fac9c95a71&variant=verified)](https://m8ven.ai/mcp/ahmlvs-ailiste-mcp-drspeb?s=readme)

A free, read-only [MCP](https://modelcontextprotocol.io) server for AI assistants: the new-build homes of
Cyprus - Limassol, Paphos, Larnaca, Nicosia and Famagusta's free area - and what is really there. For each
building: the stage our team saw on site, with the day; the developer; renders; floors, homes, bedrooms and
delivery. For each district: the asking price per square metre and for a whole home.

- **Endpoint:** `https://mcp.ailiste.app/` - Streamable HTTP, no sign-in, no key
- **Website:** [ailiste.app](https://ailiste.app) - how to connect, in six languages: [ailiste.app/mcp](https://ailiste.app/mcp/)
- **Official MCP Registry:** `app.ailiste/mcp`
- **Claude's connector directory:** [claude.ai/directory/ailiste](https://claude.ai/directory/ailiste)

This repository holds no code: the server runs at the address above. It is here so that catalogues of MCP
servers, and people, can find it.

## Tools

All five are read-only.

| tool | what it answers |
|---|---|
| `search` | buildings, developers, districts and cities by name, in English, Greek, Russian, Ukrainian, Hebrew or Chinese - at most 8, each with its ailiste page |
| `find_buildings` | new builds by city, district, developer, apartments or villas, bedrooms, construction stage, delivery year, sea view, pool, or seen by our team - 10 at a time |
| `get_building` | what a building's page says: developer, stage and the day we saw it, our photographs, delivery, floors, homes, bedrooms, sizes, the asking price it starts at, views, amenities |
| `district_prices` | asking prices in a district or city for one kind and size of home: median, mean and middle half, per m² and for the whole home, with the sample and the day |
| `get_developer` | a developer's buildings by city, stage and kind, and how many our team has visited |

## Connect

- **Claude** (claude.ai or the desktop app): from Claude's connector directory, https://claude.ai/directory/ailiste - or Settings → Connectors → Add custom connector → `https://mcp.ailiste.app/`
- **Claude Code:** `claude mcp add --transport http ailiste https://mcp.ailiste.app/`
- **Cursor** (`mcp.json`): `{"mcpServers": {"ailiste": {"url": "https://mcp.ailiste.app/"}}}`
- **Grok:** grok.com/connectors → New Connector → Custom → `https://mcp.ailiste.app/`
- **Gemini CLI:** `gemini extensions install https://github.com/ahmlvs/ailiste-mcp`
- Any other client that speaks Streamable HTTP: the endpoint above.

The configuration, for a client that takes a JSON file (Cursor's `mcp.json`, Claude Code's `.mcp.json`, VS Code,
Windsurf and others):

```json
{
  "mcpServers": {
    "ailiste": {
      "type": "http",
      "url": "https://mcp.ailiste.app/"
    }
  }
}
```

The same as a command:

```bash
claude mcp add --transport http ailiste https://mcp.ailiste.app/
```

## Ask it

- "New two-bedroom apartments in Germasogeia with a pool, ready by 2027"
- "Is Zanos City in Nicosia really under construction?"
- "What does a square metre cost in Paphos, and where is it cheaper?"
- "Who is Kimonas Group and what are they building?"

## What it is and is not

- Prices are **asking prices** in adverts, not sale prices.
- `seen_by_us` is the day our team stood at the building; a stage without it is what its portal lists.
- Every answer links to its page on ailiste.app, where the photographs and the map are.
- No account, no personal data, no transactions. What assistants ask is kept, without who asked:
  [ailiste.app/privacy](https://ailiste.app/privacy/).

## License

The text of this repository: MIT. The data is ailiste's and is served by the endpoint.
