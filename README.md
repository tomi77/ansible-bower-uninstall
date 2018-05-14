# ansible-bower
A Ansible role to uninstall Bower packages

## Parameters

| Name             | Default                   | Description |
| ---------------- | ------------------------- | ----------- |
| bower_executable | ./node_modules/.bin/bower | Location of a `bower` command |
| pkg              |                           | Package(s) to install. If omit, uninstall from `bower.json` |
| chdir            | .                         | Location of a project |

## Examples

~~~yaml
# Uninstall all from bower.json
- tomi77.bower-uninstall

# Uninstall using global bower
- role: tomi77.bower-uninstall
  executable: bower

# Uninstall lodash package
- role: tomi77.bower-uninstall
  pkg: lodash

# Specify project location
- role: tomi77.bower-uninstall
  chdir: /location/of/a/project
~~~
