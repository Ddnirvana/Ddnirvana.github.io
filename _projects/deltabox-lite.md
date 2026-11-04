---
layout: page
title: DeltaBox Lite
permalink: /projects/deltabox-lite/
description: Lightweight file sandboxing for AI agents, with diff, commit, and abort.
importance: 1
category: Agent systems
published: true
---

**DeltaBox Lite** gives AI agents a controlled filesystem workspace with explicit **diff, commit, and abort** operations. It lets developers inspect an agent's file changes and choose whether to keep or roll them back, at the level of a task or a tool call.

[Source code on GitHub](https://github.com/delta-box/deltabox-lite) · [Release introduction (中文)](https://mp.weixin.qq.com/s/uFswgOfOJK-yrYwZslTDaA)

### What it provides

- **Reviewable changes:** inspect file changes before deciding what to retain.
- **Checkpoints and rollback:** accept a session's changes or return to an earlier checkpoint.
- **Agent integration:** a command-line interface and adapters for agent workflows, including Pi and DSH.

DeltaBox Lite is a standalone file-sandbox runtime. It builds on our research into agent sandboxes, alongside [DeltaBox]({{ '/publications/#dong2026deltabox' | relative_url }}), which uses microVM checkpoints for stateful agents.

We open-sourced DeltaBox Lite on **October 16, 2026**. See the [repository README](https://github.com/delta-box/deltabox-lite#readme) for current platform support, installation, and usage.
