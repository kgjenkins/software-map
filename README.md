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
| building | where the lab is located | Mann Library |
| url | website URL | https://mannlib.cornell.edu/use/spaces/all/b30a |
| hours | text or link for opening hours | Open 24/7<br>http://mannlib.cornell.edu/hours |
| access | who can access the lab | public<br>restricted to AAP students |
| description | about the lab | 44 Dell Desktops |
| os | operating system(s) | Windows 10<br>Mac<br>macOS 10.4 Mojave |
| admin | who runs the lab | CU Library<br>CIT |
| software | names of sofware package available (versions optional) | Adobe Photoshop<br>QGIS<br>QGIS 3.2 |

Here's an example of how this might look as GeoJSON:

```json
{
  "type": "Feature",
  "properties": {
    "id": 793,
    "name": "Willard Straight CIT Lab",
    "building": "Willard Straight Hall",
    "hours": "Open During Normal Building Hours.",
    "access": "public",
    "admin": "CIT",
    "os": "Windows",
    "description": "7 Dell Optiplex 990<br /> Intel Core i7 Core-2600<br /> 3.4 Ghz / 4 Gb Ram<br /> CD/DVD RW",
    "software": [
      "Adobe Acrobat Distiller",
      "Adobe Acrobat Professional",
      "Adobe Media Player",
      "Audacity",
      "Dr. Java",
      "Google Earth",
      "Google Sketchup",
      "Microsoft Access",
      "Microsoft Excel",
      "Microsoft InfoPath",
      "Microsoft OneNote",
      "Microsoft PowerPoint",
      "Microsoft Publisher",
      "Microsoft Word",
      "Miktex",
      "Minitab",
      "Net-Print Black and White",
      "Net-Print Color",
      "Netbeans IDE",
      "Premier AT",
      "Refworks",
      "Scanner",
      "SSH Secure Shell",
      "Windows Media Player"
    ]
  },
  "geometry": {
    "type": "Point",
    "coordinates": [ -76.485659, 42.446652 ]
  }
}

```


