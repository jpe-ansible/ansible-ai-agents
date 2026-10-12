# `hermes_runtime`

Installs a checksum-verified Hermes Agent release, enforces the tagged checkout,
verifies the installed CLI version, and manages gateway and dashboard systemd
units. Run the role with privilege escalation. The target must support the
upstream installer and systemd.

## Inputs

| Variable | Type | Required | Description |
| --- | --- | --- | --- |
| `hermes_runtime_version` | string | no | Bare release version; defaults to `2026.9.11`. |
| `hermes_runtime_repo_url` | string | no | Upstream source repository URL. |
| `hermes_runtime_installer_url` | string | no | Immutable installer URL for the selected release. |
| `hermes_runtime_installer_sha256` | string | no | Installer checksum; defaults to the source release pin. |
| `hermes_runtime_installer_path` | path | no | Download destination for the installer. |
| `hermes_runtime_install_dir` | path | no | Source checkout path. |
| `hermes_runtime_bin` | path | no | Installed Hermes CLI path. |
| `hermes_runtime_user` | string | yes | Service account. |
| `hermes_runtime_group` | string | yes | Service group. |
| `hermes_runtime_uid` | integer | yes | UID used for user-session ordering. |
| `hermes_runtime_hermes_home` | path | yes | Working directory and `HERMES_HOME`. |
| `hermes_runtime_environment_file` | path | yes | Optional environment file loaded by both units. |
| `hermes_runtime_dashboard_web_dist` | path | no | Dashboard web asset directory. |
| `hermes_runtime_dashboard_host` | string | yes | Dashboard bind host. |
| `hermes_runtime_dashboard_port` | integer | yes | Dashboard port. |
| `hermes_runtime_gateway_cmd` | string | yes | Gateway command. |
| `hermes_runtime_unit_restart_interval_sec` | integer | yes | systemd start-limit interval. |
| `hermes_runtime_unit_restart_burst` | integer | yes | systemd start-limit burst. |
| `hermes_runtime_restart` | string | yes | systemd restart policy. |
| `hermes_runtime_restart_sec` | string | yes | Delay before a restart. |
| `hermes_runtime_systemd_unit_dir` | path | no | Unit directory used by default unit paths. |
| `hermes_runtime_gateway_unit_path` | path | no | Gateway unit destination. |
| `hermes_runtime_dashboard_unit_path` | path | no | Dashboard unit destination. |
| `hermes_runtime_gateway_restart_handler` | string | no | Handler notified when the gateway unit changes. |
| `hermes_runtime_dashboard_restart_handler` | string | no | Handler notified when the dashboard unit changes. |
| `hermes_runtime_unit_on_failure` | string | no | Optional `OnFailure` unit for both services; defaults to empty. |
| `hermes_runtime_gateway_environment` | list of `{name, value}` | no | Additional gateway `Environment` entries; defaults to empty. |
| `hermes_runtime_dashboard_environment` | list of `{name, value}` | no | Additional dashboard `Environment` entries; defaults to empty. |
| `hermes_runtime_gateway_after_user_manager` | boolean | no | Order the gateway after the user's systemd manager; defaults to false. |

## Example

```yaml
- name: Install Hermes runtime
  hosts: agents
  become: true
  roles:
    - role: dryvist.ai_agents.hermes_runtime
      vars:
        hermes_runtime_user: hermes
        hermes_runtime_group: hermes
        hermes_runtime_uid: 1001
        hermes_runtime_hermes_home: /var/lib/example.com/.hermes
        hermes_runtime_environment_file: /var/lib/example.com/.hermes/.env
        hermes_runtime_dashboard_host: example.com
        hermes_runtime_dashboard_port: 8080
        hermes_runtime_gateway_cmd: /usr/local/bin/hermes gateway run --replace
        hermes_runtime_unit_restart_interval_sec: 300
        hermes_runtime_unit_restart_burst: 5
        hermes_runtime_restart: always
        hermes_runtime_restart_sec: 5s
```
