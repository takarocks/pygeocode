# pygeocode
Simple Python code for generating geocode (latitude and longitude) using Google Maps API.

# Version
  - 1.0
  - Oct 30, 2019

# Prerequisite
Google Maps API

# Setup
1. Get your Google API Key for Google Maps API.
2. Set your Google API Key as an environment variable GOOGLE_APIKEY. Alternatively, you can use config.py file and set your API Key in where it says `YOUR_APIKEY`.

# How to generate geocode for a single address
1. Run application as follows. Make sure to use single quote or double quote to surround address.
```shell
python pygeocode -a '53 State Street, Boston, MA 02109'
```
2. You will see following output on terminal.
```text
42.3587344, -71.0562932, 53 State Street, Boston, MA 02109
```

# How to generate geocode for multiple addresses
1. Alternatively, if you want to generate geocode for multiple addresses, create text file as follows. Keep each address per line, save the file as UTF-8 encoding without BOM (byte order mark). You can combine multiple international addresses in local language. For example, an address in the US and an address in Japan. See example below.
```text
53 State Street, Boston, MA 02109
163-8001 東京都新宿区西新宿2-8-1
```
2. Run application as follows. (Assuming the file is saved as `addresses.txt` in previous step.)
```shell
python pygeocode.py -f addresses.txt
```
3. You will see following output on terminal.
```text
42.3587344, -71.0562932, 53 State Street, Boston, MA 02109
35.6896342, 139.6921007, 163-8001 東京都新宿区西新宿2-8-1
```
