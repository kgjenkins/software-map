# software-map

A prototype replacement for Cornell's public computer lab software map.
This prototype uses Leaflet to create an interactive map using data from a .csv file:

https://kgjenkins.github.io/software-map/

The existing map, built around 2008, is at:

http://mapping.cit.cornell.edu/publiclabs/map/


## Data for the map

Proposed attributes for each lab:

| attribute | description | example |
| - | - | - |
| coordinates | point longitude, latitude | [-76.476471, 42.448915] |
| name | common name of the lab | Mann B30A Classroom |
| location | where the lab is located | Mann Library |
| hours | text or link for opening hours | Open 24/7<br>http://mannlib.cornell.edu/hours |
| access | who can access the lab | public<br>restricted to AAP students |
| description | about the lab | 44 Dell Desktops |
| os | operating system(s) | Windows<br>Mac |
| admin | who runs the lab | CU Library<br>CIT |
| software | names of sofware package available (versions optional) | Adobe Photoshop<br>QGIS<br>QGIS 3.2 |

Here's an example of how this might look as JSON:

```json
{
  "coordinates": [-76.476471, 42.448915],
  "name": "Mann Library - B30A PC Classroom",
  "location": "B30A Mann Library",
  "hours": "http://mannlib.cornell.edu/hours",
  "access": "public",
  "description": "44 Dell Desktops",
  "os": "Windows",
  "admin": "CU Library",
  "software": [
    "Adobe Acrobat Distiller",
    "Adobe Acrobat Professional",
    "Adobe Acrobat Reader",
    "Adobe Bridge",
    "Adobe Dreamweaver",
    "Adobe Drive",
    "Adobe ExtendScript Toolkit",
    "Adobe Extension Manager",
    "Adobe Fireworks",
    "Adobe Flash Professional",
    "Adobe Illustrator",
    "Adobe InDesign",
    "Adobe Media Encoder",
    "Adobe Media Player",
    "Adobe Photoshop",
    "Adobe Premier Pro",
    "ArcGIS 10.5.1",
    "AutoCAD",
    "Endnote",
    "Google Earth",
    "Google Sketchup",
    "Jaws"
    "Microsoft Access",
    "Microsoft Excel",
    "Microsoft InfoPath",
    "Microsoft OneNote",
    "Microsoft PowerPoint",
    "Microsoft Publisher",
    "Microsoft Word",
    "Miktex",
    "Net-Print Black and White",
    "Net-Print Color",
    "Premier AT",
    "QGIS 3.2",
    "R",
    "Scanner",
    "STATA/Intercooled",
    "Stella",
    "Tropcrop",
    "VideoLAN",
    "Windows Media Player"
  ]
}
```


