# Repository rules

- Keep scripts out of the repository. Example names and systems use generic personas and example values.
- `roles/agent_base/meta/argument_specs.yml` and its single assertion task define the roster contract.
- Open pull requests against `develop`. Release from `main` with Release Please.
- `agent_base` owns the roster input contract and generic agent plumbing.
  `hermes_runtime` owns generic Hermes runtime mechanics: install, units, and plugins.
  Deployment-specific data, secrets, and source patches stay in the consumer.

## Commands

- `nix develop -c ansible-playbook -i examples/inventory.yml tests/contract.yml`
- `nix develop -c ansible-playbook -i examples/inventory.yml playbooks/site.yml`
- `nix develop -c ansible-lint`
- `nix develop -c pre-commit run --all-files`
