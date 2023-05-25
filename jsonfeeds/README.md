# Sasquatch news feed

Chronograf is the main UI for the [Sasquatch](https://sqr-068.lsst.io) Phalanx application.

Chronograf uses the [JSON Feed Version 1.1](https://www.jsonfeed.org) specification to display a news feed on the client Status page.

This folder contains the JSON feed files used in each of the RSP environments where we deploy Sasquatch.
These files are served from the main branch of this repository, for example this is the URL for the [tucson_teststand.json](https://raw.githubusercontent.com/lsst-sqre/rsp_broadcast/main/jsonfeeds/tucson-teststand.json) feed.

To add a new item to the JSON feed, edit the file for the corresponding RSP environment and add the following content under the `items` key.
Remember to increment the item `id` number.

```
{
    "id": "12",
    "url": "https://sqr-068.lsst.io",
    "title": "Long live Sasquatch!",
    "content_text": "Sasquatch is a new service of the RSP that hosts the EFD, learn more at SQR-068.",
    "date_published": "2022-07-11T02:00:00-07:00",
    "date_modified": "2022-07-11T02:00:00-07:00",
    "image": "",
    "authors": [
        {
            "name": "SQuaRE"
        }
    ]
},
```
