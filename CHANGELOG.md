# Changelog

## [1.2.3](https://github.com/jpe-ansible/ansible-ai-agents/compare/v1.2.2...v1.2.3) (2026-10-29)


### Bug Fixes

* **hermes_runtime:** remove root-home install state by listing it ([#51](https://github.com/jpe-ansible/ansible-ai-agents/issues/51)) ([e402860](https://github.com/jpe-ansible/ansible-ai-agents/commit/e4028605e886263a168353b3144eb8fd897080b8))

## [1.2.2](https://github.com/jpe-ansible/ansible-ai-agents/compare/v1.2.1...v1.2.2) (2026-10-29)


### Bug Fixes

* **hermes_runtime:** report the launcher binding when the version read fails ([#48](https://github.com/jpe-ansible/ansible-ai-agents/issues/48)) ([3f1a60f](https://github.com/jpe-ansible/ansible-ai-agents/commit/3f1a60fbebef66b2f7a650be2bdea0f02206cbae))

## [1.2.1](https://github.com/jpe-ansible/ansible-ai-agents/compare/v1.2.0...v1.2.1) (2026-10-28)


### Bug Fixes

* **hermes_runtime:** bind the launcher to the service home ([#45](https://github.com/jpe-ansible/ansible-ai-agents/issues/45)) ([25ed638](https://github.com/jpe-ansible/ansible-ai-agents/commit/25ed638659132f00d7970704deac290433734a44))

## [1.2.0](https://github.com/jpe-ansible/ansible-ai-agents/compare/v1.1.5...v1.2.0) (2026-10-28)


### Features

* **hermes_runtime:** publish the PM-selected virtualenv ([#41](https://github.com/jpe-ansible/ansible-ai-agents/issues/41)) ([1bc9ac7](https://github.com/jpe-ansible/ansible-ai-agents/commit/1bc9ac7d047531a3bd1e7c14edac645c415bc5ae))

## [1.1.5](https://github.com/jpe-ansible/ansible-ai-agents/compare/v1.1.4...v1.1.5) (2026-10-28)


### Bug Fixes

* **hermes_runtime:** build and verify the PM-selected environment ([#39](https://github.com/jpe-ansible/ansible-ai-agents/issues/39)) ([0fa0826](https://github.com/jpe-ansible/ansible-ai-agents/commit/0fa08260251a38aa1b74232da9e874127fd805b2))

## [1.1.4](https://github.com/jpe-ansible/ansible-ai-agents/compare/v1.1.3...v1.1.4) (2026-10-28)


### Bug Fixes

* **hermes_runtime:** point the installer at the managed install dir ([#36](https://github.com/jpe-ansible/ansible-ai-agents/issues/36)) ([aa4d15c](https://github.com/jpe-ansible/ansible-ai-agents/commit/aa4d15c7ad829458f0a5f95d6b4098ec79d44eb2))

## [1.1.3](https://github.com/jpe-ansible/ansible-ai-agents/compare/v1.1.2...v1.1.3) (2026-10-28)


### Bug Fixes

* **hermes_runtime:** rerun installer stages on an existing checkout ([#33](https://github.com/jpe-ansible/ansible-ai-agents/issues/33)) ([755355d](https://github.com/jpe-ansible/ansible-ai-agents/commit/755355de2ef6ae9ed575a00a129b0e8432bb1065))

## [1.1.2](https://github.com/jpe-ansible/ansible-ai-agents/compare/v1.1.1...v1.1.2) (2026-10-28)


### Bug Fixes

* **hermes_runtime:** reinstall when the runtime venv Python differs from the PM pin ([#30](https://github.com/jpe-ansible/ansible-ai-agents/issues/30)) ([d1f1282](https://github.com/jpe-ansible/ansible-ai-agents/commit/d1f1282c61e31cd7bbc7bbebea2099fec7cc510d))

## [1.1.1](https://github.com/jpe-ansible/ansible-ai-agents/compare/v1.1.0...v1.1.1) (2026-10-28)


### Bug Fixes

* **hermes_runtime:** match the installed CLI version by its banner title ([#25](https://github.com/jpe-ansible/ansible-ai-agents/issues/25)) ([55c1fda](https://github.com/jpe-ansible/ansible-ai-agents/commit/55c1fda4d4b07003fad4dddaed2bd39b7cc2ecf6))

## [1.1.0](https://github.com/jpe-ansible/ansible-ai-agents/compare/v1.0.2...v1.1.0) (2026-10-28)


### Features

* **hermes_runtime:** install checksum-pinned plugins into each home ([#24](https://github.com/jpe-ansible/ansible-ai-agents/issues/24)) ([bfb3366](https://github.com/jpe-ansible/ansible-ai-agents/commit/bfb3366cd5b73c087385d218a9db18f57d068aad))


### Bug Fixes

* **hermes_runtime:** time out the first-install run ([#22](https://github.com/jpe-ansible/ansible-ai-agents/issues/22)) ([038e10b](https://github.com/jpe-ansible/ansible-ai-agents/commit/038e10b872c115296aa1115342df2f7b61e83146))

## [1.0.2](https://github.com/jpe-ansible/ansible-ai-agents/compare/v1.0.1...v1.0.2) (2026-10-20)


### Bug Fixes

* **hermes_runtime:** skip the checkout pin check mode cannot predict ([#20](https://github.com/jpe-ansible/ansible-ai-agents/issues/20)) ([bd620cd](https://github.com/jpe-ansible/ansible-ai-agents/commit/bd620cd3f48a1ef083859366aa1c9b7d5e1bc92b))

## [1.0.1](https://github.com/jpe-ansible/ansible-ai-agents/compare/v1.0.0...v1.0.1) (2026-10-14)


### Bug Fixes

* **hermes_runtime:** skip the checkout pin and reinstall when the CLI reports the pinned release ([#12](https://github.com/jpe-ansible/ansible-ai-agents/issues/12)) ([2456a81](https://github.com/jpe-ansible/ansible-ai-agents/commit/2456a817cd80ef5a5619d8f57310aa2c8a6cca45))

## 1.0.0 (2026-10-13)


### Features

* add the agent roster contract collection scaffold ([#1](https://github.com/jpe-ansible/ansible-ai-agents/issues/1)) ([09ced39](https://github.com/jpe-ansible/ansible-ai-agents/commit/09ced39f223822e2a4842236740c83264e29a8ae))
* **hermes_runtime:** add install and units entry points ([#8](https://github.com/jpe-ansible/ansible-ai-agents/issues/8)) ([e6f0bd4](https://github.com/jpe-ansible/ansible-ai-agents/commit/e6f0bd48014c8546096f41be1b72f48bbdff78f6))
* **hermes_runtime:** add the pinned Hermes install and systemd unit role ([#6](https://github.com/jpe-ansible/ansible-ai-agents/issues/6)) ([cf567ac](https://github.com/jpe-ansible/ansible-ai-agents/commit/cf567acfb0fef80787ef8d3745761540faeda3fd))

## Changelog

Release notes are maintained by Release Please.
