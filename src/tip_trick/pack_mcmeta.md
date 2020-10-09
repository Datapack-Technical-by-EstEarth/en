# pack.mcmeta trick

# about

It is a gimmick that you can use.

# Implementation

`pack.mcmeta` also support JSON Text Component. 
Which can be applied to `Advancement` too.

## Type 1

```json
{
	"pack": {
		"pack_format": 6,
		"description": [
			{
				"text": "verrion: 1.1.8\n",
				"color": "gold"
			},
			{
				"text": "dates: July 2020\n"
			},
			{
				"text": "author: EstEarth"
			}
		]
	}
}
```
![](./pack/1.png)

If you add `description '': ["", {` the bottom two lines will become the default color.

![](./pack/1_1.png)

## Type 2

```json
{
    "pack": {
        "pack_format": 6,
        "description": [
            {
                "text": "verrion: 1.1.8\n",
                "color": "dark_purple"
            },
            {
                "text": "dates: July 2020\n",
                "color": "#6600ff"
            },
            {
                "text": "author: EstEarth",
				"color": "gold",
				"font": "alt"
            }
        ]
    }
}
```
![](./pack/2.png)

For game version 1.16+ You can use *HEX* color value and *Custom Font* with *Resource pack*.

## Example of use for Advancement

```json
{
	"display": {
		"title": {
			"text": "      Est Clock Utility      ",
			"color": "yellow"
		},
		"description": [
			{
				"text": "Clock Day, ",
				"color": "green"
			},
			{
				"text": "Time, ",
				"color": "yellow"
			},
			{
				"text": "Weather, ",
				"color": "dark_aqua"
			},
			{
				"text": "Place characteristics, ",
				"color": "aqua"
			},
			{
				"text": "Moon, ",
				"color": "gray"
			},
			{
				"text": "Biomes",
				"color": "green"
			}
		],
		"icon": {
			"item": "minecraft:clock"
		},
		"announce_to_chat": false,
		"show_toast": false
	},
	"parent": "global:estearth",
	"criteria": {
		"trigger": {
			"trigger": "minecraft:tick"
		}
	}
}
```
![](./pack/3.png)

## Note

`\n` is for the new line. Recommend to put it behind the code pattern is more beautiful. If you put it in front of `n`, it will be attached to another text.