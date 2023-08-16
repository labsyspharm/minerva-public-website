---
layout: default
nav_exclude: false
title: Additional Customizations
parent: Running Minerva
nav_order: 17
---
After your story is exported (with the "Publish" button), you can manually edit the `exhibit.json` file, which follows [this schema](https://labsyspharm.github.io/minerva-story/json-schema/exhibit/build/).

## Additional Customization

Manual edits to the `exhibit.json` file allow further customization than possible with the UI.

### Lensing Configuration

You may wish to display a custom channel in a movable "lens" atop an existing waypoint.

You may add a "Lensing" configuration with the following properties:

- "Group" must match the `Name` of an item in the `Groups` array:
- "Rad" optionally specifies the radius of the lens in screen pixels:

The "Lensing" may be defined for all waypoints with:

```json
{
  "Lensing": {"Group": "Lensing Channel Group", "Rad": 100},
  "Stories": [],
  "Groups": [],
  "Masks": []
}
```

The lensing may also be defined within a waypoint:

```json
  "Stories": [
    {
      "Name": "Example Story",
      "Waypoints": [
        {
          "Lensing": {
            "Group": "Lensing Channel Group",
            "Rad": 100
          },
          "Zoom": 0.5,
          "Pan": [ 0.5, 0.5 ],
          "Name": "Example Waypoint",
          "Group": "Example Channel Group",
          "Description": "In this tissue specimen...",
        },
      ]
    }
  ]
```


{: .fs-3 }
{: .fw-300 }
> \*Remember to ....