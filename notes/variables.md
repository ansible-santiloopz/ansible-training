# Variables

Ansible variables are managed with `Jinja2` template engine. This allow us to include values that change over time.
```yaml
-
	name: <value>
	hosts: <value>
	vars:
	- <varKey>: <value>
	- <varKey>: <value>
	- <varKey>: <value>
	...