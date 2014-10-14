PluginLoader
============

A simple plugin loader

Usage
=====

### files/folders:

```
pluginfileloader.py
main.py
plugins
       \plugin1.py
       \plugin2.py
```

### main.py:

```python
from pluginfileloader import PluginFileLoader

plugin_path = 'plugins'
plugin_classes = []
for plugin_class in PluginFileLoader(plugin_path):
    cl = plugin_class()
    plugin_classes.append(cl)
```

Another Plugin Blueprint
========================

### files/folders:

```
pluginfileloader.py
main.py
pluginblueprint.py
plugins
       \plugin1.py
       \plugin2.py
```

### main.py:

```python
from pluginfileloader import PluginFileLoader
from pluginblueprint import MyPluginBlueprint

plugin_path = 'plugins'
plugin_classes = []
for plugin_class in PluginFileLoader(plugin_path, MyPluginBlueprint):
    cl = plugin_class()
    plugin_classes.append(cl)
```
