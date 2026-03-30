# codex-global-rules

[![GitHub Stars](https://img.shields.io/github/stars/Hyggetxc/codex-global-rules?style=flat-square)](https://github.com/Hyggetxc/codex-global-rules/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Hyggetxc/codex-global-rules?style=flat-square)](https://github.com/Hyggetxc/codex-global-rules/network/members)
[![GitHub Issues](https://img.shields.io/github/issues/Hyggetxc/codex-global-rules?style=flat-square)](https://github.com/Hyggetxc/codex-global-rules/issues)
[![AGENTS.md](https://img.shields.io/badge/AGENTS-md-2f81f7?style=flat-square)](https://github.com/Hyggetxc/codex-global-rules/blob/main/AGENTS.md)

`codex-global-rules` is a repository for maintaining Codex global rules in one place.

It is designed for people who want to:

- keep a single source of truth for cross-project Codex rules
- sync a reusable `AGENTS.md` across devices or workspaces
- keep snapshots of important rule changes
- publish rules in a sanitized way without exposing real local device names or project names

## Translations

- [English](./README.md)
- [简体中文](./README.zh-CN.md)

## Online

- Repository: [https://github.com/Hyggetxc/codex-global-rules](https://github.com/Hyggetxc/codex-global-rules)
- Main rules file: [AGENTS.md](https://github.com/Hyggetxc/codex-global-rules/blob/main/AGENTS.md)

## Why This Exists

When Codex is used across multiple projects, it is easy for collaboration rules to drift over time.

This repository keeps the global rules in a single versioned place so they can be:

- reviewed
- updated
- backed up
- reused across projects
- shared without leaking machine-specific or project-specific private information

## Features

- Store a central `AGENTS.md` as the main global rules file
- Keep historical rule snapshots in `snapshots/`
- Use placeholder paths such as `<用户目录>` instead of real local paths
- Avoid committing real device names or sensitive project names
- Maintain a reusable structure for long-term Codex collaboration

## Repository Structure

- `AGENTS.md`: the main global rules file
- `snapshots/`: backup notes and historical snapshots for important rule changes

## Usage

1. Review the repository-level [`AGENTS.md`](./AGENTS.md).
2. Adapt it to your own workflow if needed.
3. Sync it to your Codex user-level global rules path.
4. Create a snapshot before large changes.
5. Push changes back to this repository as the canonical source.

Example user-level target path:

- Windows: `%USERPROFILE%\\.codex\\AGENTS.md`

Use your own local user directory when applying the file. Do not commit your real machine path back into the repository.

## Privacy

- This repository is intended to store sanitized global rules only.
- Real local device names, real usernames, and real project names should not be committed.
- Use generic placeholders such as `<用户目录>` or `<当前项目>` wherever possible.

## Roadmap

Possible future additions:

- `docs/` for setup guides and examples
- bilingual docs for more rule modules
- templates for different Codex usage styles
- release notes for major rule revisions
- examples for project-level inheritance patterns

## Support

If this repository helps you standardize and reuse your Codex global rules, please consider giving it a Star:

- [Star this repository](https://github.com/Hyggetxc/codex-global-rules)
