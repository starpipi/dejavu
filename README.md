# dejavu: The missing Web UI for Elasticsearch

[![GitHub License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/appbaseio/dejavu/dev/LICENSE.md) ![React Version](https://img.shields.io/badge/react-v15.6-brightgreen.svg)
[![Docker Pulls](https://img.shields.io/docker/pulls/appbaseio/dejavu.svg)](https://hub.docker.com/r/appbaseio/dejavu/)

1. **[Dejavu: Intro](#1-dejavu-intro)**
2. **[Features](#2-features)**
   a. [Easily Connect to Indices](#easily-connect-and-remember-indices)
   b. [Visual Filters](#visual-filters)
   c. [Enhanced Filtering with Queries](#enhanced-filtering-with-queries)
   d. [Modern UI Elements](#modern-ui-elements)
   e. [Realtime Data Updates](#realtime-data-updates)
   f. [Import JSON or CSV Data](#import-json-or-csv-data)
   g. [Build search UIs](#build-search-uis)
3. **[Comparison](#3-comparison-with-other-data-browsers)**
4. **[Roadmap](#4-roadmap)**
5. **[Build Locally / Contributing](#5-build-locally)**
6. **[Get Dejavu](#6-get-dejavu)**
   a. [Docker Installation](#docker-installation)
   b. [Hosted Alternatives](#hosted-alternatives)

---

### 1. Dejavu Intro

**dejavu** is the missing web UI for Elasticsearch. Existing web UIs leave much to be desired or are built with server-side page rendering techniques that make it less responsive and bulkier to run (I am looking at you, Kibana).

We started building dejavu with the goal of creating a modern Web UI (no page reloads, infinite scroll, filtered views, realtime updates, search UI builder) for Elasticsearch with 100% client-side rendering so one can easily run it as a [hosted app on github pages](https://dejavu.appbase.io), [as a chrome extension](https://chrome.google.com/webstore/detail/dejavu/jopjeaiilkcibeohjdmejhoifenbnmlh) or [as a docker image](https://hub.docker.com/r/appbaseio/dejavu/).

Starting `v1.0`, dejavu is the only Elasticsearch web UI that supports importing data via JSON and CSV files, as well as defining field mappings from the GUI.

Starting with `v1.5`, we support the ability of creating custom headers so you can easily pass different authentication headers, provide enhanced filtering and bulk updating of data via Elasticsearch's Query DSL.

Starting with `v2.0`, we support the ability to build faceted search UIs to test relevancy. You can also export the generated code to a codesandbox.

Starting with `v3.0`, we support the ability to connect to multiple indexes. You can also globally search across your indexes using global search bar.

### 2. Features

#### Easily Connect and Remember Indices

![Connect to an Index](https://www.dropbox.com/s/djlr7svk59ivqeh/f1.gif?raw=1)

Dejavu allows you to connect to any of the indexes present in your cluster and also caches each connected index locally so they are easily accessible when browsing again.

#### Visual Filters

![Filter Views](https://www.dropbox.com/s/qgniwj10ga2kbai/f2.gif?raw=1)

Sort through the data, find information visually, hide irrelevant data and make sense of all. With all the native data types we have . Global searchbar allows you to perform text search across your dataset.

Moreover, any filtered view can be exported as a JSON or CSV file.

#### Modern UI elements

![Pagination](https://www.dropbox.com/s/kl30dzi30265klq/f3.gif?raw=1)

It's not uncommon to have thousands of documents in your index. Dejavu supports paginated view which also allows you to change page size.

Dejavu also supports browsing data from multiple indexes and types, updating data either individually or via queries in bulk. Deletions are also supported.

#### Import JSON or CSV Data

![Import JSON or CSV files](https://www.dropbox.com/s/17xsh3edi9smiqf/f4.gif?raw=1)

Importer view allows importing CSV or JSON data directly into Elasticsearch through a guided data mappings configuration.

#### Build Search UIs

![Build search UIs](https://www.dropbox.com/s/73ab53rmgct5vxw/f5.gif?raw=1)

With Search Preview, you can now build visual search UIs, test search relevancy and export code to a codesandbox.

---

### 3. Comparison with other data browsers

|      Features      |                         dejavu                          |                   ES-head                    |              ES-kopf              |                       ES-browser                        |                        Kibana                        |
| :----------------: | :-----------------------------------------------------: | :------------------------------------------: | :-------------------------------: | :-----------------------------------------------------: | :--------------------------------------------------: |
|    Installation    |       Chrome extension, Docker Image, Hosted App.       |      Elasticsearch plugin, static page       | Elasticsearch plugin, static page | Elasticsearch plugin (doesn't work with v2.0 and above) |                 Elasticsearch plugin                 |
|     Modern UI      | Built with React v15.6.0, uses a live-reload interface. |  Built with jQuery v1.6.1, slightly stodgy   |      Built with Angular 1.x       |           Built with ExtJs, but a bit stodgy            |            Built with Node.JS, Hapi, Jade            |
|  Browser features  |           CRUD with support for data filters.           | Read data with support for full-text search. |           No data view            |           Data view support for a single type           | Read view with support for visualizations / charting |
| Data Import/Export |              Yes, in JSON and CSV formats.              |                      -                       |                 -                 |                            -                            |      Only export is supported, no CSV support.       |
|   Search Preview   |           Visually build and test search Ux.            |                      -                       |                 -                 |                            -                            |                          -                           |
|    Open Source     |                       MIT license                       |                 Apache v2.0                  |            MIT license            |                       Apache v2.0                       |                     Apache v2.0                      |

---

### 4. Roadmap

<s>Here's a rough roadmap of things to come in the version `1.0.0` release.</s>

:fireworks: We just hit the 1.0.0 roadmap.

-   [x] Battle-testing with different datasets
-   [x] Feature support for advanced filtering
        <s>Offline detection and reconnection for realtime updates</s>
-   [x] Performance improvements while scrolling
-   [x] Support for importing and exporting data
-   [x] Support for a continuous query view
-   [x] Available as a docker image

🍾 We just hit the 2.0.0 release.

-   [x] An intuitive data editing experience in tabular mode (v/s JSON edit mode)
-   [x] View data types from within the data browser view
-   [x] A more streamlined import process
-   [x] Refactor codebase to improve hackability (Migrate to React 16+, ES6 syntax)
-   [x] Ability to build (and test) search visually

:sparkles: We just hit the 2.0.0 release:

-   [x] Rewrite dejavu browser for high performance when browsing large datasets
-   [x] Support addition of custom analyzers, and updating index settings
-   [x] Make editing of data experience more intuitive (in addition to the raw JSON, show a relevant UI field with validations)
-   [x] Connectors to dashboarding systems for a more flavored visualization experience.

Roadmap beyond v3:

-   [ ] Improve coverage from 10% to 90%
-   [ ] Mobile friendly viewing and editing experience
-   [ ] Improve filtering support (add range filters, date filters)

---

### 5. Build Locally

See the **[CONTRIBUTING File](./CONTRIBUTING.md)**

---

### 6. Get Dejavu

#### Docker Installation

```
docker run -p 1358:1358 -d appbaseio/dejavu
open http://localhost:1358/
```

You can also run a specific version of **dejavu** by specifying a tag. For example, version `1.0.0` can be used by specifying the `docker run -p 1358:1358 appbaseio/dejavu:1.5.0` command.

##### CORS

To make sure you enable CORS settings for your ElasticSearch instance, add the following lines in the ES configuration file.

```sh
http.port: 9200
http.cors.allow-origin: "http://localhost:1358"
http.cors.enabled: true
http.cors.allow-headers : X-Requested-With,X-Auth-Token,Content-Type,Content-Length,Authorization
http.cors.allow-credentials: true
```

If you are running your Elasticsearch with docker, you can use flags to pass the custom CORS configuration. See the [docker-compose.yml](https://github.com/appbaseio/dejavu/blob/dev/docker-compose.yml) file for an example.

###### Elasticsearch v2.x

`docker run --name es -d -p 9200:9200 elasticsearch:2 -Des.http.port=9200 -Des.http.cors.allow-origin="http://localhost:1358" -Des.http.cors.enabled=true -Des.http.cors.allow-headers=X-Requested-With,X-Auth-Token,Content-Type,Content-Length,Authorization -Des.http.cors.allow-credentials=true`

###### Elasticsearch v5.x

`docker run --name es -d -p 9200:9200 -d elasticsearch:5 -E http.port=9200 -E http.cors.allow-origin="http://localhost:1358" -E http.cors.enabled=true -E http.cors.allow-headers=X-Requested-With,X-Auth-Token,Content-Type,Content-Length,Authorization -E http.cors.allow-credentials=true`

#### Hosted Alternatives

can also be run via hosted app at https://dejavu.appbase.io or [installed as a chrome extension](https://chrome.google.com/webstore/detail/dejavu/jopjeaiilkcibeohjdmejhoifenbnmlh).

For example: If you are using the chrome-extension instead of docker image, the `http.cors.allow-origin` in Elasticsearch.yml file would change accordingly:

```sh
http.port: 9200
http.cors.allow-origin: "chrome-extension://jopjeaiilkcibeohjdmejhoifenbnmlh"
http.cors.enabled: true
http.cors.allow-headers : X-Requested-With,X-Auth-Token,Content-Type,Content-Length,Authorization
http.cors.allow-credentials: true
```

---
