# Raspberry Pi GPS

Build offline map (tile server OSM) with GPS and Raspberry Pi.

## Getting Started

A just-for-fun project
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Raspberry Pi
GPS U-Blox NEO-6M
UART to USB Converter

Python
OpenCV, Numpy, urllib

### Installing

Setup tile server: https://switch2osm.org/serving-tiles/manually-building-a-tile-server-18-04-lts/
Download the repository:

```
git clone https://github.com/datletrung/Raspberry-Pi-GPS.git
cd Raspberry-Pi-GPS
```

### Running the code

There are 2 files that is render_map.py and run.py:
  - render_map.py basically renders the map by using file coordinate.txt, without using GPS NEO-6M.
  - run.py use GPS NEO-6M to get realtime data. Therefore, make sure you change your USB port before you run the code.
  
```
p = '<COM# or /usb/tty#>'
```

You can test code with Here Map API in heremap folder, just simply replace your app_id and app_code and runthe code.

```
url = ..."app_id=<appid>&app_code=<appcode>"...
```

If you use a tile server, make sure your URL to your server is correct.

```
smurl = r"http://<server_ip>/map/{0}/{1}/{2}.png"
```

End with an example of getting some data out of the system or using it for a little demo

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Authors

* **Tin Le** - **Lê Trung Tất Đạt** - (https://github.com/datletrung)
