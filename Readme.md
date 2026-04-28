# `librelane_plugin_example`

This is a demonstrative example on how to make a plugin for Librelane that
includes both a custom step and a custom flow.

The step has a tool dependency, namely Ruby, to demonstrate the inclusion of an
open-source utility wiht a plugin.

## Testing this Plugin

Start by adding the path to the git repo root in your PYTHONPATH environment variable.

Then, to check if the plugin is recognized by Librelane:

```bash
$ nix develop --command librelane --version
[…]
Discovered plugins:
librelane_plugin_example -> 0.1.0
```

Testing that the added step and flow are working correctly:

```bash
$ nix develop --command librelane --flow FlowWithCustomAreaDoubler --run-example spm
```

## License
Apache License, version 2.0.

See `License`.

