# software-map

A prototype replacement for Cornell's public computer lab software map.
This prototype uses Leaflet to create an interactive map using data from a .geojson file:

https://kgjenkins.github.io/software-map/

The existing map, built around 2008, is at:

http://mapping.cit.cornell.edu/publiclabs/map/


## Data for the map

Each lab will be a GeoJSON point feature with the following properties:

| attribute | description | example |
| - | - | - |
| id | unique text string (from old system, where applicable) | "801" |
| name | common name of the lab | "Mann B30A Classroom" |
| building | building where the lab is located | Mann Library |
| url | website URL | "https://mannlib.cornell.edu/use/spaces/all/b30a" |
| hours | text or link for opening hours | "Open 24/7"<br>"http://mannlib.cornell.edu/hours" |
| access | who can access the lab | "public"<br>"restricted to AAP students" |
| admin | who runs the lab | "CU Library"<br>"CIT" |
| os | operating system(s) | "Windows 10"<br>"Mac"<br>"macOS 10.4 Mojave" |
| description | about the lab | "44 Dell Desktops"<br>"Located in the basement level of Olin Library" |
| printing | available printing options | "Net-Print Black & White"<br>"Net-Print Black & White, Net-Print Color" |
| software | names of sofware package available (version optional) | "Adobe Photoshop"<br>"Microsoft Word 2016"<br>"QGIS"<br>"QGIS 3.2.1" |

Here's an example of how this might look as GeoJSON:

```json
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [ -76.485659, 42.446652 ]
  },
  "properties": {
    "id": "793",
    "name": "Willard Straight CIT Lab",
    "building": "Willard Straight Hall",
    "hours": "Open During Normal Building Hours.",
    "access": "public",
    "admin": "CIT",
    "os": "Windows",
    "description": "7 Dell Optiplex 990 <br> Intel Core i7 Core-2600 <br> 3.4 Ghz / 4 GB Ram <br> CD/DVD RW<br><br>Also Macs with OS Yosemite, Adobe Creative Cloud, Microsoft Office 2016, and Final Cut Pro X",
    "printing": "Net-Print Black & White, Net-Print Color",
    "software": [
      "Adobe Acrobat Distiller",
      "Adobe Acrobat Pro",
      "Adobe Creative Cloud",
      "Adobe Media Player",
      "Audacity",
      "Autodesk",
      "Dr. Java",
      "Eclipse",
      "Google Earth",
      "Microsoft Access 2016",
      "Microsoft Excel 2016",
      "Microsoft InfoPath",
      "Microsoft OneNote 2016",
      "Microsoft PowerPoint 2016",
      "Microsoft Publisher 2016",
      "Microsoft Word 2016",
      "MiKTeX",
      "Minitab",
      "Netbeans IDE",
      "Premier AT",
      "Refworks",
      "Scanner",
      "SketchUp",
      "SSH Secure Shell",
      "Stella",
      "Windows Media Player",
      "VideoLAN"
    ]
  }
}
```


