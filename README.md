# MMM-homeassistant-feed
A MagicMirror module that displays information from homeassistant API.

This code is partially copied from https://github.com/amcolash/MMM-json-feed.


## Configuration
It is very simple to set up this module, a sample configuration looks like this:

```
modules: [
  {
    module: 'MMM-homeassistant-feed',
    position: 'bottom_left',
    config: {
      url: 'http://youehomeassistant:8123/api/states',
      prettyName : 'true',
      stripName: 'true',
      values: ["cover.office", "sensor.owm_pressure"]
    }
  }
]
```

## Configuration Options

| Option               | Description
| -------------------- | -----------
| `prettyName`         | Pretty print the name of each JSON key (remove camelCase and underscores). <br><br> **Default value:** `true`
| `stripName`          | Removes all keys before the printed key. <br><br>**Example:** `a.b.c` will print `c`.<br> **Default value:** `true`
| `title`              | Title to display at the top of the module. <br><br> **Default value:** `JSON Feed`
| `url`                | The url of the homeassitant api . <br><br> **Default value:** `REQUIRED`
| `updateInterval`     | The time between updates (In milliseconds). / <br><br> **Default value:** `300000 (5 minutes)`
| `values`             | Specify specific values from the json feed to only show what you need (entity_id). <br><br>**Example:** `["key1", "key2", "keyA.keyB.keyC"]`<br> **Default value:** `[]` (Shows all keys in the object)
# MMM-homeassistant-sensors
