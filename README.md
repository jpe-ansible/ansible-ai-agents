# Ansible AI Agents

The `dryvist.ai_agents` collection defines a roster contract and a generic Hermes
runtime role for separately identified AI agents.

## Install

Pin the collection in a consumer `requirements.yml` file:

```yaml
collections:
  - name: https://github.com/jpe-ansible/ansible-ai-agents.git
    type: git
    version: v0.0.0
```

Install it with `ansible-galaxy collection install -r requirements.yml`.

## Roster contract

Set the role input `agent_base_agents` to a list of agents. Each entry has a lowercase `<function>-<persona>` name, a unique human display name, a one-line
purpose, and optional `owns` values. An `owns` value names an external system that only that agent may touch, and may appear on one agent only.

```yaml
agent_base_agents:
  - name: orchestrator-atlas
    display: Atlas Orchestrator
    owns: []
    purpose: Coordinate agent requests.
  - name: docs-scribe
    display: Scribe Documentation
    owns: [docs]
    purpose: Review documentation requests.
```

The input fields are:

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Lowercase `<function>-<persona>` identifier. |
| `display` | string | yes | Unique human display name. |
| `owns` | list of strings | no | External systems this agent alone may touch; defaults to `[]`. |
| `purpose` | string | yes | One-line purpose. |

## Run the contract test

From a development shell, run:

```sh
ansible-playbook -i examples/inventory.yml tests/contract.yml
```

The test validates the example roster, expects duplicate ownership and invalid names to fail, and checks argument-spec rejection of a missing required field.

## Hermes runtime

The `hermes_runtime` role installs a pinned Hermes Agent release and manages
gateway and dashboard systemd units. See [the role README](roles/hermes_runtime/README.md)
for inputs and an example.
