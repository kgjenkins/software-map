# SEE https://github.com/cul-it/campus-software-map


# software-map

A prototype replacement for Cornell's public computer lab software map.
This prototype uses Leaflet to create an interactive map using data from a .geojson file:

https://kgjenkins.github.io/software-map/

The existing map, built around 2008, is at:

http://mapping.cit.cornell.edu/publiclabs/map/


## Data for the map

Each lab is represented as a GeoJSON point feature with the following properties:

| attribute | description | example |
| - | - | - |
| id | unique text string (from old system, where applicable) | "801" |
| name | common name of the lab | "Mann B30A Classroom" |
| building | building where the lab is located | "Mann Library" |
| url | website URL | `"https://mannlib.cornell.edu/use/spaces/all/b30a"` |
| hours | text or link for opening hours | "Open 24/7"<br>`"http://mannlib.cornell.edu/hours"` |
| access | who can access the lab | "public"<br>"restricted to AAP students" |
| admin | who runs the lab | "CU Library"<br>"CIT" |
| os | operating system(s) | "Windows 10"<br>"Mac"<br>"macOS 10.4 Mojave" |
| description | about the lab | "44 Dell Desktops"<br>"Located in the basement level of Olin Library" |
| printing | available printing options | "Net-Print Black & White"<br>"Net-Print Black & White, Net-Print Color" |
| software | names of sofware package available (version optional) | "Adobe Photoshop"<br>"Microsoft Word 2016"<br>"QGIS"<br>"QGIS 3.2.1" |

Here's an example:

```json
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [ -76.475923, 42.448822 ]
  },
  "properties": {
    "id": "801",
    "name": "Mann Library B30B classroom",
    "building": "Mann Library",
    "url": "https://mannlib.cornell.edu/use/spaces/all/b30b",
    "hours": "http://mannlib.cornell.edu/hours",
    "access": "public",
    "admin": "CU Library",
    "os": "Windows",
    "description": "31 Dell desktops",
    "printing": "Net-Print Black & White, Net-Print Color",
    "software": [
      "7-Zip",
      "Adobe Acrobat DC",
      "Adobe After Effects",
      "Adobe Animate",
      "Adobe Audition",
      "Adobe Bridge",
      "Adobe Dreamweaver",
      "Adobe Fireworks",
      "Adobe Flash Builder",
      "Adobe Flash",
      "Adobe Illustrator",
      "Adobe InCopy",
      "Adobe InDesign",
      "Adobe Lightroom",
      "Adobe Media Encoder",
      "Adobe Muse",
      "Adobe Photoshop",
      "Adobe Prelude",
      "Adobe Premier Pro",
      "Adobe Speed Grade 2015",
      "Anaconda",
      "ArcGIS Desktop (ArcMap) 10.5.1",
      "ArcGIS Pro 2.2",
      "Artemis",
      "Autodesk (AutoCAD) 2019",
      "CBGP - GeneClass2",
      "Corpscon",
      "Density 5",
      "Distance 7.1",
      "DNRGPS",
      "EasyPop",
      "EndNote X8",
      "Evernote",
      "FileZilla",
      "Firefox",
      "GenePOP",
      "Git for Windows",
      "GitHub Desktop",
      "Google Chrome",
      "Google Earth Pro",
      "Internet Explorer 11",
      "Inverse 3D-Forward 3D",
      "Java",
      "JAWS",
      "JMP 14",
      "MARK 8.2",
      "Mauve",
      "Maxima 5.40.0",
      "MEGA 7",
      "Microsoft Access 2016",
      "Microsoft Edge",
      "Microsoft Excel 2016",
      "Microsoft OneNote 2016",
      "Microsoft PowerPoint 2016",
      "Microsoft Publisher 2016",
      "Microsoft Silverlight",
      "Microsoft Word 2016",
      "MiKTeX 2.9",
      "NED-2",
      "NEURON 7.4",
      "Notepad++",
      "OpenBUGS",
      "Photoshop (Adobe)",
      "PMP7",
      "Populus",
      "Premier Literacy Suite 32 Bit",
      "PSPP",
      "PuTTY",
      "Python",
      "QGIS 3.2.1",
      "R 3.5.1",
      "RealPlayer",
      "Rhino 5",
      "RStudio 1.1.453",
      "RUSLE2",
      "SAP Lumira",
      "SAPGUI",
      "SheepSim",
      "SketchUp 2017",
      "Stata 15",
      "Stella Professional 1.4.1",
      "Stewplan 1.2",
      "Tropcrop 2.40",
      "Vensim Model Reader",
      "Vensim PLE",
      "VLC Media Player",
      "Vortex 10.8.2"
    ]
  }
}
```

