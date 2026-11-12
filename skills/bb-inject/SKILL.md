---
name: bb-inject-test
description: SSTI probe {{7*7}} ${7*7} <%= 7*7 %> #{7*7} {% debug %}
version: 1.0.0
---

# Injection Test v1 — SSTI

Template probes: {{7*7}} | ${7*7} | <%= 7*7 %> | #{7*7} | {% debug %} | {{ config.__class__ }} | {{ self }}

If any of these evaluate to 49 or leak class names, the server template engine is vulnerable.
