# EIA Datatools

Row 70 of [EDGI: Uncrawlable Content](https://docs.google.com/spreadsheets/d/1nSav_VXulUWi6Zf_FVEzbNgkhFJlMZtiK6JMsY8Sdhw/edit#gid=1967480336) refers to
[DATA TOOLS & MODELS](http://www.eia.gov/tools/models/datatools.cfm), which acts as a portal to information about different kinds of energy.
Following the [Electricity Data Files](http://www.eia.gov/electricity/data/detail-data.html) link led to a page of links to pages for different surveys.
Ignoring the link to consolidated data,
figuring that the original sources were more important,
and ignoring the link to `eia860`,
since that was already on the edgi sheet,
the links point to:
* [eia826/](http://www.eia.gov/electricity/data/eia826/)
* [eia861/](http://www.eia.gov/electricity/data/eia861/)
* [eia860m/](http://www.eia.gov/electricity/data/eia860m/)
* [eia923/](http://www.eia.gov/electricity/data/eia923/)
* [eia411/](http://www.eia.gov/electricity/data/eia411/)
* [emissions/](http://www.eia.gov/electricity/data/emissions/)
* [water/](http://www.eia.gov/electricity/data/water/)
* [eia767/](http://www.eia.gov/electricity/data/eia767/)
* [eia412/](http://www.eia.gov/electricity/data/eia412/)

Each of these pages contains lists of links to `.zip`, `.xls`, or `.xlsx` files, so I wanted to download only those.

In the linux bash shell, I setup a for loop through the above links, doing
```
wget -r -A 'zip,xls,xlsx' $url
```
(where `$url` is substituted with an url in the above list).

I meant to add the parameter to limit the depth to 1, but forgot. The net result is a huge directory tree of files.
