---
title: Real-time Arrivals
thumbnail: "/upload/arrivals.png"
description: Real-time vehicle position delivered via a RESTful web service in XML,
  JSON, and JSONP
categories: []
year: 2009
date: 

---
The API delivers three different flavors of data: XML, JSON, and JSONP. This table lists the formats and their MIME types.

| MIME type | Description |
| --- | --- |
| text/xml | XML is an encoded document format with arbitrary structure best consumed by machines. |
| application/json | JSON (an acronym for JavaScript Object Notation) is a lightweight text-based open standard designed for the exchange of human-readable data. This is the default. |
| application/javascript | Also known as JSON-P or JSON with padding. This is a JSON payload wrapped in a callback function. JSON-P is designed to be evaluated in the browser within a <script> element. |

## Metro’s Realtime API Collections

The interface is divided into four collections: Agency, Routes, Stops, and Vehicles. Each collection returns a list of elements. The element IDs tacitly suggest the URL for the element.

| Method | Description |
| --- | --- |
| agencies | “lametro” is the only available Agency element (for now). Agency ID is case-sensitive, and should be all lower-cased. |
| routes | A list of routes available at the agency. |
| stops | A list of stops served by the route. |
| vehicles | A list of the current position of all vehicles belonging to the agency. |

Consider these examples. The first retrieves a _collection_ of routes operated by agency LA Metro. The second retrieves predictions for _element_ stop 6033 . These links open in a new browser window. Go ahead and try them!

* [http://api.metro.net/agencies/lametro/routes/](http://api.metro.net/agencies/lametro/routes/ "http://api.metro.net/agencies/lametro/routes/")
* [http://api.metro.net/agencies/lametro/stops/6033/predictions/](http://api.metro.net/agencies/lametro/stops/6033/predictions/ "http://api.metro.net/agencies/lametro/stops/6033/predictions/")

Check the [**examples**](https://web.archive.org/web/20170825081250/http://developer.metro.net/realtime-api-examples) page for more.

## Methods available for most elements

| Method | Description |
| --- | --- |
| info | General information about the element. |
| messages | Service update, alerts, and other messages relevant to the element. |
| predictions | Predictions for the element. |

## Links to documentation

Use JSON-P if you’re writing JQuery code that requires a callback function.

| Page | Description |
| OVERVIEW |
| --- | --- |
| http://developer.metro.net/realtime-api-overview/ | This page |
| MIME TYPES |
| http://developer.metro.net/realtime-api-returning-json/ | application/json |
| http://developer.metro.net/realtime-api-returning-json-p/ | application/javascript |
| http://developer.metro.net/realtime-api-returning-xml/ | text/xml |
| COLLECTIONS |
| http://developer.metro.net/realtime-api-routes | Route methods |
| EXAMPLES |
| http://developer.metro.net/realtime-api-examples | Grab bag of examples |
