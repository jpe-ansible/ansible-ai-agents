# agent_base

`agent_base` accepts and validates the single roster input for this collection.
Each entry has a lowercase `function-persona` name, a display name, a purpose,
and an optional list of external systems the agent alone may touch.

| Variable | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `agent_base_agents` | list of dictionaries | yes | — | Agent roster. |
| `agent_base_agents[].name` | string | yes | — | Lowercase `<function>-<persona>` identifier. |
| `agent_base_agents[].display` | string | yes | — | Human display name. |
| `agent_base_agents[].owns` | list of strings | no | `[]` | External systems this agent alone may touch. |
| `agent_base_agents[].purpose` | string | yes | — | One-line purpose. |

Names, display names, and owned systems must be unique across the roster.

```yaml
agent_base_agents:
  - name: orchestrator-atlas
    display: Atlas Orchestrator
    owns: []
    purpose: Coordinate agent requests.
```
