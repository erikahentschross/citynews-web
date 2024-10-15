# CityNews Web Widgets 

For use in iframes embedded in the website to provide a seamless user experience with other election coverage

## Integrating into election coverage web page

Navigate to where the election is located in the CMS. There will be several links to the widgets available. Click on each to get the url for that particular widget. Use this URL as the src in an iframe within the webpage. 

The Map widget can also default to an individual riding. Add the riding name to the end of the URL to set this default.

## Data folder structure

Elections are organized in the data folder as follows: 

```bash
├── {PROV} (2 letter abbreviation)
│   ├── {ElectionYear}
│   │   ├── {PROV}_config.json
│   │   ├── {PROV}_results.json
│   │   ├── {PROV}_prevResults.json
│   │   ├── {PROV}_topo.json
│   └── headshots
│   │   ├── ...candidate headshots
```

## Pushing data to the widget

#### Setup tab
Under Cloud, enter credentials for the CMS you are using. The directory field should point to the subdirectory the widget is placed in

#### Run tab
1. Enter BLADE URL. BLADE URL can be generated using the Election URL Generator in Chameleon or from the BLADE discovery tool in BLADE Runner. Select election event. Must be in JSON format
2. Check Cloud checkbox
3. Filename: /data/{prov}/{year}/{prov}_results.json
4. Filename:(only push once if the previous year's data is inaccurate) /data/{prov}/{year}/{prov}_prevResults.json

## Pushing candidate headshots

Candidate heashots are easily retrieved from chameleon using the Candidate Headshots URL Generator:
1. Select Election Event from the dropdown
2. Change file format to .jpg
3. once downloaded and unzipped, place headshots directly into the headshots folder (see data folder structure)

